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

## Factory Objects & Factory Method Pattern

The **Factory Method Pattern** is a *creational pattern*. In order to understand Factory Method patterns, we must first understand **factory objects**.

### Factory Objects

A factory object is an object whose role is to create "product" objects of particular types. Factory objects makes software easier to maintain and change, because object creation happens in the factories. The methods that use these Factories can then focus on other behaviour.

Benefits:

* is much simpler to add new types of an object to the object factory without modifying the client code
* allow client code to operate on generalizations (*coding to an interface*)
* cut out redundant code and made the software easier to modify, particularly if there are multiple clients that want to instantiate the same set of classes.

### Factory Method Pattern

Factory Method uses a separate "method" in the same class to create objects. The power of Factory Methods come in particular from how they create specialized product objects.

This design pattern's intent is to define an interface for creating objects, but let the subclasses decide which class to instantiate.

![uml](imgs\factoryMethodPattern.PNG)

There should be an abstract Creator class, that contains methods that only operate on generalizations. The Factory Method is declared by the Creator abstractly, so that each Concrete Creator class is obliged to provide a Factory Method.  

There should also be a subclass of the abstract Creator class, a Concrete Creator that is responsible for concrete instantiation. The Concrete Creator inherits methods from the abstract Creator.  

There should be a factoryMethod in the concrete creator subclass. Every time a Concrete Creator subclass is added to the design, the factoryMethod() must be defined to make the right products. This is how the subclass "decides" to create objects.

If object creation is separate from other behaviour, the code becomes cleaner to read, and easier to maintain or change. The client code is simplified. The code becomes more extensible, and inheritance allows for the specialization of object creation.