# CS++ Java — Getting Started Guide

> Your complete guide to Git, GitHub, Java, Maven, JUnit, and GitHub Codespaces

Welcome to CS++! This guide covers everything you need to get started with the Java (AP CSA) assignments. All coding happens in the browser using GitHub Codespaces — no local installation required.

---

## Table of Contents

1. [What You Need](#what-you-need)
2. [What is Git?](#what-is-git)
3. [What is GitHub?](#what-is-github)
4. [What is GitHub Codespaces?](#what-is-github-codespaces)
5. [What is Java?](#what-is-java)
6. [What is Maven?](#what-is-maven)
7. [What is JUnit?](#what-is-junit)
8. [What is GitHub Classroom?](#what-is-github-classroom)
9. [Java Fundamentals](#java-fundamentals)
10. [Try It Yourself — Practice Examples](#try-it-yourself--practice-examples)
11. [Tips for Success](#tips-for-success)
12. [FAQ](#faq)

---

## What You Need

- A GitHub account (free at [github.com](https://github.com))
- A web browser (Chrome, Firefox, Edge, or Safari)
- The GitHub Classroom link from your teacher

That is it. No Java installation, no IDE download, no terminal setup.

---

## What is Git?

Git is a version control system that tracks changes in your code. Think of it as an unlimited undo history for your entire project.

**Key concepts:**
- **Repository (repo)** — A folder that Git tracks. Contains your code and its full history.
- **Commit** — A snapshot of your code at a specific moment. Each commit has a message describing what changed.
- **Push** — Sends your commits from Codespaces to GitHub so the autograder can see them.
- **Clone** — Creates a copy of a repository on your machine (or in Codespaces).

---

## What is GitHub?

GitHub is a website that hosts Git repositories. It adds collaboration features like pull requests, issues, and — most importantly for you — GitHub Classroom and GitHub Actions (which runs the autograder).

---

## What is GitHub Codespaces?

GitHub Codespaces is a full development environment that runs in your browser. When you open a Codespace, you get:

- A VS Code editor with syntax highlighting and autocomplete
- A terminal for running commands
- Java, Maven, and all dependencies pre-installed
- Direct connection to your GitHub repository

You do not need to install anything on your computer.

---

## What is Java?

Java is a compiled, object-oriented programming language. Every piece of code lives inside a **class**, and every program starts from a `main` method.

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**Key features:**
- **Strongly typed** — Every variable must declare its type (`int`, `double`, `String`, etc.)
- **Object-oriented** — Code is organized into classes and objects
- **Compiled** — Java code is compiled to bytecode before it runs
- **Platform independent** — Compiled Java runs on any system with a Java Virtual Machine (JVM)

---

## What is Maven?

Maven is a build tool for Java projects. It handles:

- **Compiling** your Java code
- **Running tests** automatically
- **Managing dependencies** (like JUnit)
- **Standardizing project structure** so every assignment looks the same

You do not need to configure Maven — it is already set up in every assignment. The important command is:

```bash
mvn test
```

This compiles your code and runs all the JUnit tests. You can run this in the Codespaces terminal to check your score locally before pushing.

---

## What is JUnit?

JUnit is a testing framework for Java. Your teacher writes JUnit tests that check whether your methods return the correct values. When you push your code, GitHub Actions runs these tests automatically and gives you a score.

A JUnit test looks like this:

```java
@Test
public void testAddIntegers() {
    assertEquals(5, Unit1.addIntegers(2, 3));
}
```

This test calls your `addIntegers` method with `2` and `3` and checks that it returns `5`. If it does, you get the points. If not, the test fails and tells you what went wrong.

---

## What is GitHub Classroom?

GitHub Classroom is how your teacher distributes assignments. When you click an assignment link:

1. GitHub creates a **personal copy** of the repository just for you
2. You open it in Codespaces and write your code
3. You commit and push your changes
4. GitHub Actions runs the tests and calculates your score
5. Your teacher can see your score on their dashboard

---

## Java Fundamentals

### Variables and Data Types

```java
int age = 17;                    // whole number
double gpa = 3.85;               // decimal number
boolean enrolled = true;          // true or false
String name = "Alice";            // text (note the capital S)
char grade = 'A';                 // single character
```

### Arithmetic Operators

```java
int sum = 10 + 3;        // 13
int diff = 10 - 3;       // 7
int product = 10 * 3;    // 30
int quotient = 10 / 3;   // 3 (integer division — truncates)
int remainder = 10 % 3;  // 1 (modulo)
double result = 10.0 / 3; // 3.333... (use double for decimals)
```

### Type Casting

```java
double x = 5.99;
int y = (int) x;          // y is 5 (truncates, does not round)

int a = 7;
double b = (double) a;    // b is 7.0
```

### Strings

```java
String greeting = "Hello";
int len = greeting.length();                    // 5
String upper = greeting.toUpperCase();          // "HELLO"
String sub = greeting.substring(1, 3);          // "el"
boolean has = greeting.contains("ell");         // true
String replaced = greeting.replace('l', 'r');   // "Herro"

// Concatenation
String full = "Hello" + " " + "World";         // "Hello World"

// Compare strings with .equals(), NOT ==
if (greeting.equals("Hello")) {
    System.out.println("Match!");
}
```

### Math Class

```java
Math.abs(-5)          // 5
Math.max(3, 7)        // 7
Math.min(3, 7)        // 3
Math.sqrt(16)         // 4.0
Math.pow(2, 3)        // 8.0
Math.round(4.6)       // 5 (returns long)
Math.random()         // random double between 0.0 and 1.0
```

### If-Else Statements

```java
int score = 85;

if (score >= 90) {
    System.out.println("A");
} else if (score >= 80) {
    System.out.println("B");
} else {
    System.out.println("Below B");
}
```

### Logical Operators

```java
// && (AND) — both must be true
if (age >= 16 && hasPermit) { ... }

// || (OR) — at least one must be true
if (day.equals("Saturday") || day.equals("Sunday")) { ... }

// ! (NOT) — flips true/false
if (!isRaining) { ... }
```

### Loops

```java
// For loop — when you know how many times
for (int i = 0; i < 5; i++) {
    System.out.println(i);  // prints 0, 1, 2, 3, 4
}

// While loop — when you don't know how many times
int count = 0;
while (count < 5) {
    System.out.println(count);
    count++;
}

// For-each loop — iterate over an array
int[] nums = {10, 20, 30};
for (int n : nums) {
    System.out.println(n);
}
```

### Arrays

```java
// Declare and initialize
int[] scores = {90, 85, 92, 88};
String[] names = new String[3];  // empty array of size 3

// Access and modify
scores[0] = 95;                  // change first element
int len = scores.length;         // 4 (no parentheses!)

// Traverse
for (int i = 0; i < scores.length; i++) {
    System.out.println(scores[i]);
}
```

### ArrayList

```java
import java.util.ArrayList;

ArrayList<Integer> list = new ArrayList<>();
list.add(10);              // [10]
list.add(20);              // [10, 20]
list.get(0);               // 10
list.set(0, 15);           // [15, 20]
list.remove(0);            // [20]
list.size();               // 1
```

### Classes and Objects

```java
public class Dog {
    // Instance variables
    private String name;
    private int age;

    // Constructor
    public Dog(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Getter
    public String getName() {
        return name;
    }

    // Setter
    public void setName(String name) {
        this.name = name;
    }

    // toString
    public String toString() {
        return "Dog{name='" + name + "', age=" + age + "}";
    }
}
```

### Inheritance

```java
public class Animal {
    private String name;

    public Animal(String name) {
        this.name = name;
    }

    public String makeSound() {
        return "Some sound";
    }
}

public class Dog extends Animal {
    public Dog(String name) {
        super(name);  // call parent constructor
    }

    @Override
    public String makeSound() {
        return "Bark";
    }
}
```

### Recursion

```java
public int factorial(int n) {
    if (n <= 1) return 1;         // base case
    return n * factorial(n - 1);  // recursive case
}
// factorial(5) = 5 * 4 * 3 * 2 * 1 = 120
```

---

## Try It Yourself — Practice Examples

Open any Codespace, create a file called `Practice.java`, and run it with `javac Practice.java && java Practice`.

**Example 1 — Variables and arithmetic:**
```java
// Practice.java
public class Practice {
    public static void main(String[] args) {
        int a = 10;
        int b = 3;
        System.out.println("Sum: " + (a + b));           // 13
        System.out.println("Integer division: " + a / b); // 3
        System.out.println("Remainder: " + a % b);        // 1
        System.out.println("Double division: " + (double) a / b); // 3.333...

        double price = 19.99;
        int truncated = (int) price;
        System.out.println("Truncated: " + truncated);    // 19
    }
}
```

**Example 2 — String methods:**
```java
// Practice.java
public class Practice {
    public static void main(String[] args) {
        String word = "Computer";
        System.out.println("Length: " + word.length());           // 8
        System.out.println("Upper: " + word.toUpperCase());       // COMPUTER
        System.out.println("Substring: " + word.substring(0, 4)); // Comp
        System.out.println("Contains 'put': " + word.contains("put")); // true
        System.out.println("Replace: " + word.replace('o', '0'));  // C0mputer
    }
}
```

**Example 3 — Loops and arrays:**
```java
// Practice.java
public class Practice {
    public static void main(String[] args) {
        int[] nums = {5, 12, 8, 3, 20};
        int sum = 0;
        int max = nums[0];

        for (int n : nums) {
            sum += n;
            if (n > max) max = n;
        }

        System.out.println("Sum: " + sum);       // 48
        System.out.println("Max: " + max);        // 20
        System.out.println("Average: " + (double) sum / nums.length); // 9.6
    }
}
```

**Example 4 — A simple class:**
```java
// Practice.java
public class Practice {
    private String name;
    private int score;

    public Practice(String name, int score) {
        this.name = name;
        this.score = score;
    }

    public String toString() {
        return name + ": " + score;
    }

    public static void main(String[] args) {
        Practice p1 = new Practice("Alice", 95);
        Practice p2 = new Practice("Bob", 88);
        System.out.println(p1);  // Alice: 95
        System.out.println(p2);  // Bob: 88
    }
}
```

---

## Tips for Success

1. Always use `mvn test` in the terminal to check your progress before pushing
2. Read the test output carefully — it tells you exactly what was expected vs. what your code returned
3. Commit and push often so you do not lose work
4. Every method signature must match exactly — same name, same parameter types, same return type
5. Use `.equals()` to compare Strings, not `==`
6. Integer division truncates: `7 / 2` is `3`, not `3.5`. Use `(double)` to cast if you need decimals
7. Array `.length` has no parentheses. String `.length()` has parentheses.
8. When in doubt, re-read the README for the specific assignment — it lists every method and what it should return
9. You can run `mvn test` as many times as you want — there is no limit
10. If your code does not compile, you get 0 on all tests. Fix compile errors first.

---

## FAQ

**Q: Do I need to install Java on my computer?**
No. GitHub Codespaces comes with Java and Maven pre-installed. Everything runs in your browser.

**Q: How do I open my assignment in Codespaces?**
Go to your repository on GitHub, click the green "Code" button, select the "Codespaces" tab, and click "Create codespace on main."

**Q: How do I check my score before pushing?**
Run `mvn test` in the Codespaces terminal. It shows which tests pass and fail.

**Q: How do I see my autograded score after pushing?**
Go to your repository on GitHub, click the "Actions" tab, and look at the most recent workflow run. The score appears in the autograding step.

**Q: I pushed but my score did not update. What do I do?**
Make sure you committed AND pushed. In Codespaces, click the Source Control icon, stage your changes, write a commit message, click Commit, then click Sync Changes.

**Q: My code compiles but the test says "expected 5 but was 0." What does that mean?**
Your method ran but returned the wrong value. The test expected `5` but your method returned `0`. Check your logic and make sure you are returning the correct result.

**Q: Can I modify the test files?**
No. The autograder uses the original test files from the repository. Any changes you make to tests will be ignored. Only edit the files specified in the assignment README.

**Q: What is `static`?**
A `static` method belongs to the class, not to an object. You call it with `ClassName.methodName()` instead of creating an object first. Most early assignments use static methods.

**Q: What is the difference between `int` and `Integer`?**
`int` is a primitive type. `Integer` is a wrapper class (an object). You need `Integer` when using collections like `ArrayList<Integer>` because generics require objects, not primitives.

**Q: I get "package does not exist" or "cannot find symbol." What is wrong?**
Make sure your file is in the correct directory and the `package` declaration at the top matches the folder structure. Do not move files around.

---

View all assignments and scoring breakdowns at [csplusplus.com/maven-tests](https://csplusplus.com/maven-tests)

*CS++ — AP Computer Science A — [csplusplus.com](https://csplusplus.com)*
