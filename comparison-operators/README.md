# ![[tktk Module Name] - tktk Microlesson Name](./assets/comparison-operators.png)

**Learning objective:** By the end of this lesson, students will be able to examine comparison operators to evaluate and compare statements. 

## Demo: Comparison Operators (10 min)

[Comparisons](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op2.html) in Java can be made on primitives using `<`, `>`, `<=`, and `>=`.

> **Knowledge Check**: What is a primitive data type?

```java
'A' > 'a'
//=> false

'b' > 'a'
//=> true

12 > 12
//=> false

```

Note that you **cannot** do:

```java
12 >= "12"

// or

"Apple" > "Oranges"
```

#### Equality Operator `==`

When verifying equality between primitives, use `==`:

```java
System.out.println(1 == 2);
//=> false
```

But what about with objects like `String`s?