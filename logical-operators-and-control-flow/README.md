# ![[tktk Module Name] - tktk Microlesson Name](./assets/logical-operators-and-control-flow.png)

**Learning objective:** By the end of this lesson, students will be able to explain how control flow is implemented in Java using block statements and scope. 

## Opening (5 min)

> Control flow structures are an important aspect of programming languages that allow your code to take certain actions based on a variety of scenarios. Control flow is a fundamental concept in programming that allows you to dictate how your code runs under different conditions or until a certain condition is met.

*The text above is from culttt.com.*

Control flow is a concept that's consistent across most programming languages. The components of control flow (loops, `if...else` conditionals, `switch` statements, comparison operators) are also universal principles.

What varies is the way different control flow components are implemented from language to language. Let's see how it's done in Java.

Java supports a compact set of statements — specifically control flow statements — that you can use to incorporate interactivity in your application.

-----

## Introduction: Logical Operators and Control Flow (10 min)

#### Block Statements

Statements meant to be executed after a control flow operation will be grouped into a **block statement**. These statements are wrapped around a pair of curly braces:

```java
{
  System.out.println("hello");
  System.out.println("roar");
}
```

#### Block Scope

Scope changes depending on whether a variable is defined in the class (we use the `mVariableName` convention for these) or in a method (these variables have local scope only and are not available outside that method).

In Java, variables defined in **block statements** modify scope, meaning those variables are not available outside of the block.

<!-- **Instructor Note**: Show the scope error in the IDE, then correct it as shown in the second code block.-->

For example:

```java
boolean beautiful = true;

if (beautiful) {
  String name = "lydia";
}

System.out.println(name); // symbol 'name' cannot be resolved
```

Variables defined in **block statements** are not available outside of the curly braces. How might we resolve this issue?

<!-- **Instructor Note**: First, try to print out `name` without an `else` statement, then add the `else` when the program still won't compile.-->

```java
boolean beautiful = true;
String name = "pepe";

if (beautiful) {
  name = "robin"; // Use the predefined variable.
}

System.out.println(name); //=> robin
```

_Written by Kristen Tonga_
