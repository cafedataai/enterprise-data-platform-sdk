# Coding Guidelines

> **Project:** Enterprise Data Platform SDK
>
> **Organization:** Data & AI Cafe

---

# Purpose

This document defines the coding guidelines for the Enterprise Data Platform SDK.

The objective is to ensure that every contributor writes clean, maintainable, consistent, and production-ready code.

These guidelines apply to every Python module, package, and capability developed within this repository.

---

# General Principles

Code should be:

- Simple
- Readable
- Consistent
- Testable
- Maintainable
- Extensible

Always write code for humans first and computers second.

---

# Keep It Simple

Choose the simplest solution that correctly solves the problem.

Avoid unnecessary abstractions, nested logic, and overly clever implementations.

Good code should be easy to understand without requiring extensive explanation.

---

# Single Responsibility

Every module, class, and function should have a single responsibility.

If a class or function starts solving multiple problems, consider refactoring it.

---

# Small Functions

Functions should:

- Perform one task
- Have a clear purpose
- Be easy to read
- Be easy to test

Prefer functions that are approximately **10–30 lines** long. If a function grows much larger, consider extracting smaller helper functions.

---

# Small Classes

Classes should represent a single concept.

Avoid "God Classes" that manage multiple responsibilities.

Large classes are often a sign that responsibilities should be split.

---

# Avoid Deep Nesting

Avoid code like:

```python
if condition1:
    if condition2:
        if condition3:
            ...