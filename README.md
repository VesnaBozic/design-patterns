# Design patterns in Python


## Definition

The design pattern is a technique which used by the developer to solve the commonly occurring software design. In simple word, it is a predefine pattern to solve a recurring problem in the code. These patterns are mainly designed based on requirements analysis.

The design pattern is a part of the software development. It is a general repeatable solution for the potential problem in software development. We can follow the patterns details and apply a solution which suits our code.


We may often confuse the patterns and algorithm, but both are separate approaches to solve repetitive problems. Algorithms generally define the clear set of the solution that can be implemented in some problems, where the patters are high-level description of the solution.

***The pattern is not a specific piece of code, but a general concept for solving a particular problem. You can follow the pattern details and implement a solution that suits the realities of your own program.***

For example - An algorithm is like a cooking recipe: we have a clear set of ingredients (or set of solutions) to cook something (problems or goals). On the other side, a pattern is like a blueprint: we can see what the result and its features are, but we can modify the order of implementation.

All design pattern containt the following elements

• Intent/purpose of the pattern briefly describes both the problem and the solution.

• Motivation/context further explains the problem and the solution the pattern makes possible.

• Structure of classes shows each part of the pattern and how they are related.

• Sample code in one of the popular programming languages makes it easier to graso the idea behind the pattern.


## Why use design patterns?

Because they offer us tried and tested solution for the specific problems. It give us record of execution to decrease any technical risk to the projects. We can use them easily and flexible.

Design patterns have the predefined set of tried and tested solutions to a common problem encountered while developing software. If we know about the design pattern, then we can apply the solution without wasting time. It also teaches us how to solve the problem using the principle of object-oriented design.

Design pattern also enhances the common understanding between the developer and their teammates. 

Design patterns are also useful for the learning purpose because they introduce the common problem that we may have ignored. They also allow thinking that area that may not have had the hand-on experience.


## Clasification

 #### CREATIONAL
 
 Deals with the elements in the system - how they are created. 
 
 Some of the patterns : Constructor, Factory, Abstract, Prototype, Singleton, Builder.

#### STRUCTURAL

Deals with compostion. The structural patterns deal with how classes and objects are composed. Objects can be composed using inheritance to obtain new functionality. When we need change in one part of the system, the rest of the system doesn't need to change.

Some of the patterns : Decorator, Facade, Flyweight, Adapter, Proxy.

#### BEHAVIORAL PATTERNS

These design patterns are focused on the interaction between different objects in the system.

Some of the patterns : Iterator, Mediator, Observer, Visitor.


***Beside these patterns there are architectural patterns. For example : Client-Server, REST, peer to peer***

## The Singleton Pattern

Singleton is a creational design pattern that lets you ensure that a class has only one instance, while providing a global access point to this instance.

The Singleton pattern lets you access some object from anywhere in the program.

All implementations of the Singleton have these two steps in common:

- Make the default constructor private, to prevent other objects from using the new operator with the Singleton class.

- Create a static creation method that acts as a constructor. Under the hood, this method calls the private constructor to create an object and saves it in a static field. All following calls to this method return the cached object.

If our code has access to the Singleton class, then it’s able to call the Singleton’s static method. So whenever that method is called, the same object is always returned.

##### Example 

```
The government is an excellent example of the Singleton pattern. A country can have only one official government.
```

**Use the Singleton pattern when a class in your program should have just a single instance available to all clients; for example, a single database object shared by different parts of the program.**

**The Singleton pattern disables all other means of creating objects of a class except for the special creation method. This method either creates a new object or returns an existing one if it has already been created.**


#### How to implement

Add a private static field to the class for storing the singleton instance.

Declare a public static creation method for getting the singleton instance.

Implement “lazy initialization” inside the static method. It should create a new object on its first call and put it into the static field. The method should always return that instance on all subsequent calls.

Make the constructor of the class private. The static method of the class will still be able to call the constructor, but not the other objects.

Go over the client code and replace all direct calls to the singleton’s constructor with calls to its static creation method.







