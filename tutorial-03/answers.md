# WIX1002 Fundamentals of Programming
## Tutorial 3: Flow of Control (Selection)

### Question 1: Write statements for each of the following.

#### a. Determine whether 3 × 8 = 27.

```java
System.out.println(3 * 8 == 27);
```

#### b. Determine whether an input integer is an odd number or even number.

```java
if (number % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
```

#### c. Determine whether a character is a capital letter.

```java
if (ch >= 'A' && ch <= 'Z') {
    System.out.println("Capital letter");
} else {
    System.out.println("Not a capital letter");
}
```

#### d. Display two strings in alphabetical order, ignoring their case.

```java
if (str1.compareToIgnoreCase(str2) <= 0) {
    System.out.println(str1);
    System.out.println(str2);
} else {
    System.out.println(str2);
    System.out.println(str1);
}
```

#### e. A switch statement that displays Sunday, Monday, ..., Saturday if the input is 0, 1, ..., 6.

```java
switch (day) {
    case 0 -> System.out.println("Sunday");
    case 1 -> System.out.println("Monday");
    case 2 -> System.out.println("Tuesday");
    case 3 -> System.out.println("Wednesday");
    case 4 -> System.out.println("Thursday");
    case 5 -> System.out.println("Friday");
    case 6 -> System.out.println("Saturday");
    default -> System.out.println("Invalid input");
}
```

### Question 2: Correct the error for the following statements.

#### (a)

**Question:**

```java
if (num1 = num2)
    System.out.println("Number 1 is equal to number 2.");
```

**Corrected statement:**

```java
if (num1 == num2)
    System.out.println("Number 1 is equal to number 2.");
```

#### (b)

**Question:**

```java
if (x > y > z)
    System.out.println("x is the largest number");
```

**Corrected statement:**

```java
if (x > y && x > z)
    System.out.println("x is the largest number");
```

#### (c)

**Question:**

```java
String s1, s2;

if (s1 == s2)
    System.out.println("They are equal strings.");
else (s1 != s2)
    System.out.println("They are not equal strings.");
```

**Corrected statement:**

```java
if (s1.equals(s2))
    System.out.println("They are equal strings.");
else
    System.out.println("They are not equal strings.");
```

#### (d)

**Question:**

```java
if x > 0 or y > 0;
    System.out.println("Either x or y is positive");
```

**Corrected statement:**

```java
if (x > 0 || y > 0)
    System.out.println("Either x or y is positive");
```

### Question 3: Write the output for the following statements when x = 9 and y = 10.

#### (a)

**Question:**

```java
if (x < 10)
    if (y > 10)
        System.out.println("*****");
    else
        System.out.println("#####");
System.out.println("$$$$$");
```

**Output:**

```text
#####
$$$$$
```

#### (b)

**Question:**

```java
if (x < 10) {
    if (y < 10)
        System.out.println("*****");
    else {
        System.out.println("#####");
        System.out.println("$$$$$");
    }
}
```

**Output:**

```text
#####
$$$$$
```

#### (c)

**Question:**

```java
if (x < 10) {
    if (y < 10)
        System.out.println("*****");
    System.out.println("#####");
} else {
    System.out.println("$$$$$");
}
```

**Output:**

```text
#####
```

#### (d)

**Question:**

```java
if (x > 10) {
    if (y > 10) {
        System.out.println("*****");
        System.out.println("#####");
    } else
        System.out.println("$$$$$");
}
```

**Output:**

```text
```


### Question 4: Write the Java statements that use the if statement to find the biggest number among three given integers.

```java
if (num1 >= num2 && num1 >= num3) {
    System.out.println("The biggest number is " + num1);
} else if (num2 >= num1 && num2 >= num3) {
    System.out.println("The biggest number is " + num2);
} else {
    System.out.println("The biggest number is " + num3);
}
```


### Question 5: Write the Java statements that determine whether a year is a leap year. A leap year is divisible by 4 but not by 100. However, a leap year is also divisible by 400.

**Java statements:**

```java
if (year % 400 == 0 || (year % 4 == 0 && year % 100 != 0)) {
    System.out.println("Leap year");
} else {
    System.out.println("Not a leap year");
}
```