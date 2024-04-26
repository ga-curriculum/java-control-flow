# ![[tktk Module Name] - tktk Microlesson Name](./assets/hero.png)

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

##### A Special Note on Equality Among `String`s

There are two ways to compare the equality of `String`s:

```java
String blue = "blue";
boolean withSign = (blue == "blue");            //=> true
boolean withWords = (blue).equals("blue");      //=> true
```

Do you know which one of these would be preferred?

Let's do another example to show you which and why:

```java
String blue = "blue";
String bl = "bl";
String ue = "ue";

System.out.println(bl+ue);                      //=> blue
boolean withSigns = (bl+ue == blue);            //=> false
boolean withWords = (bl+ue).equals(blue);       //=> true
```

Why isn't `withSigns` `true` when the output looks the same?

Objects and arrays are complex collections of values, and when we refer to them, we're actually referencing where they live in memory. That's why we say objects are **passed by reference**, while `int` and `float` are **passed by value**.

`==` compares the place where the object was stored on the computer. What this means is that Java doesn't care if they look similar; it only compares whether or not they're the exact same object in memory. When checking for equality in each of the cases above, we're actually comparing two objects that are in two different places in memory.

`String blue` has a reference to where it's stored on the computer, and that's a different place than where `String bl` is stored. They're not exactly the same, according to `==`.

`equals()`, on the other hand, can be called on an instance of a `String` object. This method checks if the `char` arrays in each `String` are the same, not if the references are the same.

In short, use `equals()` when comparing `String`s.

> **Knowledge Check**: Why can we call methods on a variable of a `String` data type but not on an `int`?

#### Don't Forget About Me: `!=`

There's also an `!=` operator, which is the inverse of `==`.

_Written by Kristen Tonga_