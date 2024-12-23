<h1>
  <span class="headline">Java Control Flow</span>
  <span class="subhead">Unconditional Branching Statements</span>
</h1>

**Learning objective:** By the end of this lesson, you'll be able to code efficient `for` loops and `switch` branching in Java by avoiding unnecessary statement executions using unconditional branching statements.

## An introduction to unconditional branching control flow

Unconditional branching statements alter the normal flow of program execution without evaluating a condition. It is also known as **jumping**. Let's look at two of the most used unconditional branching statements while dealing with loops and branches:

- `break` statement
- `continue` statement

## `break` statement

The break statement is used to terminate the execution of a loop or a switch statement prematurely. When encountered, it immediately transfers control to the statement following the loop or switch block. The primary purpose of the break statement is to improve the execution time by:

- Optimizing loop execution by exiting early when a goal is met and avoiding indefinite loop scenarios.
- Preventing fall-through in a `switch` control flow

A `switch` statement can be written without the `break` statement in each of the `case` statement blocks. However, the program will execute the code for the matched `case` statement block and continue executing all subsequent `case` statement blocks until it reaches the end of the `switch` block. This behavior is called **fall-through**.

**Example 1**: Decide the type of coffee based on the order number entered in a coffee machine but allow fall-through by not using the `break` statement.

```java
int orderNumber = 2;

switch (orderNumber) {
    case 1:
        System.out.println("Espresso");
    case 2:
        System.out.println("Latte");
    case 3:
        System.out.println("Cappuccino");
    default:
        System.out.println("Unknown order");
}
// Output: 
// Latte
// Cappuccino
// Unknown order
```

**Example 2**: Count the number of steps taken in a day until the goal of 10,000 steps is reached except on rest day.

```java
int steps = 0;
int goal = 10000;
boolean restDay = true;

while (steps < goal) {
    steps += 2000; // Simulate taking 2000 steps
    if (restDay){
      System.out.println("Take a break today")
      break;
    }
    System.out.println("Current steps: " + steps);
}
// Prints: Take a break today
```

## `continue` statement

The `continue` statement skips the current iteration of a loop and moves to the next iteration.

Example:

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) continue; // Skip when i is 3
    System.out.println(i);
}
// Prints:
// 1
// 2
// 4
// 5
```
