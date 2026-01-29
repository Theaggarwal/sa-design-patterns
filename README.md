# Design Patterns Implementation

This repository contains implementations of various design patterns in C#. Design patterns are reusable solutions to common problems in software design that provide templates for writing maintainable and scalable code.

## Table of Contents

- [Creational Patterns](#creational-patterns)
- [Structural Patterns](#structural-patterns)
- [Behavioral Patterns](#behavioral-patterns)
- [Architectural Patterns](#architectural-patterns)

---

## Creational Patterns

Creational patterns deal with object creation mechanisms, trying to create objects in a manner suitable to the situation.

### Abstract Factory
**Definition:** Provides an interface for creating families of related or dependent objects without specifying their concrete classes. It defines a factory interface that creates multiple related products.

**Use Case:** When you need to create families of related objects (e.g., GUI elements for different operating systems).

### Builder
**Definition:** Separates the construction of a complex object from its representation, allowing you to construct the object step by step. The builder pattern lets you produce different types and representations of an object using the same construction code.

**Use Case:** Creating complex objects with many optional parameters (e.g., constructing a custom pizza with various toppings).

### Factory Method
**Definition:** Defines an interface for creating an object, but lets subclasses decide which class to instantiate. It promotes loose coupling by eliminating the need for client code to know specific classes.

**Use Case:** When a class cannot anticipate the type of objects it needs to create, or when subclasses should specify the objects to create.

### Prototype
**Definition:** Specifies the kinds of objects to create using a prototypical instance, and creates new objects by copying this prototype. It allows you to clone objects without coupling to their concrete classes.

**Use Case:** When object creation is expensive or complex, and you need to create many similar objects (e.g., cloning game objects).

### Singleton
**Definition:** Ensures a class has only one instance and provides a global point of access to it. It restricts instantiation to a single object and provides a controlled way to access that instance.

**Use Case:** Managing shared resources like database connections, logging, or configuration managers.

---

## Structural Patterns

Structural patterns deal with object composition, creating relationships between entities to form larger structures while keeping these structures flexible and efficient.

### Adapter
**Definition:** Converts the interface of a class into another interface clients expect. It allows incompatible interfaces to work together by providing a wrapper that translates between them.

**Use Case:** Making incompatible interfaces compatible (e.g., adapting an old library interface to match a new one).

### Bridge
**Definition:** Decouples an abstraction from its implementation so the two can vary independently. It uses composition to separate the abstraction hierarchy from the implementation hierarchy.

**Use Case:** Avoiding permanent binding between abstraction and implementation (e.g., separating a shape's interface from its drawing mechanism).

### Composite
**Definition:** Composes objects into tree structures to represent part-whole hierarchies. It lets clients treat individual objects and compositions of objects uniformly.

**Use Case:** Representing hierarchical structures like file systems, organizational charts, or UI components.

### Decorator
**Definition:** Attaches additional responsibilities to an object dynamically, providing a flexible alternative to subclassing. It wraps an object with a decorator object that adds new functionality.

**Use Case:** Adding features to objects without modifying their structure (e.g., adding scrollbars or borders to a window).

### Facade
**Definition:** Provides a unified, simplified interface to a set of interfaces in a subsystem. It hides the complexity of a large subsystem behind a single interface.

**Use Case:** Simplifying the interaction with complex subsystems (e.g., a single API for a complicated library).

### Flyweight
**Definition:** Uses sharing to support large numbers of fine-grained objects efficiently. It reduces memory usage by sharing common state between multiple objects.

**Use Case:** Managing many similar objects with shared state (e.g., characters in a text editor or particles in a game).

### Proxy
**Definition:** Provides a surrogate or placeholder for another object to control access to it. It acts as an intermediary that can add additional functionality like lazy loading, caching, or access control.

**Use Case:** Controlling access to an object, lazy initialization, or logging access (e.g., a proxy for a database connection).

---

## Behavioral Patterns

Behavioral patterns focus on the responsibilities of objects and how they cooperate. They define how objects interact and distribute responsibility.

### Chain of Responsibility
**Definition:** Avoids coupling the sender of a request to its receiver by giving more than one object a chance to handle the request. It passes the request along a chain of handlers.

**Use Case:** Processing requests through multiple handlers (e.g., event handling, logging, or approval workflows).

### Command
**Definition:** Encapsulates a request as an object, allowing you to parameterize clients with different requests, queue requests, and support undoable operations.

**Use Case:** Implementing undo/redo functionality, queuing operations, or scheduling tasks.

### Interpreter
**Definition:** Defines a grammatical representation for a language and an interpreter to interpret sentences in that language. It helps define how to evaluate language syntax.

**Use Case:** Building domain-specific languages, expression evaluators, or query parsers.

### Iterator
**Definition:** Provides a way to access the elements of a collection sequentially without exposing its underlying representation. It decouples the algorithm from the data structure.

**Use Case:** Traversing different collection types uniformly (e.g., iterating over arrays, linked lists, or trees).

### Mediator
**Definition:** Defines an object that encapsulates how a set of objects interact. It promotes loose coupling by keeping objects from referring to each other explicitly.

**Use Case:** Centralizing complex communication logic between multiple objects (e.g., dialog box coordination).

### Memento
**Definition:** Without violating encapsulation, captures and externalizes an object's internal state without exposing its structure, allowing the object to be restored to this state later.

**Use Case:** Implementing undo functionality, saving game states, or transaction rollbacks.

### Observer
**Definition:** Defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified automatically.

**Use Case:** Event-driven programming, publishing-subscribing systems, or real-time data updates.

### State
**Definition:** Allows an object to alter its behavior when its internal state changes. The object will appear to change its class, while using composition instead of inheritance.

**Use Case:** Objects with state-dependent behavior (e.g., traffic lights, order processing workflows).

### Strategy
**Definition:** Defines a family of algorithms, encapsulates each one, and makes them interchangeable. It lets the algorithm vary independently from clients that use it.

**Use Case:** Selecting different algorithms at runtime (e.g., different sorting or payment methods).

### Template Method
**Definition:** Defines the skeleton of an algorithm in a base class, letting subclasses override specific steps without changing the algorithm's structure.

**Use Case:** Creating extensible frameworks where subclasses customize specific behaviors (e.g., data processing pipelines).

---

## Architectural Patterns

Additional architectural and organizational patterns.

### Private Class Data
**Definition:** Controls write access to class data by restricting it to methods of the class itself, while exposing read-only access through separate getter methods. It protects sensitive data from unauthorized modification.

**Use Case:** Ensuring data integrity and preventing accidental modifications to critical object state.

### Repository
**Definition:** Provides an abstraction for data access, mediating between the domain and data mapping layers. It acts as an in-memory collection of domain objects.

**Use Case:** Separating data access logic from business logic, enabling easier testing and switching data sources.

---

## Pattern Distribution

- **Creational Patterns:** 5 (Abstract Factory, Builder, Factory Method, Prototype, Singleton)
- **Structural Patterns:** 7 (Adapter, Bridge, Composite, Decorator, Facade, Flyweight, Proxy)
- **Behavioral Patterns:** 10 (Chain of Responsibility, Command, Interpreter, Iterator, Mediator, Memento, Observer, State, Strategy, Template Method)
- **Architectural Patterns:** 2 (Private Class Data, Repository)

**Total: 24 Design Patterns**

---

## How to Use

Each pattern is implemented in its own directory with:
- `Program.cs` - Example implementation and usage
- `[Pattern].csproj` - Project file
- `README.md` - Pattern-specific documentation

Navigate to the specific pattern folder to explore the implementation details.
