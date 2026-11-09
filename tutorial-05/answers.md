# WIX1002 Fundamentals of Programming
## Tutorial 5: Arrays

---

## 1. Write statements for each of the following:

**a. Declare an array that is used to store 12 floating-point numbers.**
```java
float[] numbers = new float[12];
```

**b. Initialize an array that is used to store the values of A to E.**
```java
char[] letters = {'A', 'B', 'C', 'D', 'E'};
```

**c. Declare an array that is used to store 100 students' names.**
```java
String[] students = new String[100];
```

**d. Declare an array for a table with 6 rows and 2 columns that is used to store integer values.**
```java
int[][] table = new int[6][2];
```

**e. Initialize an array with the following values:**
```java
int[][] array = {{6, 9}, {2, 5}, {4, 6}};
```

**f. After initializing the array, modify the values of the above array to:**
```java
array[1][1] = 4;
array[2][0] = 3;
array[2][1] = 7;
```

**g. Display all the values of an array named `contact` in separate lines.**
```java
for (int i = 0; i < contact.length; i++) {
    System.out.println(contact[i]);
}
```

---

## 2. Correct the error for the following statements.

**a.**

Original:
```java
String[] code = {'AAA', 'AAB', 'AAC', 'AAD'};
```
Corrected:
```java
String[] code = {"AAA", "AAB", "AAC", "AAD"};
```

**b.**

Original:
```java
int[] num = new num[10];
```
Corrected:
```java
int[] num = new int[10];
```

**c.**

Original:
```java
for (int k = 0; k <= num.length(); k++)
    sum += num;
```
Corrected:
```java
for (int k = 0; k < num.length; k++)
    sum += num[k];
```

**d.**

Original:
```java
int[][] t = new int[3][];
t[1][2] = 5;
```
Corrected:
```java
int[][] t = new int[3][3];
t[1][2] = 5;
```

**e.**

Original:
```java
int i = 4;
int[] score = new int[5];
score[1] = 78;
score[++i] = 100;
```
Corrected:
```java
int i = 4;
int[] score = new int[5];
score[1] = 78;
score[i++] = 100;
```

---

## 3. Determine the values of each element of array `marks`.

```java
int[] marks = new int[5];
int i = 0, j = 1;
marks[i] = 12;
marks[j] = marks[i] + 19;
marks[j-1] = marks[j] * marks[j];
marks[j*3] = marks[i+1];
marks[++j] = marks[i] % 5;
marks[2*j] = marks[j-1];
```

**Final Answer:**

| Element    | Value |
|------------|-------|
| `marks[0]` | 961   |
| `marks[1]` | 31    |
| `marks[2]` | 1     |
| `marks[3]` | 31    |
| `marks[4]` | 31    |

---

## 4. Display the number of occurrences of the word "the" (case-sensitive) in `sentence`.

```java
int count = 0;
for (int i = 0; i < sentence.length; i++) {
    if (sentence[i].equals("the")) {
        count++;
    }
}
System.out.println("Number of occurrences of \"the\": " + count);
```

---

## 5. Display `sentence` in reverse order. Each string must be reversed as well.

```java
for (int i = sentence.length - 1; i >= 0; i--) {
    String word = sentence[i];
    String reversed = "";
    for (int j = word.length() - 1; j >= 0; j--) {
        reversed += word.charAt(j);
    }
    System.out.println(reversed);
}
```

---

## 6. Generate 1 random integer within 0–255, convert to binary, store in an 8-bit array, and display it.

```java
import java.util.Random;

Random random = new Random(266);
int num = random.nextInt(256);
int[] binary = new int[8];

for (int i = 7; i >= 0; i--) {
    binary[i] = num % 2;
    num = num / 2;
}

for (int i = 0; i < 8; i++) {
    System.out.print(binary[i]);
}
```