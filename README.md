# Design patterns in Python


## Definition

The design pattern is a technique which used by the developer to solve the commonly occurring software design. In simple word, it is a predefine pattern to solve a recurring problem in the code. These patterns are mainly designed based on requirements analysis.

The design pattern is a part of the software development. It is a general repeatable solution for the potential problem in software development. We can follow the patterns details and apply a solution which suits our code.

We may often confuse the patterns and algorithm, but both are separate approaches to solve repetitive problems. Algorithms generally define the clear set of the solution that can be implemented in some problems, where the patters are high-level description of the solution.

For example - An algorithm is like a cooking recipe: we have a clear set of ingredients (or set of solutions) to cook something (problems or goals). On the other side, a pattern is like a blueprint: we can see what the result and its features are, but we can modify the order of implementation.

All design pattern containt the following elements

• Pattern name

• Intent/purpose

• Aliases

• Motivation/context

• Problem

• Solution

• Structure

• Participants

• Collaborations

• Consequences/constraints

• Implementation

• Sample code

• Known uses

• Related patterns

## Why use design patterns?

Because they offer us tried and tested solution for the specific problems. It give us record of execution to decrease any technical risk to the projects. We can use them easily and flexible.

Design patterns have the predefined set of tried and tested solutions to a common problem encountered while developing software. If we know about the design pattern, then we can apply the solution without wasting time. It also teaches us how to solve the problem using the principle of object-oriented design.

Design pattern also enhances the common understanding between the developer and their teammates. 

Design patterns are also useful for the learning purpose because they introduce the common problem that we may have ignored. They also allow thinking that area that may not have had the hand-on experience.


## Clasification

 #### CREATIONAL
 
 Deals with the elements in the system - how they are created. 

#### STRUCTURAL

The structural patterns deal with how classes and objects are composed. Objects can be
composed using inheritance to obtain new functionality

#### BEHAVIORAL PATTERNS

These design patterns are focused on the interaction between objects

## The Singleton Pattern

#### The problem

One of the first debugging techniques we learn is simply printing the values of certain
variables to the console. This helps us see what is going on inside our program. Looking at the output of our program at different points in its execution helps us locate and fix bugs swiftly.

But us our code quickly becomes more complicates it becaomes littered with print statements, and that’s fine, until the moment we have to deploy our code. Running your code on a server, as a scheduled job on your own machine, or as a standalone piece of software on a client’s computer means that we can no longer rely on the console for feedback when something goes wrong.
We have no way of knowing what went wrong or how to replicate the issue. This takes
debugging from the realm of science straight into gambling. 

The simplest solution is to replace print statements with a command to write the output to a file instead of to the console, like this:

```
def log_message(msg):
    with open("filename.log", "a") as log_file:
        log_file.write("{0}\n".format(msg))
        
log_message("save this for later")
```

Now you can see what is happening in the program when things go wrong. Our log
file is like a black box on an aircraft: it keeps a tally of our program’s execution. When
our program crashes, we can pop open the black box and see what happened leading
up to the crash, as well as where you should start looking for a bug.

The log_message function opens a file and appends the message passed to it to the
file. This is the DRY principle in action. DRY stands for don’t repeat yourself.
Whenever possible, We should repackage the code in such a way that you can reuse it without the need to copy and paste the lines somewhere else.

#### Singleton Design Pattern in Python

As the name describes itself, it is a way to provide one object of a particular type. It is used to describe the formation of a single instance of class while offering a single global access point to the object.

It prevents the creation of multiple objects of the single class. The newly created object will be shared globally in an application.

We can understand it with the simple example of Data connectivity. While setting up the database connection, we generate an exclusive Database connection object to work with the Database. We can perform every operation regarding database using that single connection object. This process is called a Single design pattern.

One of the best benefits of using a singleton pattern is that we can restrict the shared resource and maintain integrity. It also prevents the overwriting in the current code by the other classes ensuing perilous or incompetent code. We can call the same object at multiple points of programs without worrying that it may be overwritten in the same points.

#### Advantages of Singleton Patterns

A class created using the singleton pattern violates the Single Responsibility Principle, which means it can solve two problems simultaneously.

Single Pattern is difficult to implement in the multithreading environment because we need to ensure that the multithreading environment wouldn't create singleton objects several times.

It makes the unit testing very hard because they follow the global state to an application.

#### Disadvantages of Single Pattern

A class created using the singleton pattern violates the Single Responsibility Principle which means it can solve two problems at a single time.

Single Pattern is difficult to implement in the multithreading environment, because we need to ensure that multithreading environment wouldn't create singleton object several times.

It makes the unit testing very hard because they follow the global state to an application

#### Applicability of Design Pattern

In the project, where we need a firm control over the global variables, we must use the Singleton Method.

Singleton patterns solves the most occurring problems such as logging, caching, thread pools, and configuration setting and often used in conjunction with the Factory design pattern.


