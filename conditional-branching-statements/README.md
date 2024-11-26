<h1>
  <span class="headline">Java Control Flow</span>
  <span class="subhead">Conditional Branching Statements</span>
</h1>

**Learning objective:** By the end of this lesson, you'll be able to write java code that can branch the control flow during execution using conditional branching statements 

## An introduction to conditional branching control flow
Conditional branching statements in Java allow a program to execute specific **block statements** based on conditions. These statements evaluate expressions using conditional operators and "branch" the flow of execution accordingly. The conditional branching options in Java are:
- `if` statement
- `if-else` statement
- `if-else-if` ladder
- `switch` statement

## Java Block Statements
A block statement in Java is a group of zero or more statements enclosed within curly braces `{}`. It is used to combine multiple statements into a single unit or **scope**, allowing the program to consider them as one statement. Variables declared inside a block are local to the block and cannot be accessed outside of it. 
Syntax:
```java
{
    // Statements go here
    statement1;
    statement2;
    ...
}
```
Understanding statement blocks helps you organize your code into reusable, logical sections, improving readability and debugging efficiency. It's the foundation of structured programming. In the context of java control flow manipulation, block statements are used to gather and represent all the statements that represent an independent branch to be executed conditionally or iterated repetitively. 

## `if` Statement
The `if` statement executes a block statement only if a condition evaluates to true. It is used for simple 'to execute or to not execute' scenarios.

Syntax:
```java
if (condition) {
    // Statements to execute if the condition is true
}
```

Example: Checking if a store is open based on the current hour
```java
int hour = 10; // Current hour in 24-hour format

if (hour >= 9) {
    System.out.println("The store is open.");
}
// Output: The store is open.
```

## `if-else` statement
The `if-else` statement executes one block of code if the condition is true, and another block if it is false. It is used for either-or branching scenarios.

Syntax:
```java
if (condition) {
    // Statements to execute if the condition is true
} else {
    // Statements to execute if the condition is false
}
```

Example: Checking if a store is open or closed at a specified hour
```java
int hour = 20; // 8 PM in 24-hour format

if (hour < 18) {
    System.out.println("The store is open.");
} else {
    System.out.println("The store is closed.");
}
// Output: The store is closed.
```

## `if-else-if` ladder
The `if-else-if` ladder is used for multiple conditions where different blocks of code are executed based on different conditions. In this ladder, the conditional expression of each `if`/`else if` rung is evaluated sequentially until one of them evaluates to `true`. The `else` statement block is executed if the `if` statement and all the `else if` statements evaulated to `false`. It is used for multiple control flow branching scenarios, each based on it's own Boolean expression evaluation.

Syntax:
```java
if (condition1) {
    // Code to execute if condition1 is true
} else if (condition2) {
    // Code to execute if condition2 is true
} else {
    // Code to execute if all conditions are false
}
```

Example: Categorizing a person's age group
```java
int age = 25;

if (age < 13) {
    System.out.println("Child");
} else if (age < 20) {
    System.out.println("Teenager");
} else if (age < 60) {
    System.out.println("Adult");
} else {
    System.out.println("Senior");
}
// Output: Adult
```

## `switch` statement
The switch statement evaluates a variable and matches its value against multiple cases, executing the corresponding `case` statement block. The `default` statement block is executed if there is no matching `case`. It is used for multiple control flow branching scenario based on a single variable's value.

Syntax:
```java
switch (variable) {
    case value1:
        // Code to execute if variable == value1
        break;
    case value2:
        // Code to execute if variable == value2
        break;
    // Additional cases...
    default:
        // Code to execute if no cases match
}
```

Example: Deciding the type of coffee based on the order number entered in a coffee machine.
```java
int orderNumber = 2;

switch (orderNumber) {
    case 1:
        System.out.println("Espresso");
        break;
    case 2:
        System.out.println("Latte");
        break;
    case 3:
        System.out.println("Cappuccino");
        break;
    default:
        System.out.println("Unknown order");
}
// Output: Latte
```