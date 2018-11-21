# Interfaces, protocols, traits, mixins, abstract classes

There are many ways to combine software code. This page explains a bit about
common patterns for combining code: interfaces, protocols, traits, mixins, abstract classes.

These languages all use similar techniques that have different names:

* Java interface
* Swift protocol
* Rust trait
* Ruby mixin
* C++ abstract class

These concepts are ways to do more-abstract composition instead of more-concrete inheritance.

These concepts may also be known as abilities, behaviors, capabilities, qualities, etc.

These concepts encourage code reuse, and tend to improve testability, maintainability, and even security.

These concepts are examples of the dependency inversion principle:

* High-level modules should not depend on low-level modules.

* Both should depend on abstractions.

* Abstractions should not depend on details.

How other classes gain access to the techniques depends on the particular language.


## Interface

An interface is a description of a code's capabilties and/or how to interact with the code.

* An interface provides definitions of functionality, such as functions, methods, messages, exceptions, etc.

* The interface is an agreement of what the object understands and how to interact with it.

* An interface is useful because it enables unrelated objects to communicate and/or co-operate.

* A class that has code and data for all the methods corresponding to an interface, and declaring so, is said to "implement" the interface.

* A class can implement multiple interfaces, and hence can be of different types at the same time.

* An interface a kind of type definition; anywhere an object can be exchanged (for example, in a function call or method call), the type of the object to be exchanged can be defined in terms of one of its implemented interfaces, rather than specifying a specific class. This approach means that any class that implements that interface can be used.

* An interface can contain any number of methods. For example, the Java language defines the interface "Readable" that has the single read() method; various implementations are used for different purposes, including FileReader, PipedReader, and StringReader.

* An interface can contain no methods. For example, the Java language define the interface "Serializable" that contains no methods and serves to provide run-time information to generic processing using reflection.

* An interface can be valuable for testing. For example, a dummy implementation may be used to allow development to progress before the final implementation is available. In another case, a fake or mock implementation may be substituted during testing. Such stub implementations are replaced by real code later in the development process.

* An interface can be valuable for trying multiple implementation strategies. For example, an interface can be implemented by writing typical code, and then implented again by writing very fast optimized code.


## Protocol

An object-oriented protocol is like an interface.

The first difference is that typically a protocol may have some method implementations, such as default code.

The second difference is that Apple favors the name "protocol" instead of "interface", which means that many iOS developers use the name "protocol".

An object-oriented protocol is totally different in meaning than a transmission protocol (such as SSH, FTP, HTTP).


## Trait

A trait is like a interface and a protocol.

The most important difference is that a trait provides all the method implementations a.k.a. the method bodies.

Traits also have useful properties in some languages:

* symmetric sum: an operation that merges two disjoint traits to create a new trait

* override (or asymmetric sum): an operation that forms a new trait by adding methods to an existing trait, possibly overriding some of its methods.

* alias: an operation that creates a new trait by adding a new name for an existing method.

* exclusion: an operation that forms a new trait by removing a method from an existing trait. (Combining this with the alias operation yields a shallow rename operation).

Traits can be composed in the following ways in some languages:

* Trait composition is commutative; the ordering of adding traits does not matter. For example, given trait S = A + B, then trait T = B + A is the same as S.

* Conflicting methods are excluded from the composition.

* Nested traits are equivalent to flattened traits; the composition hierarchy does not affect the traits behaviour. For example, given trait S = A + X, where X = B + C, then trait T = A + B + C is the same as S.[1]

Some languages and compilers (e.g. Rust) require traits to be explicated, which ensures the safety of generics in the language, and also helps to avoid major problems of templates (e.g. in C++).


## Mixin

A mixin is like an interface, protocol, and trait.

A mixin defines behaviors via full method definitions, same as a traits, and may also carry state through member variables, whereas traits usually don't.

A mixin can also be understood as an interface plus its implemented methods, and plus any member variables.

Mixins are useful when a programmer wants to share functionality between different classes. Instead of repeating the same code over and over again, the common functionality can simply be grouped into a mixin, then included into each class that requires it.


## Abstract class

An abstract class is, conceptually, a class that cannot be instantiated, and is usually implemented as a class that has one or more abstract functions a.k.a. pure virtual functions.

An abstract function, a.k.a. pure virtual function, is one which must be overridden by any concrete (i.e., non-abstract) derived class. In C++, this is indicated in the declaration with the syntax " = 0" in the member function's declaration.


## Summary

Comparison:

* An interface defines behaviors via method signatures (a.k.a. method headers) and never includes method implementations (a.k.a. the method bodies).

* An protocol defines behaviors via method signatures (a.k.a. method headers), same as an interface, and may also provide one or more method implementations (a.k.a. the method bodies).

* A trait defines behaviors via full method definitions, i.e. the trait provides all the method implementations a.k.a. the method bodies.

* A mixin defines behaviors via full method definitions, same as a traits, and may also carry state through member variables, whereas traits usually don't.

* An abstract class defines behaviors via method signatures (e.g. pure virtual functions) and can also include method implementations, member variables, helper methods, and more. An abstrace class is usable solely by its subclasses, which is unlike interaces, protocols, traits, and mixins.

Similarities:

* Interfaces, protocols, traits, and mixins are sometimes described as being "included" or "composed", rather than "inherited" or "subclassed".

* These avoid the inheritance ambiguity that multiple inheritance can cause, which is known as the "diamond problem".

* These all help with code sharing.


## See also

https://en.wikipedia.org/wiki/Protocol_(object-oriented_programming)

https://en.wikipedia.org/wiki/Traits_(computer_science)

https://en.wikipedia.org/wiki/Mixin

https://javascript.info/mixins
