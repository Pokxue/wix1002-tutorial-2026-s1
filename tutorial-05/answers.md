# WIX1002 Fundamentals of Programming
## Tutorial 5: Arrays

### 1. Write statements for each of the following:

**a. Declare an array that is used to store 12 floating-point numbers.**
float numbers[12];

**b. Initialize an array that is used to store the values of A to E.**
char letters[5] = {'A', 'B', 'C', 'D', 'E'};

**c. Declare an array that is used to store 100 students' names.**
string students[100];

**d. Declare an array for a table with 6 rows and 2 columns that is used to store integer values.**
int table[6][2];

**e. Initialize an array with the following values:**
int array[3][2] = {{6,9}, {2,5}, {4,6}}

**f. After initializing the array, modify the values of the above array to:**
array[1][1] = 4;
array[2][0] = 3;
array[2][1] = 7;

**g. Display all the values of an array named `contact` in separate lines.**
for (int i = 0; i < contact.length; i++)
 {
    System.out.println(contact[i]);
 }


### 2. Correct the error for the following statements.
**a.**
Original:
String[] code = {'AAA', 'AAB', 'AAC', 'AAD'};

Corrected:
String[] code = {"AAA", "AAB", "AAC", "AAD"};

**b.**
Original:
int[] num = new num[10];

Corrected:
int[] num = new int[10];


**c.**
Original:
for(int k=0; k<=num.length(); k++)
    sum+=num;

Corrected:
for(int k=0; k<num.length; k++)
    sum+=num[k];

**d.**
Original:
int [][]t = new int[3][];
t[1][2] = 5;

Corrected:
int[][] t = new int[3][3];
t[1][2] = 5;

**e.**
Original:
int i=4;
int []score = new int[5];
score[1] = 78;
score[++i] = 100;

Corrected:
int i = 4;
int[] score = new int[5];
score[1] = 78;
score[i++] = 100;

### 3. Determine the values of each element of array marks. Assume the array was declared as:

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

marks[0] = 961;
marks[1] = 31;
marks[2] = 1;
marks[3] = 31;
marks[4] = 31;

### 4. Write the statements that display the number of occurrences of the word "the" (case-sensitive) in a string array named `sentence`.

**Answer:**
int count = 0;
for (int i = 0; i < sentence.length; i++)
 {
    if (sentence[i].equals("the")) 
    {
        count++;
    }
}
System.out.println("Number of occurrences of \"the\": " + count);


### 5. Write the statements that display the string array named `sentence` in reverse order. Each string element must be displayed in reverse order as well.

**Answer:**
for (int i = sentence.length - 1; i >= 0; i--) {
    String word = sentence[i];
    String reversed = "";
    for (int j = word.length() - 1; j >= 0; j--) {
        reversed += word.charAt(j);
    }
    System.out.println(reversed);
}

### 6. Write the statements that generate 1 random integer within 0–255. Convert the number to binary and store the bits into an 8-bit array. Then, display the binary number.

**Answer:**
Random random = new Random(266);
int num = random.nextInt(256);
int[] binary = new int[8];

for (int i = 7; i >= 0; i--)
{
    binary[i] = num % 2;
    num = num / 2;
}

for (int i = 0; i < 8; i++)
{
    System.out.print(binary[i]);
}