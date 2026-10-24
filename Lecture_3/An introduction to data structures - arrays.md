
# An introduction to data structures - arrays.



---

## A concept of a data structure

A data structure is:

- interrelationship among data elements that determine how data is recorded, manipulated, stored, and presented by a database
- any method of organizing a collection of data to allow it to be manipulated effectively (The Free On-line Dictionary of Computing, http://foldoc.org)

Data structure consists of elements and connections between these elements, where elements are simple data (e.g., integer number) and/or structured data (e.g., string)

---

## A concept of an array

An array is:

- a list of data values, all of the same type, any element of which can be referenced by an expression consisting of an array name followed by an indexing expression (Microsoft Terminology 2011. Entry from the Microsoft Language Portal)
- a fundamental data structure that supports the ability to access an element at an arbitrary position [a random access method] (G.Matisons. Datu struktūras. Lekciju konspekts. – Rīga. 2003)

The elements of an array are stored sequentially in a computer memory and each element has a specified position that is called an index

### A concept of an array

Usually, indices of array elements start with 0 and are assigned by default while declaring an array

![Array indices](https://images.openai.com/static-rsc-4/jZijzwPoYZLKbq8Q8TaYL2LVscR1xKYoH8aIGkXY6n_z943PpS6n5lfrA1ikZeSQaNUALHd_k6DlVjQI2QzGdGtF-pibXxVDySs5i68aEW_0-Y6JPGooe855Ft_K86w9iAmR4Y3p183BrGMjigL7Yyk38vIljGfQppYCSCuIqUuZMn6EHwQFvSTaGkwrpo5I?purpose=fullsize)

---

## Dimensions of an array

A dimension of an array is a number of indices, which is needed to pick an element of an array

![Dimensions of an array](https://images.openai.com/static-rsc-4/JxcavviPKSIoIgZJoOQNjfYR9EASsZU2_hZ1Wpx5aVQrvJ5zUvW8oGTtpZMxBmyRTiqzzzv-gGBn9yOTuzQrvr5wcGpS3SO_P0_GyOikri4_wOlmAfGEObEFjq7dwk0vBIHnvEPUdLkYX3hE9zGxBb_taWUM6GJYmMNStHl4MT1HJ1iN-cnaIhbdQF9nGBiN?purpose=fullsize)

---

## Basics of Arrays in Java

Syntax: `dataType[] arrayName = new dataType[size];`

```java
int m[];                //Array Declaration
m = new int[10];        //Create an Array
int a[] = new int[20];
int[] b = new int[30];  //preferred syntax form
int mas[] = {1, 2, 3, 4, 5};
```

### Basics of Arrays in Java

```java
numbers[0] = 10; // Setting the first element of the array
numbers[0] = 20; // Changing the first element to 20
int length = numbers.length; // Getting the length of the array
```

### Basics of Arrays in Java

Accessing a specific element of an array

```java
int mas[] = {1, 2, 3, 4, 5};
mas[0] = 10;
System.out.print(mas[1]);
int i = 2;
int x = mas[i];
mas[i*2] = 20;
```

### Basics of Arrays in Java

```java
class Main {
  public static void main(String[] args) {
    int mas[] = {1, 2, 3, 4, 5};
    for(int i=0; i<mas.length; i++) {
        System.out.println("index:"+ i + " and value:" + mas[i]);
    }
    System.out.println("Array length: " + mas.length);
  }
}
```

### Basics of Arrays in Java

```java
import java.util.Scanner;
class Main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    double m[] = new double[10];
    for (int i=0; i<10; i++) {
        System.out.print("m[" + i + "]=");
        m[i] = sc.nextDouble();
    }
    sc.close();
    for (int i=0; i<10; i++)
        System.out.print(m[i] + " ");
}
}
```

### Basics of Arrays in Java

```java
import java.util.Random; //Using Random Class
class Main {
    public static void main(String[] args) {
        double[] m = new double[5];
        int[] a = new int[5];
        Random r = new Random();
        for (int i=0; i<5; i++) {
            m[i] = r.nextDouble();  // [0;1)
            a[i] = r.nextInt(100);  // [0; 100)
            System.out.println("Double: " + m[i] + " and int: " + a[i]);
        }
    }
}
```

### Basics of Arrays in Java
```java
import java.util.Random;
class Main {
  public static void main(String[] args) {
    Random rand = new Random();
          int max=100,min=-50;
          System.out.println("Generated numbers are within "+min+" to "+max);
          System.out.println(rand.nextInt(max - min + 1) + min);
          System.out.println(rand.nextInt(max - min + 1) + min);
          System.out.println(rand.nextInt(max - min + 1) + min);
    }
}
```

---

## Two-dimensional arrays

Syntax: `dataType[][] arrayName = new dataType[rows][columns];`

```java
int[] m = new int[5];       //1D array
int[][] twoD = new int[3][4]; //2D array
```

![Two-dimensional arrays](https://images.openai.com/static-rsc-4/x7WB-jWgK8GlgkvzgZm6xTxJB5uV8p1hVRNXJi70iZZ4xiE7oU7Pm3MCuEAz4ydpTUDALta-kHJPpsaPhnpKPIyxtQ6EZv4geob1kP5DXp77fnjg82syP4OAM0_Z3z0ZtOKYSoxNZ1-q-_eEGkyO-xCYlfvSz7A9quHdpOScUZrgskwM2BPUQ__lLd7qDkbz?purpose=fullsize)

### Two-dimensional arrays

```java
double m1[][];
double[][] m2;       // preferred syntax form
double []m3[];
int[][] twoD = {{11, 12, 13, 14},
{21, 22, 23, 24},
{31, 32, 33, 34}};
System.out.println("Element: " + twoD[1][1]);
```

### Two-dimensional arrays

```java
class Main {
  public static void main(String[] args) {
          // declaring and initializing 2D array
        int[][] arr = { { 2, 7, 9 }, { 3, 6, 1 }, { 7, 4, 2 } };
          // printing 2D array
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++)
                System.out.print(arr[i][j] + " ");
            System.out.println();
        }
    }
}
```

---

## Arrays of Different Data Types

Arrays can store any data type:

```java
String[] names = {"Anna", "John", "Eva"};
double[] prices = {2.5, 3.6, 4.1};
boolean[] flags = {true, false, true};
```

---

## array.length

```java
public class Main {
    public static void main(String[] args) {
        int[][] numbers = {{1, 2, 3}, {4, 5, 6}};
        System.out.println("Rows: " + numbers.length); // Print number of rows
        System.out.println("Columns in first row: " + numbers[0].length);  // Print number of columns in the first row
        for (int i = 0; i < numbers.length; i++) {
            for (int j = 0; j < numbers[i].length; j++) {
                System.out.print(numbers[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

---

## Summary

- Arrays group multiple values of the same type.
- 1D arrays – lists; 2D arrays – tables.
- Use loops to process arrays.
- Use array.length to control iteration and avoid errors.
