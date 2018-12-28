# Introduction to Design Patterns: Creational & Structural Pattern

## Introduction to Design Patterns

A design pattern is a practical proven solution to a recurring design problem.

One of the most famous books on design patterns is *Design Patterns: Elements of Reusable Object-Oriented Software* by Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides. This course will draw upon a selection of the patterns presented in this book.

### Gang of Four’s Pattern Catalogue

The grouping of patterns together forms a catalog, otherwise known as the **Gang of Four’s design pattern catalog**.

Depending on the context of the problem, you would select a different **pattern language** to use. A pattern language is a collection of patterns that are related to a certain problem space.

Categories of patterns

* **Creational patterns**: deal with the creation or cloning new objects. Creational patterns depend on the programming language being used.
* **Structural patterns** describe how objects are connected to each other. These patterns relate to the design principles of decomposition and generalization.
* **Behavioural patterns** focus on how objects distribute work, and describe how each object does a single cohesive function.

## Singleton Pattern

A **singleton** is a *creational pattern*, which describes a way to create an object.

The intent of a Singleton pattern is to provide global access to a class that is restricted to one instance. In general, this is achieved by having a private constructor, with a public method that instantiates the class "if" it is not already instantiated.

An advantage of this version of a Singleton class is **lazy creation**. Lazy creation means that the object is not created until it is truly needed.

There are trade-offs to the Singleton design principle. If there are multiple computing threads running, there could be issues caused by the threads trying to access the shared single object.

## Factory Method Pattern