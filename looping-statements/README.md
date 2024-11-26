<h1>
  <span class="headline">Java Control Flow</span>
  <span class="subhead">Looping statements</span>
</h1>

**Learning objective:** By the end of this lesson, you'll be able to write java code that can manipulate the control flow to repeatedly execute a block of statement using looping statements

## An introduction to looping control flow
Loops in Java allow repetitive execution of a statement block as long as a condition is met. Java provides three principal looping constructs: 
- `for` loops
- `while` loops
- `do-while` loops

## `for` loops
A `for` loop is used when the number of iterations has already been determined before beginning the iterations.

Syntax:
```java
for (initialization; condition; increment/decrement) {
    // Statement block to execute repeatedly
}
```

Example: Printing numbers on a scoreboard from 1 to 5.
```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Scoreboard Number: " + i);
}
// Output:
// Scoreboard Number: 1
// Scoreboard Number: 2
// Scoreboard Number: 3
// Scoreboard Number: 4
// Scoreboard Number: 5
```

## `while` loops
A `while` loop is used when the number of iterations is undetermined until the iterations start executing, and depends on a condition.

Syntax:
```java
while (condition) {
    // Statement block to execute repeatedly while the condition is true
}
```

Example: Counting the number of steps taken in a day until the goal of 10,000 steps is reached.
```java
int steps = 0;
int goal = 10000;

while (steps < goal) {
    steps += 2000; // Simulate taking 2000 steps
    System.out.println("Current steps: " + steps);
}
// Output:
// Current steps: 2000
// Current steps: 4000
// Current steps: 6000
// Current steps: 8000
// Current steps: 10000
```

## `do-while` loops

A `do-while` loop is used when you need to execute the looped statement block at least once, regardless of the `while` condition.

Syntax:
```java
do {
    // Statement block to execute repeatedly
} while (condition);
```

Example: Asking for a password repeatedly until the correct password is entered.
```java
String correctPassword = "java123";
String enteredPassword;
int attempts = 0;

do {
    enteredPassword = "guess" + attempts; // Simulate user input
    System.out.println("Attempting with: " + enteredPassword);
    attempts++;
} while (!enteredPassword.equals(correctPassword));

// Output:
// Attempting with: guess0
// Attempting with: guess1
// Attempting with: guess2
// ...
// Attempting with: java123
```