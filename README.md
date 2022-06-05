# Design patterns


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

Problems that occur frequently enough in tech life usually have well-defined solutions, which are flexible, modular and more understandable. These solutions when abstracted away from the tactical details become design patterns.


## Example 

The class constructor is one of the basic concepts in an object oriented language. The constructors help create objects of the class and can take in parameters.

```
public class Aircraft {

    private String type;

    public Aircraft(String type) {
        this.type = type;
    }
}
```


In the above example, we have the default constructor for the class that takes in a single parameter the type of the aircraft. Now say after a few days, you realize you want to add additional properties to your Aircraft class. Say you want to add the color of the aircraft as a property, but you have already released a version of your library and can't modify the original constructor. The solution is to add another constructor with two parameters like so

```
public class Aircraft {

    private String type;
    private String color;

    public Aircraft(String type) {
        this.type = type;
    }

    public Aircraft(String type, String color) {
        this.type = type;
        this.color = color;
    }
}
```

If we continue this way we'll end up having a bunch of constructors with increasing number of arguments. It's called telescoping pattern.

***The telescoping pattern*** is called an anti-pattern: how NOT to do things!


### Tips for Object Oriented Design

- Separate out parts of code that vary or change from those that remain the same.

- Always code to an interface and not against a concrete implementation.

- Encapsulate behaviors as much as possible.

- Favor composition over inheritance. Inheritance can result in explosion of classes and also sometimes the base class is fitted with new functionality that isn't applicable to some of its derived classes.

- Interacting components within a system should be as loosely coupled as possible.

- Ideally, class design should inhibit modification and encourage extension.

## Types of Design Patterns

Design patterns for object orientated programs are divided into three broad categories :

- Creational

- Structural

- Behavioural

### Creational

Creational design patterns relate to how objects are constructed from classes. New-ing up objects may sound trivial but unthoughtfully littering code with object instance creations can lead to headaches down the road. The creational design pattern come with powerful suggestions on how best to encapsulate the object creation process in a program.

- Builder Pattern
- ProtoType Pattern
- Singleton Pattern
- Abstract Factory Pattern

### Structural 

Structural patterns are concerned with the composition of classes i.e. how the classes are made up or constructed. These include:

- Adapter Pattern

- Bridge Pattern

- Composite Pattern

- Decorator Pattern

- Facade Pattern

- Flyweight Pattern
 
- Proxy Pattern

### Behavioral

Behavioral design patterns dictate the interaction of classes and objects amongst eachother and the delegation of responsibility.

- Interpreter Pattern

- Template Pattern

- Chain of Responsibility Pattern

- Command Pattern

- Iterator Pattern

- Mediator Pattern

- Memento Pattern

- Observer Pattern

- State Pattern

- Strategy Pattern

- Visitor Pattern




