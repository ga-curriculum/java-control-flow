<h1>
  <span class="headline">Java Control Flow</span>
  <span class="subhead">Conditional Operators</span>
</h1>

**Learning objective:** By the end of this lesson, you'll be able to write java code to demonstrate the working of comparison and boolean operators.

## An introduction to conditional operators

Operators are special symbols that perform specific operations on one, two, or three operands, and then return a result. Conditional operators are used to evaluate conditions and make decisions based on Boolean logic. In other words, after performing the required operation on their operands, conditional operators return the result as a boolean value of `true` or `false`. Conditional operators make conditional branching and condition based iterating of loops possible.

## Types of conditional operators
There are three types of conditional operators in Java:
- Relational/Comparison operators
- Logical/Boolean operators
- Ternary operator

## Relational/Comparison operators
Relational or Comparison operators in Java are used to compare two values and return a Boolean result.

| Operator | Operator Description |
|:---:|:---|
|`==`|Is LHS **equal to** RHS?|
|`!=`|Is LHS **not equal** to RHS?|
|`<`|Is LHS **less than** RHS?|
|`>`|Is LHS **greater than** RHS?|
|`<=`|Is LHS **less than or equal to** RHS?|
|`>=`|Is LHS **greater than or equal to** RHS?|

*_LHS stands for any expression on the Left Hand Side of the operator and RHS stands for any expression on the Right Hand Side of the operator._


Lets understand these relational/comparison operators better through examples.

Example 1: Veryfying if two integers are equal
```java
int x = 10;
int y = 20;
boolean isEqual = (x == y);
System.out.println(isEqual); // Output: false
```
>⚠ Notice the difference between the usage of `=` as an assignment operator and as a comparison operator.

Example 2: Verifying if two strings are different
```java
String str1 = "Hello";
String str2 = "World";
boolean isNotEqual = str1 != str2;
System.out.println(isNotEqual); // Output: true
```
Example 3: Veryfying if a person is a minor
```java
int age = 16;
boolean isMinor = age < 18;
System.out.println(isMinor); // Output: true
```

## Logical/Boolean operators
Logical or operators in Java allow you to combine or invert Boolean expressions, enabling more complex logic. These operators work on true and false values and return a Boolean result. They are often used in conditional checks, but they can also be applied independently for tasks like data validation or logical comparisons.

| Operator | Operator Description |
|:---:|:---|
|`&&`|Logical AND. Returns `true` if both LHS and RHS expressions are `true`.|
|`\|\|`|Logical OR. Returns `true` if even one of the expressions, LHS or RHS is `true`.|
|`!`|Logical NOT. Returns the inverted boolean value of the expression that follows it.|

Lets understand these relational/comparison operators better through examples.

Example 1: Verifying if user supplied both user name and password correct before authenticating
```java
boolean isUsernameCorrect = true;
boolean isPasswordCorrect = false;
boolean isAuthenticated = isUsernameCorrect && isPasswordCorrect;
System.out.println(isAuthenticated); // Output: false
```
Example 2: Verifying if a customer satisfies at least one of the conditions for discount
```java
boolean hasPromoCode = false;
boolean isPrimeMember = true;
boolean eligibleForDiscount = hasPromoCode || isPrimeMember;
System.out.println(eligibleForDiscount); // Output: true
```
Example 3: Negating a condition based on another mutually exclusive condition
```java
boolean isWeekend = false;
boolean isWeekday = !isWeekend;
System.out.println(isWeekday); // Output: true
```
Example 4: Now, lets make things interesting by combining more than one logical operations in a single statement.
```java
boolean isEmployee = true;
boolean hasAccessCard = false;
boolean canAccessOffice = isEmployee && !hasAccessCard;
System.out.println(canAccessOffice); // Output: false
```

## Ternary operator
Now that we are in the subject of conditional operators, lets look at one more conditional operator not related to flow contol. In Java, the Ternary operator  `?`  is a shorthand for conditional expressions. It is used solely to evaluate a condition and return a value. It is used in contexts when the returned value is 
- Not intended for flow control.
- Preferred as a non-boolean data

Syntax:
```java
condition ? value_if_true : value_if_false;
```
Example:
```java
int speed = 80;
int speedLimit = 60;
String status = (speed > speedLimit) ? "Over Speeding" : "Within Limit";
System.out.println(status); // Output: Over Speeding
```
## Independent Practice
(10 minutes)

1. Using the appropriate comparison operator, write code to verify if a stock price is expensive in comparsion to a buying threshold. 
    <details>
      <summary>Solution</summary>
      <code class="language-java">  
        double price = 150.75;
        double threshold = 100.00;
        boolean isExpensive = price > threshold;
        System.out.println(isExpensive); // Output: true
      </code>
    </details>

2. Using the appropriate comparison operator, write code to verify if a checkin luggage weight is within a maximum weight limit
    <details>
      <summary>Solution</summary>
      <code class="language-java">  
        int weight = 20;
        int maxWeight = 25;
        boolean isWithinLimit = weight <= maxWeight;
        System.out.println(isWithinLimit); // Output: true
      </code>
    </details>

3. Using the appropriate comparison operator, write code to verify if a person has got enough points to qualify for a reward
    <details>
      <summary>Solution</summary>
      <code class="language-java">  
        int points = 120;
        int requiredPoints = 100;
        boolean qualifiesForReward = points >= requiredPoints;
        System.out.println(qualifiesForReward); // Output: true
      </code>
    </details>

4. By combining appropriate logical and comparison operators, write code to verify is a person is eligible for free entry in a museum. Children below 18 years and seniors above 60 years get a free entry. Students of any educational institution, immaterial of their age, also get a free entry.
    <details>
      <summary>Solution</summary>
      <code class="language-java">  
        int age = 25;
        boolean isStudent = true;
        boolean getsFreeEntry = (age < 18 || age > 60) || isStudent;
        System.out.println(getsFreeEntry); // Output: true
      </code>
    </details>