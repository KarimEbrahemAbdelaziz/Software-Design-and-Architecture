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

### Facade Pattern

The façade design pattern provide a single, simplified interface for client classes to interact with a subsystem. It is a *structural* design pattern.

A façade is a wrapper class that encapsulates a subsystem in order to hide the subsystem’s complexity, and acts as a point of entry into a subsystem without adding more functionality in itself.

![uml](imgs\Example_of_Facade_design_pattern_in_UML.png)

In summary, the façade design pattern:

* Is a means to hide the complexity of a subsystem by encapsulating it behind a unifying wrapper called a façade class.
* Removes the need for client classes to manage a subsystem on their own, resulting in less coupling between the subsystem and the client classes.
* Handles instantiation and redirection of tasks to the appropriate class within the subsystem.
* Provides client classes with a simplified interface for the subsystem.
* Acts simply as a point of entry to a subsystem and does not add more functional the subsystem

### Adapter Pattern

Not all systems have compatible software interfaces. In other words, the output of one system may not conform to the expected input of another system. This frequently happens when a pre-existing system needs to incorporate third-party libraries or needs to connect to other systems. The **adapter design** pattern facilitates communication between two existing systems by providing a compatible interface. It is a *structural design pattern*.  

The adapter design pattern consists of several parts

* A *client class*. This class is the part of your system that wants to use a third-party library or external systems.
* An *adaptee class*. This class is the third-party library or external system that is to be used.
* An *adapter class*. This class sits between the client and the adaptee.
* A *target interface*. This is used by the client to send a request to the adapter.

![uml](imgs\Adapter.PNG)

In summary, an adapter is meant to:

* Wrap the adaptee and exposes a target interface to the client.
* Indirectly change the adaptee’s interface into one that the client is expecting by implementing a target interface.
* Indirectly translate the client’s request into one that the adaptee is expecting.
* Reuse an existing adaptee with an incompatible interface.  