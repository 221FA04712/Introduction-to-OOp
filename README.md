# Introduction-to-OOp

# About Java

Java is one of the most popular and influential programming languages in the world, known for its platform independence, simplicity, and strong support for Object-Oriented Programming (OOP). Introduced by Sun Microsystems in 1995, Java was designed from the ground up with OOP in mind, making it a powerful tool for building real-world applications.

What sets Java apart from many other languages is its **“write once, run anywhere”** capability. Thanks to the Java Virtual Machine (JVM), Java code can run on any device or operating system that has a compatible JVM — without needing to be rewritten or recompiled.

Java’s object-oriented nature is deeply embedded into its design. Unlike some other languages that added OOP features later, Java embraces OOP as its core philosophy. This makes it more intuitive when building complex software systems using concepts like classes, objects, and methods.

## What Makes Java Unique and Special

- **Platform Independence:** Java code is compiled into bytecode, which runs on the JVM, allowing it to be executed across different platforms without modification.

- **Robust and Secure:** Java emphasizes strong memory management, exception handling, and security features, making it a reliable choice for enterprise-level development.

- **Pure OOP Approach:** Java promotes a strict object-oriented model, where everything (except primitives) revolves around objects and classes.

- **Rich Standard Library:** Java provides a vast and well-organized set of libraries (Java API) that makes development faster and more efficient.

- **Automatic Memory Management:** With built-in garbage collection, Java manages memory automatically, reducing the chances of memory leaks and other issues.



#  Programming Paradigms: Procedural vs Object-Oriented Programming in Java

##  Overview

Procedural Programming (PP) is function-based and follows a linear top-down approach. Object-Oriented Programming (OOP) models real-world entities using objects, emphasizing encapsulation, inheritance, and polymorphism.

---


##  Key Differences

| Feature              | Procedural Programming                           | Object-Oriented Programming (OOP)           |
|----------------------|---------------------------------------------------|---------------------------------------------|
| Structure            | Code organized into functions                    | Code organized into classes and objects     |
| Data Handling        | Data is passed manually to functions             | Data is encapsulated within objects         |
| Behavior Definition  | Functions define behavior externally             | Behavior defined within objects (methods)   |
| Reusability          | Limited due to tight coupling                    | High through inheritance and polymorphism   |
| Polymorphism         | Not supported                                    | Supported via method overriding             |
| Encapsulation        | Not inherent                                     | Core principle: hides internal state        |
| Extendability        | Requires modifying existing code                 | Easily extendable via new subclasses        |
| Java Example Style   | Uses static methods and data structures          | Uses class hierarchy and overridden methods |

---






















# Java Identifiers

An **identifier** can be a method name, class name, variable name, or label in Java.

### Example: Code1:: IdentifierExample.java

In this code, there are 5 identifiers:

| Identifier         | Type             |
|-------------------|------------------|
| `IdentifierExample`| Class Name       |
| `main`             | Method Name      |
| `String`           | Predefined Class Name |
| `args`             | Variable Name    |
| `a`                | Variable Name    |

These identifiers follow Java’s rules for naming conventions and represent different elements in the code.

You can see the full example code [here](./IdentifierExample.java).


# Java Identifiers — Interview Questions

Here are some key interview questions and answers covering the important concepts of Java identifiers:

---

### 1. What is an identifier in Java, and what rules must it follow when naming?

**Answer:**  
An **identifier** is the name used to identify variables, methods, classes, labels, or other user-defined elements in Java code. It serves as a unique name for these entities.

**Rules for naming identifiers:**  
- Must start with a letter (`A-Z` or `a-z`), a dollar sign (`$`), or an underscore (`_`). It **cannot start with a digit**.  
- Subsequent characters can be letters, digits (`0-9`), dollar signs, or underscores.  
- Cannot be the same as any **Java reserved keyword** (e.g., `class`, `if`, `while`).  
- Java identifiers are **case-sensitive** (`myVar` and `myvar` are different).  
- No spaces or special characters (like `@`, `#`, `!`) are allowed.  
- There is no strict limit on length, but excessively long names are discouraged for readability.

---

### 2. Can Java identifiers include special characters or Unicode letters? Which characters are allowed or disallowed?

