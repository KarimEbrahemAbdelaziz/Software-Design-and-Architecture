# Module 1 Notes

## Object-Oriented Thinking
By using objects to represent things in your code, the code stays **organized**, **flexible**, and **reusable**.

## Design in the Software Process
Software is developed through a process, generally iterative. The iterations consist of taking a set of requirements based on the identified problem(s) and using them to create **conceptual design** mock-ups and **technical design** diagrams, which can then be used to create a working software implementation, which must also pass testing.

It is important to allot time to form the requirements and design, even if they are not perfectly established.

**Requirements** are conditions or capabilities that must be implemented in a product, based on client or user request. They are the starting point of a project—you must understand what your client wants.

### Conceptual Design
The *conceptual design* recognizes appropriate **components**, **connections**, and **responsibilities** of the software product.

Conceptual designs are expressed or communicated through **conceptual mock-ups**. These are visual notations that provide initial thoughts for how requirements will be satisfied. Mock-ups for software involving user interfaces are often presented as reframes, which are a kind of blueprint or basic visual representation of the product.

### Technical Design
Technical designs build on conceptual designs and requirements to define the technical details of the solution.

In order to accomplish this, technical designs begin by splitting components into smaller and smaller components that are specific enough to be designed in detail. By breaking down components more and more into further components, each with specific responsibilities, you get down to a level where you can do a detailed design of a particular component. The final result is that each component will have their technical details specified.

In order to communicate technical design, technical diagrams are used. Technical diagrams visualize how to address specific issues for each component.

### Design for Quality Attributes
Sometimes, there are restrictions on design that require compromise. Besides software requirements based on desired functionality, there are also quality attributes to define how well this functionality must work. But your decisions may also involve trade-offs in different quality attributes, such as performance, convenience, and security, and these attributes need to be balanced.

**Context** provides important information when deciding on the balance of qualities in design.

### Satisfying Qualities
Qualities are achieved through satisfying functional and non- functional requirements, which in turn are the basis for the design process.
**Functional requirements** describe what the system or application is expected to do. **Non-functional requirements** specify how well the system or application does what it does.

## Class Responsibility Collaborator
During the process of conceptual design, it is helpful not only to identify components, responsibilities, and connections but also to represent them. One technique is to use **Class, Responsibility, Collaborator (CRC) cards**.

To keep track of each candidate component and its responsibilities using a CRC card, you place a component’s name in the class name section, and the responsibilities in the responsibilities section. Connections are captured in the collaborators section. 

A key advantage of using CRC cards is that they allow you to physically reorganize your design.
