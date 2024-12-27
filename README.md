# README

## 1. Java Architecture

Java architecture follows the Write Once, Run Anywhere philosophy. Java programs are compiled into bytecode, which can run on any platform that has a Java Virtual Machine (JVM).

- JVM (Java Virtual Machine): It runs the Java bytecode on different platforms.
- JRE (Java Runtime Environment): It provides libraries and JVM to run Java programs.
- JDK (Java Development Kit): It includes the JRE and development tools (like the Java compiler).

## 2. Java Buzzwords

Java has a set of characteristics often referred to as buzzwords. Here are a few:
- Simple: Java's syntax is simple, and it eliminates complexities like memory management.
- Object-Oriented: Everything in Java is an object (except for primitive types).
- Platform-Independent: Bytecode runs on any system with a JVM.
- Multithreaded: Java supports multiple threads of execution.
- Secure: Java provides a secure environment for applications, especially for network-based programs.
- Portable: Java applications are portable and can run on any device that has a JVM.

## 3. Classpath

The Classpath is a parameter that tells the Java compiler and JVM where to find the compiled classes and libraries. When you run or compile a Java program, the JVM looks in the classpath to find the required classes.

- Setting the classpath: You can set the classpath manually using the `-cp` flag when running Java programs, or set the environment variable `CLASSPATH` in your system.

Example of running a program with a specified classpath:

```bash
java -cp /path/to/classes MyProgram
```

## 4. Structure of a Java Program

A basic Java program has the following structure:

```java
public class HelloWorld {
    public static void main(String[] args) {
        // Print "Hello, World!" to the console
        System.out.println("Hello, World!");
    }
}
```

- Class Declaration: The program starts with `public class HelloWorld`, where `HelloWorld` is the class name.
- main Method: The `main` method is the entry point. It is where execution begins.
- Statements: Inside the `main` method, we print "Hello, World!" using `System.out.println`.

## 5. Compiling and Running Java Programs

### Compiling:
To compile the Java program, we use the `javac` command:
```bash
javac HelloWorld.java
```
This generates a `HelloWorld.class` file, which contains the bytecode.

### Running:
To run the program, we use the `java` command:
```bash
java HelloWorld
```
This will execute the bytecode and print the output to the console.

## Example Code: Basic Java Program

```java
// HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        // Print message to the console
        System.out.println("Hello, World!"); 
    }
}
```

## Key Points:
- Java program structure: Class + `main` method + statements.
- Compilation: `javac HelloWorld.java` compiles the code.
- Execution: `java HelloWorld` runs the compiled bytecode.

## 6. Classes and Objects:
- Definition of a Class and an Object: A class is a template for creating objects, and an object is an instance of a class. The class defines properties (fields) and behaviors (methods), and the object holds actual data.
- Creating Objects: Learn how to instantiate objects from a class and use them to access fields and methods.
- Constructors: Understand how constructors are used to initialize objects when they are created, with both default and parameterized constructors.
  
Example Code:

```java
class Car {
    String model;
    String color;

    // Constructor
    Car(String model, String color) {
        this.model = model;
        this.color = color;
    }

    // Method
    void displayDetails() {
        System.out.println("Model: " + model);
        System.out.println("Color: " + color);
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating an object using constructor
        Car car1 = new Car("Toyota", "Red");
        car1.displayDetails();  // Output: Model: Toyota, Color: Red
    }
}
```

---

## 7. Inheritance:
- Definition: Inheritance is a mechanism where a new class (subclass) can inherit fields and methods from an existing class (superclass). This allows for code reuse and extension.
- Constructor Inheritance: Constructors are not inherited, but the subclass can call the parent class constructor using `super()`.
- Method Overriding: Subclasses can override methods from the parent class to provide specific behavior for the subclass.

Example Code:

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.sound();  // Output: Dog barks
    }
}
```

---

## 8. Method Overloading:
- Definition: Method overloading occurs when a class has multiple methods with the same name but different parameter types or numbers of parameters.
- Purpose: It allows you to use the same method name for different operations, reducing code duplication.

Example Code:

```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        System.out.println(calc.add(5, 3));  // Output: 8
        System.out.println(calc.add(5, 3, 2));  // Output: 10
    }
}
```

---

## 9. Access Modifiers:
- Public: The member can be accessed from anywhere in the program.
- Private: The member is accessible only within the same class.
- Protected: The member can be accessed within the same package and by subclasses.
- Default (no modifier): The member is accessible only within the same package.

Example Code:

```java
class Person {
    public String name;  // Accessible from anywhere
    private int age;     // Only accessible within the same class

    // Public method to access private field
    public int getAge() {
        return age;
    }

    // Public method to set private field
    public void setAge(int age) {
        if(age > 0) {
            this.age = age;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Person p = new Person();
        p.name = "John";  // Accessible because 'name' is public
        p.setAge(25);  // Set age using public method
        System.out.println("Name: " + p.name);
        System.out.println("Age: " + p.getAge());  // Accessible through public method
    }
}
```

---

## Key Points:
1. Classes and Objects: Learn how to define and create objects from classes and use constructors to initialize them.
2. Inheritance: Understand how inheritance promotes code reuse and how to override methods in subclasses.
3. Method Overloading: Master how to define multiple methods with the same name but different parameters.
4. Access Modifiers: Familiarize yourself with the different access levels (`public`, `private`, `protected`, and default) to control visibility.

Would you like to focus on any of these concepts with additional details or examples? Let me know!