---
title: "Stop Writing Java in Python"
description: "A guide for Java developers learning to write Pythonic code by unlearning Java habits and embracing Python's module-based, function-first approach."
date: 2026-01-20
---

# Stop Writing Java in Python: How to Think Pythonically as a Java Developer

## Prerequisites

This tutorial assumes you have experience with Java and basic familiarity with Python syntax.

---

## Introduction

When I first started learning Python after years of writing Java, I did what felt natural: I put everything into classes.

Utility classes. Service classes. Manager classes.  
Sometimes even a class with a single `@staticmethod`.

The code worked. Tests passed. Nothing was technically wrong.

But it didn’t feel right.

Instead of helping me move faster, Python felt like something I had to wrestle with. I wasn’t writing *bad* code—but I was clearly writing code the language didn’t want.

If you’re a Java developer learning Python, you might recognize this feeling. Python doesn’t force object-oriented design, and that freedom can be unsettling. Where are the interfaces? Where does shared logic live? Why are there so many top-level functions?

In this tutorial, you’ll learn **why Java-style Python often feels wrong**, even when it runs correctly—and how to shift your mindset so your code feels natural in Python.

This isn’t a syntax comparison or a beginner’s guide. It’s about **unlearning habits that don’t translate well from Java** and replacing them with Pythonic ways of structuring programs.

By the end, you’ll understand:

- Why not everything should be a class in Python  
- How **modules** replace many Java utility patterns  
- When classes *do* make sense in Python  
- Practical rules of thumb for writing idiomatic Python as a Java developer  

---

## Why Java Developers Put Everything in Classes

In Java, classes are not optional. They’re the fundamental unit of structure.

If you want a function, it must live inside a class.  
If you want organization, you use packages and class hierarchies.  
If you want reuse, you reach for interfaces or abstract base classes.

Over time, Java encourages habits that make perfect sense:

- Grouping related functions into utility classes  
- Using static methods for stateless behavior  
- Designing class hierarchies early  
- Treating “object-oriented” as synonymous with “well-structured”  

So when Java developers move to Python, they often bring that structure with them.

Here's a familiar pattern:

```python
class StringUtils:
    @staticmethod
    def is_blank(value: str) -> bool:
        return not value or value.strip() == ""
```

Nothing here is wrong. The code is readable and testable.

But this is often a sign that you're writing Java in Python.

---

## Modules Are the Default Unit of Organization in Python

In Python, a .py file is a module, and modules already provide namespacing and structure.

A module can contain:

- Functions
- Constants
- Classes
- Imports

Because of this, many Java-style utility classes simply aren’t needed.

The previous example is more commonly written like this:

```python
def is_blank(value: str) -> bool:
    return not value or value.strip() == ""
```

Placed inside `string_utils.py`.

You still get:

- Logical grouping
- Clear imports
- Easy testability
- Explicit namespacing

You just avoid an extra class layer that adds no state and no behavior.

> **Tip:** In Python, a class that contains only static methods is often a code smell. It usually means the class is being used for organization rather than modeling behavior.

---

## A Concrete Refactor: From Java-Style to Pythonic

Here's a pattern I used a lot early on:

```python
class OrderService:
    @staticmethod
    def calculate_total(order):
        return sum(item.price for item in order.items)
```

A more Pythonic version separates data from behavior:

```python
from dataclasses import dataclass

@dataclass
class Item:
    price: float

@dataclass
class Order:
    items: list[Item]

def calculate_total(order: Order) -> float:
    return sum(item.price for item in order.items)
```

Nothing magical happened—we just let functions live where they belong and used a class only where it adds value.

This shift alone removed a surprising amount of friction for me.

---

## Functions Are First-Class Citizens in Python

One of the biggest mindset shifts for Java developers is that functions are first-class objects in Python.

Functions can be:

- Passed as arguments
- Returned from other functions
- Stored in data structures
- Defined at the top level of a module

For example:

```python
def apply(fn, value):
    return fn(value)
```

In Java, this requires lambdas and functional interfaces. In Python, it's ordinary code.

Because functions are lightweight, Python code often favors:

- Small, focused functions
- Clear data flow
- Composition over inheritance

The result is usually flatter, easier-to-refactor designs.

---

## Duck Typing: Interfaces Without Interfaces

A common Java question is: “But where are the interfaces?”

In Python, behavior matters more than inheritance.

```python
def serialize(obj) -> str:
    return obj.to_json()
```

Any object with a `to_json()` method works—no shared base class required:

```python
class User:
    def to_json(self) -> str:
        ...

class Order:
    def to_json(self) -> str:
        ...
```

> **Note:** This is called duck typing: if it walks like a duck and quacks like a duck, Python doesn't care what it inherits from.

---

## When Classes Do Make Sense in Python

Python isn’t anti–object-oriented. It’s selectively object-oriented.

Classes make sense when you need to:

- Combine state and behavior
- Model a domain concept
- Give objects a clear lifecycle

For example:

```python
class User:
    def __init__(self, name: str, is_active: bool = True):
        self.name = name
        self.is_active = is_active

    def deactivate(self) -> None:
        self.is_active = False
```

This class holds state and exposes meaningful behavior. That's exactly what classes are for.

> **Warning:** If a class exists only to group functions, it's probably unnecessary.

---

## Data First, Then Behavior

In Java, data is typically private and accessed through getters and setters.
In Python, attributes are usually public by default:

```python
class Config:
    def __init__(self, timeout: int):
        self.timeout = timeout
```

This isn't laziness—it's a deliberate trade-off.

Python emphasizes:

- Readability over ceremony
- Convention over enforcement
- Trust between developers

When more control is needed, Python gives you tools like properties, data classes, and validation libraries—but you apply them when they solve a real problem, not by default.

---

## Stop Designing Hierarchies Too Early

Java developers are often trained to design class hierarchies up front:

- Interfaces first
- Abstract base classes
- Concrete implementations

In Python, this is frequently unnecessary—and sometimes counterproductive.

Python favors:

- Simple concrete implementations
- Refactoring toward abstraction later
- Duck typing over inheritance

Instead of asking "What interface should this implement?", Python developers usually ask:

"What behavior do I need right now?"

---

## Practical Rules of Thumb for Java Developers

If you're transitioning from Java to Python, these guidelines can save you time:

- If a class has no state, consider using a function instead
- If you're grouping related functions, use a module—not a class
- Prefer simple data structures over deep object hierarchies
- Delay abstraction until you see real duplication
- Use classes to model behavior, not organization
- Let readability guide your design decisions

These aren't strict rules, but they reflect how idiomatic Python is commonly written.

---

## Summary

The hardest part of learning Python as a Java developer isn’t the syntax—it’s letting go of habits that no longer serve you.

Python doesn't reject structure. It just offers different tools:

- Modules instead of utility classes
- Functions instead of forced methods
- Composition instead of rigid hierarchies

Once you stop trying to write Java in Python, the language starts to feel lighter and more expressive. That's usually when learning Python becomes enjoyable instead of frustrating.

---

## Next Steps

As an exercise, try refactoring a small Java-style Python project:

- Remove utility classes
- Flatten class hierarchies
- Replace static methods with module-level functions

You’ll likely find the result easier to read, test, and maintain.

