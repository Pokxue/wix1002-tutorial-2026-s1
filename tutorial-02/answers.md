# WIX1002 Fundamentals of Programming
## Tutorial 2: Java Fundamental

### Question 1: Display the sentence "Faculty of Computer Science and Information Technology".

#### a. In one line using multiple Java statements

```java
System.out.print("Faculty of ");
System.out.print("Computer Science ");
System.out.print("and Information ");
System.out.print("Technology");
```

**Output**

```text
Faculty of Computer Science and Information Technology
```

#### b. In multiple lines using one Java statement

```java
System.out.println("Faculty of\nComputer Science\nand Information\nTechnology");
```

**Output**

```text
Faculty of
Computer Science
and Information
Technology
```

### Question 2: Write a Java statement that prints "SDN" - Software-defined networking.

```java
System.out.println("\"SDN\" - Software-defined networking");
```

### Question 3: Correct the errors in the following statements.

**a.** `System.Println("Java Programming");`

```java
System.out.println("Java Programming");
```

**b.** `System.in.println("Introduction to Java!")`

```java
System.out.println("Introduction to Java!");
```

**c.** `System.out.println("\t is the horizontal tab character");`

```java
System.out.println("\\t is the horizontal tab character");
```

**d.** `system.out.println("Java is case sensitive!" );`

```java
System.out.println("Java is case sensitive!");
```

### Question 4: Write statements for each of the following.

**a.** Declare a variable that is used to store the value of a matric number.

```java
String matricNumber;
```

**b.** Declare a variable that is used to store the value of π.

```java
double pi;
```

**c.** Initialize a variable named M with the value set to false.

```java
boolean M = false;
```

**d.** Initialize a variable named P with the value set to 8800000000.

```java
long P = 8800000000L;
```

**e.** Initialize a variable named letter with the value set to U.

```java
char letter = 'U';
```

**f.** Declare a constant variable named PRO. The value of the constant variable is Java.

```java
final String PRO = "Java";
```

### Question 5: Correct the errors for the following statements.

**a.**
```java
final double AMOUNT = "32.5";
AMOUNT += 10;
System.out.println("The amount is " + AMOUNT);
```

**Corrected statement:**
```java
double AMOUNT = 32.5;
AMOUNT += 10;
System.out.println("The amount is " + AMOUNT);
```

**b.**
```java
string chapter = 'Summary';
System.out.println(chapter);
```

**Corrected statement:**
```java
String chapter = "Summary";
System.out.println(chapter);
```

**c.**
```java
int num;
++num++;
num1 = num;
```

**Corrected statement:**
```java
int num = 0;
num++;
int num1 = num;
```

**d.**
```java
int num = 3000;
System.out.printf("%4.2f\n", num);
```

**Corrected statement:**
```java
double num = 3000;
System.out.printf("%4.2f\n", num);
```

**e.**
```java
String contact;
Scanner keyboard = new Scanner(System.out);
contact = keyboard.nextLine();
```

**Corrected statement:**
```java
String contact;
Scanner keyboard = new Scanner(System.in);
contact = keyboard.nextLine();
```

### Question 6

Write a Java program that prints the circumference of a circle. The input of the program is diameter. Display the result in three decimal places. (Note: π = `Math.PI`)

```java
import java.util.Scanner;

class Question6 {
    void main() {
        Scanner keyboard = new Scanner(System.in);

        System.out.print("Enter diameter : ");
        double diameter = keyboard.nextDouble();

        double circumference = Math.PI * diameter;

        System.out.printf("The circumference of the circle : %.3f%n", circumference);
    }
}
```

### Question 7

Write a Java program that converts inches to meters. (Given 1 inch equals 2.54 centimeters). Print the output in two decimal places.

```java
import java.util.Scanner;

class Question7 {
    void main() {
        Scanner keyboard = new Scanner(System.in);

        System.out.print("Enter value in inch : ");
        double inch = keyboard.nextDouble();

        double meters = inch * 2.54 / 100;

        System.out.printf("%.2f inches = %.2f meters%n", inch, meters);
    }
}
```