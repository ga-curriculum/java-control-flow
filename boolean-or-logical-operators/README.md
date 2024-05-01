# ![[tktk Module Name] - tktk Microlesson Name](./assets/boolean-statements-or-logical-operations.png)

**Learning objective:** By the end of this lesson, students will be able to combine and manipulate conditionals using Boolean logic. 

## Guided Practice: Boolean or Logical Operators (15 min)

[Logical operators](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/opsummary.html) will always return a Boolean value, `true` or `false`.

There are two binary operators that require two values:
- **`AND`**, denoted `&&`.
- **`OR`**, denoted `||`.

A third unary operator requires only one value:

* **`NOT`**, denoted `!`.

#### `&&` (`AND`)

The `&&` operator requires both values to its left and right to be `true` in order to evaluate the entire statement as `true`:

```java
boolean result = false;

if (true && true) {
  result = true;
}

System.out.println(result); //=> true
```

Any other combination using the `&&` operator is `false`.

What happens if I check `true && false`?

```java
boolean result = false;

if (true && false) {
  result = true;
}

System.out.println(result); //=> false
```

```java
boolean result = false;

if (false && false) {
  result = true;
}

System.out.println(result); //=> false
```

#### `||` (`OR`)

The `||` operator requires just one of the left or right values to be `true` in order to evaluate the entire statement as `true`.

So, if I do `true || false`, what will be returned?

```java
if (true || false) {
  System.out.println("true");
}
//=> true

if (false || true) {
  System.out.println("true");
}
//=> true

if (false || false) {
    System.out.println("true");
}
//=> ... silence ...
```

> **Knowledge Check**: What is the only combination that will return `false`?

Only `false || false` will return `false`.

The `!` takes a value and returns the opposite Boolean value:

```java
!(true)
//=> false
```

The `&&` and `||` operators use short-circuit logic, which means whether or not they execute their second operand depends on the first.

> **Knowledge Check**: Can you think of a time when this might be useful?

This is useful for checking for `null` objects before accessing their attributes:

```java
if (instructor != null && instructor.getName().equals("drew")) {
  System.out.println("davis");
}
```

In this case, if the first operand, `instructor != null`, is `false`, then the second operand, `instructor.getName().equals("drew")`, will not be evaluated. The expression is basically saying, "We already know the whole `&&` expression is `false` because `instructor != null` is `false`. Why bother dealing with the second operand?"

This is also important because a `NullPointerException` will be thrown if we try to call a method using "dot notation" on a `null` object reference.

_Written by Kristen Tonga_
