
# If.. else, loops, user input


## 1. IF.. ELSE

In Java, an if-else statement is used to make decisions in a program.

It allows the program to choose between different actions depending on whether a condition is true or false.

### Syntax

```java
if (condition) {
    // code to run if condition is true
} else {
    // code to run if condition is false
}
```

### Condition

A boolean expression (something that results in true or false).

Example: `x > 5`, `age == 18`, `isStudent`.

**if block `{ }`:**

Runs only when the condition is true.

**else block `{ }`:**

Runs only when the condition is false.

### Important Notes

- Conditions must return true or false.
- Use comparison operators (`==`, `!=`, `<`, `>`, `<=`, `>=`).
- Use logical operators (`&&`, `||`, `!`) to combine conditions.
- Curly braces `{ }` group the statements that belong to if or else.

### Example

```java
public class Main {
    public static void main(String[] args) {
        int age = 20;

        if (age >= 18) {
            System.out.println("You are an adult.");
        } else {
            System.out.println("You are a minor.");
        }
    }
}
```

---

## 2. IF.. ELSE IF Chain

```java
public class Main {
    public static void main(String[] args) {
        int score = 75;

        if (score >= 90) {
            System.out.println("Grade: A");
        } else if (score >= 75) {
            System.out.println("Grade: B");
        } else if (score >= 60) {
            System.out.println("Grade: C");
        } else {
            System.out.println("Grade: F");
        }
    }
}
```

---

## 3. Nested IF.. ELSE

```java
int number = 15;

if (number > 0) {
    if (number % 2 == 0) {
        System.out.println("The number is positive and even.");
    } else {
        System.out.println("The number is positive and odd.");
    }
} else {
    System.out.println("The number is not positive.");
}
```

---

## 4. WHILE Loop

A loop is used to repeat a block of code multiple times.

The while loop keeps running as long as a condition is true.

It is called an **entry-controlled loop** because the condition is checked before the loop body executes.

### Syntax

```java
while (condition) {
    // code to be repeated
}
```

### Important Notes

- Condition must return true or false.
- If the condition is true, the block executes.
- After execution, the condition is checked again.
- If the condition becomes false, the loop stops.

### Example 1

```java
public class Main {
    public static void main(String[] args) {
        int i = 1;

        while (i <= 5) {
            System.out.println("Number: " + i);
            i++;
        }
    }
}
```

### Example 2

```java
public class Main {
    public static void main(String[] args) {
        int a = 1;

        while (true) {  //infinite loop
            System.out.println("This will run forever! " + a);
            a++;
        }
    }
}
```

---

## 5. DO.. WHILE Loop

Similar to the while loop, but with one key difference:

In a do-while loop, the code block runs **at least once**, even if the condition is false.

It is called an **exit-controlled loop** because the condition is checked after the loop body executes.

### Syntax

```java
do {
    // code to be executed
} while (condition);
```

### Example

```java
public class Main {
    public static void main(String[] args) {
        int i = 1;

        do {
            System.out.println("Number: " + i);
            i++;
        } while (i <= 5);
    }
}
```

---

## 6. FOR Loop

A for loop is used to repeat a block of code a known number of times.

It is best when you know how many times you want to run the loop.

It combines three parts in one line:

- Initialization
- Condition
- Update/Increment

### Syntax

```java
for (initialization; condition; update) {
    // code to repeat
}
```

### Important Notes

- **Initialization** → runs once at the start (e.g. `int i = 0`)
- **Condition** → checked before every iteration; must be true or false
- **Update** → runs after each loop iteration (e.g. `i++`)

### Example

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Number: " + i);
        }
    }
}
```

---

## 7. Infinite FOR Loop

```java
public class Main {
    public static void main(String[] args) {
        for ( ; ; ) {
            System.out.println("Runs forever!");
        }
    }
}
```

---

## 8. BREAK in Java

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) {
            if (i == 5) {
                break;  // stop the loop when i = 5
            }
            System.out.println("i = " + i);
        }
    }
}
```

---

## 9. CONTINUE in Java

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            if (i == 3) {
                continue; // skip printing when i = 3
            }
            System.out.println("i = " + i);
        }
    }
}
```

### BREAK and CONTINUE

Use **break** when you need to stop a loop early.

Use **continue** when you want to skip one iteration, but keep looping.

Both make loops more flexible and help control program flow.

---

## 10. User INPUT

Input means data that the user types in while the program is running.

Example: typing your name, age, or a number to calculate something.

In Java, we use classes from the standard library to read input.

Java provides the **Scanner class** (in `java.util` package) to read input from the keyboard.

### 1. Import the class

```java
import java.util.Scanner;
```

### 2. Create a Scanner object

```java
Scanner input = new Scanner(System.in);
```

### 3. Read data

- `nextInt()` → for integers
- `nextDouble()` → for decimal numbers
- `nextLine()` → for a whole line of text
- `next()` → for a single word

### Example 1 - Read Integer

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter your age: ");
        int age = input.nextInt();   // read integer

        System.out.println("You are " + age + " years old.");
    }
}
```

### Example 2 - Read String

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = input.nextLine();   // read string

        System.out.println("Hello, " + name + "!");
    }
}
```

### Important Notes

- Scanner can read numbers, text, and booleans.
- Use `next()` for single words, `nextLine()` for full sentences.
- Always handle newline issues when mixing `nextInt()` and `nextLine()`.
- Don't forget to close the scanner with `sc.close()`.

### Example 3

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter age: ");
        int age = sc.nextInt();   // user enters: 20 + Enter

        System.out.print("Enter name: ");
        String name = sc.nextLine();  // OOPS! takes leftover '\n'

        System.out.println("Age: " + age + ", Name: " + name);
    }
}
```


