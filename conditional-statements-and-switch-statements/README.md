# ![[tktk Module Name] - tktk Microlesson Name](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to: 
- Examine how the `if...else` conditionals control program flow based on Boolean conditions. 
- Examine how the `switch` conditional control program flow based on explicit conditions. 

## Demo: Conditional Statements (10 min)

Conditional statements are a way of skipping over a block of code if it doesn't pass a Boolean expression. Java supports two conditional statements: `if...else` and `switch`.

#### `if...else` Statements

```java
if (expr) {
    code
} else {
    other code
}
```

This means run the `code` block if `expr` is `true`, otherwise (if `expr` is `false`), run the `other code` block:

```java
int i = 9;

if (i > 0) {
    System.out.println("hi");
} else {
    System.out.println("goodbye");
}
//=> hi
```

When you need to test more than one case, you may use `else...if`:

```java
String name = "kittens";

if (name.equals("puppies")) {
    name += "!!!";
} else if (name.equals("kittens")) {
    name += "!!";
} else {
    name = "!" + name;
}

System.out.println(name); //=> "kittens!!"
```

#### Ternary Operator

Java has a ternary operator for conditional expressions. You can think of the ternary operator as a concise `if...else` in one line:

```java
int age = 12;

String allowed = (age > 18) ? "yes" : "no";

System.out.println(allowed); //=> "no"
```

#### `true` or `false`

It's important to know that all of the following become `false` when converted to a `Boolean`:

- `false`
- `0`
- `""` (empty string)
- `NaN`
- `null`
- `undefined`

For example:

```java
Boolean b = Boolean.valueOf("");

System.out.println(b); //=> false
```

This can be helpful when checking if conditions exist or are undefined, or if variables don't hold value.

---

## Introduction: `switch` Statements (10 min)

The `switch` statement can be used for multiple branches based on a number or `String`:

```java
  String food = "apple";

  switch(food) {
    case "pear":
      System.out.println("I like pears");
      break;
    case "apple":
      System.out.println("I like apples");
      break;
    default:
      System.out.println("No favorite");
  }
//=> I like apples
```

In this case, the `switch` statement compares `food` to each of the cases (`pear` and `apple`) and evaluates the expressions beneath them if there's a match. It uses the `String.equals` method in this case, or `==` in the case of primitives, to evaluate equality.

The default clause is optional.

**Note: Breaks are important.** If you don't put a `break` statement, the expression will continue to be evaluated for the next cases. This might cause unintended consequences.

For example, if you eliminate the `break` statements:

```java
  String food = "apple";

  switch(food) {
    case "pear":
      System.out.println("I like pears");
    case "apple":
      System.out.println("I like apples");
    default:
      System.out.println("No favorite");
  }
```

The result would be:

```
I like apples 
No favorite
```

If `food = "pear"`, then the output would be:

```
I like pears  
I like apples 
No favorite
```

This isn't what we intended.

_Written by Kristen Tonga_