**Answer:**  
Java identifiers can include:  
- Letters (`A-Z`, `a-z`)  
- Digits (`0-9`) **after** the first character  
- The underscore (`_`)  
- The dollar sign (`$`)  
- Unicode letters and digits from other languages, as Java supports Unicode, so identifiers can use letters from many alphabets.

**Disallowed characters include:**  
- Spaces  
- Special symbols like `@`, `#`, `%`, `&`, `*`, `!`, etc.  
- Starting an identifier with a digit is disallowed.

Using `$` is technically allowed but generally reserved for compiler-generated code, so it’s best avoided in normal coding.

---

### 3. Are Java keywords allowed as identifiers? What happens if you try to use them?

**Answer:**  
No, **Java keywords cannot be used as identifiers**. Keywords are reserved words that have special meaning in the language syntax, such as `class`, `int`, `public`, `if`, and `while`.

If you try to use a keyword as an identifier, the compiler will throw a **syntax error**, and your program will not compile. For example, writing `int class = 5;` will cause a compilation error because `class` is a reserved keyword.




##  Java Reserved Words

Java has a total of **53 reserved words**:

- **50 Keywords**: Reserved for language syntax and structure.
- **3 Reserved Literals**: Used as fixed constant values (`true`, `false`, `null`).

---

###  List of 50 Java Keywords
abstract assert boolean break byte
case catch char class const*
continue default do double else
enum extends final finally float
for goto* if implements import
instanceof int interface long native
new package private protected public
return short static strictfp super
switch synchronized this throw throws
transient try void volatile while




---

##   Java Interview Question(Keyword-Focused)

###  Q1: What is the difference between `final`, `finally`, and `finalize()` in Java?

**Answer:**

- **`final`**: A **keyword** used to restrict:
  - A **variable**: cannot be reassigned.
  - A **method**: cannot be overridden.
  - A **class**: cannot be extended.

- **`finally`**: A **block** that is always executed after try-catch, regardless of exceptions.

- **`finalize()`**: A **method** called by the garbage collector before destroying an object. *(Deprecated in Java 9+)*



#  Java Classes Overview

##  What is a Class?

A **class** in Java is a blueprint or prototype from which individual **objects** are created. It encapsulates **state** (fields/attributes) and **behavior** (methods/functions) that are common to all instances of that type.

---

##  Components of a Class Declaration

A class declaration in Java generally follows this structure:

```java
[modifiers] class ClassName [extends SuperClass] [implements Interface1, Interface2, ...] {
    // fields
    // constructors
    // methods
}
```

Here’s a breakdown/OverView of each component:

###  Modifiers
- Specify access level and properties of the class.
- Common modifiers:
  - `public`: accessible from anywhere.
  - *(default)*: accessible only within the same package.
  - `abstract`: class cannot be instantiated directly.
  - `final`: class cannot be extended.

###  Class Name
- Must start with an uppercase letter (by convention).
- Should be a noun that describes the object (e.g., `Student`, `Car`, `BankAccount`).

###  Superclass (if any)
- A class can **extend** another class using the `extends` keyword.
- Java supports **single inheritance** (only one superclass).
```java
public class Dog extends Animal {
    // inherits fields and methods from Animal
}
```

###  Interfaces (if any)
- A class can **implement** one or more interfaces using the `implements` keyword.
- This allows Java to support **multiple inheritance** of type via interfaces.
```java
public class Car implements Vehicle, Engine {
    // must override all abstract methods from interfaces
}
```

###  Class Body
- Enclosed in `{}` braces.
- Contains:
  - **Fields** (variables)
  - **Constructors**
  - **Methods**
  - **Inner classes or interfaces** (optional)

---



##  Summary 

| Component     | Description |
|---------------|-------------|
| Modifiers     | Controls access (`public`, `final`, `abstract`, etc.) |
| Class Name    | Conventionally starts with a capital letter |
| Superclass    | Single inheritance via `extends` |
| Interfaces    | Multiple inheritance of type via `implements` |
| Body          | Contains fields, methods, constructors, etc. |

A class in Java is the foundation for object-oriented programming. It enables **encapsulation**, **inheritance**, and **polymorphism**, making code modular, reusable, and easy to maintain.

---

