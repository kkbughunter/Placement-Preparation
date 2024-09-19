## 2 Object-Oriented Programming
  - **Object** Object Creation, Object Lifetime, Object Reference
  - **Class** Class Declaration, Constructors & Destructors, Static Members, Nested Classes
  - **Abstraction** Abstract Classes, Interfaces, Abstract Methods
  - **Inheritance** Single & Multiple Inheritance, Multilevel Inheritance, Hybrid Inheritance, Virtual Inheritance
  - **Polymorphism** Compile-Time Polymorphism (Overloading), Run-Time Polymorphism (Overriding)
  - **Encapsulation** Private Members, Getters/Setters, Access Modifiers
  - **Dynamic Binding** Late Binding, Method Overriding, Virtual Functions, Abstract Methods
  - **Message Passing** Method Invocation, Parameter Passing (by Value/Reference)
  - **Garbage Collection** Automatic Memory Management, Finalize Method, Reference Counting
  - **Generic Types, Methods, Collections** Template Classes & Functions (C++), Generics (Java), Parametrized Collections (List<T>, Map<K, V>)

  Here’s a brief definition, example, and a small sample code for each **Object-Oriented Programming** concept:

---

### 2. Object-Oriented Programming

#### 1. **Object**
   - **Definition:** An object is an instance of a class that holds data and methods.
        - run time entities
        - Each object is an instance of a class
   - **Example:** In a `Car` class, an object could represent a specific car.
   - **Code Example (Java):**
     ```java
     class Car {
         String brand;
         int year;
     }
     public class Main {
         public static void main(String[] args) {
             Car myCar = new Car(); // Object creation
             myCar.brand = "Toyota";
             myCar.year = 2020;
         }
     }
     ```

#### 2. **Class**
   - **Definition:** A class is a blueprint for creating objects with attributes and methods.
        - User-definde data type
        - Object are variable type of class
   - **Example:** The `Car` class can define the attributes of a car like brand and year.
   - **Code Example (Java):**
     ```java
     class Car {
         String brand;
         int year;

         Car(String b, int y) { // Constructor
             this.brand = b;
             this.year = y;
         }
     }
     ```

#### 3. **Abstraction**
   - **Definition:** Abstraction hides the complex implementation details and shows only the essential features.
   - **Example:** Abstracting a `Vehicle` class to define common methods like `start()` without implementing them.
   - **Code Example (Java):**
     ```java
     abstract class Vehicle {
         abstract void start();
     }
     class Car extends Vehicle {
         void start() {
             System.out.println("Car is starting");
         }
     }
     ```

#### 4. **Inheritance**
   - **Definition:** Inheritance allows a class to inherit properties and methods from another class.
   - **Example:** A `Car` class can inherit from a `Vehicle` class.
   - **Code Example (Java):**
     ```java
     class Vehicle {
         void move() {
             System.out.println("Vehicle is moving");
         }
     }
     class Car extends Vehicle { }
     ```

#### 5. **Polymorphism**
   - **Definition:** Polymorphism allows methods to take many forms, either through overloading or overriding.
   - **Example:** Method `start()` can behave differently in `Car` and `Bike` classes.
   - **Code Example (Java - Overriding):**
     ```java
     class Vehicle {
         void start() {
             System.out.println("Vehicle is starting");
         }
     }
     class Car extends Vehicle {
         @Override
         void start() {
             System.out.println("Car is starting");
         }
     }
     ```

#### 6. **Encapsulation**
   - **Definition:** Wrapping up of data and dunctions into a single unit is known as Encapsulation.
        - restricts access to certain data by using access modifiers (private, public).
   - **Example:** Use private members and expose them through getters and setters.
   - **Code Example (Java):**
     ```java
     class Car {
         private String brand;
         public void setBrand(String b) {
             this.brand = b;
         }
         public String getBrand() {
             return brand;
         }
     }
     ```

#### 7. **Dynamic Binding**
   - **Definition:** Dynamic binding refers to runtime method binding, where the method that is called is determined at runtime.
   - **Example:** Overriding a method in the subclass and calling it through a parent class reference.
   - **Code Example (Java):**
     ```java
     class Vehicle {
         void start() {
             System.out.println("Vehicle is starting");
         }
     }
     class Car extends Vehicle {
         @Override
         void start() {
             System.out.println("Car is starting");
         }
     }
     public class Main {
         public static void main(String[] args) {
             Vehicle myVehicle = new Car(); // Dynamic binding
             myVehicle.start(); // Car's start method is called
         }
     }
     ```

#### 8. **Message Passing**
   - **Definition:** Message passing refers to objects communicating by sending messages (method calls) to each other.
   - **Example:** Object `myCar` calls the `start()` method of another object.
   - **Code Example (Java):**
     ```java
     class Car {
         void start() {
             System.out.println("Car started");
         }
     }
     public class Main {
         public static void main(String[] args) {
             Car myCar = new Car();
             myCar.start(); // Message passing
         }
     }
     ```

#### 9. **Garbage Collection**
   - **Definition:** Garbage collection automatically deallocates memory of objects that are no longer in use.
   - **Example:** Objects that no longer have references will be automatically collected.
   - **Code Example (Java):**
     ```java
     public class Main {
         public static void main(String[] args) {
             Car myCar = new Car();
             myCar = null; // Eligible for garbage collection
             System.gc(); // Suggests Java to run garbage collection
         }
     }
     ```

#### 10. **Generic Types, Methods, Collections**
   - **Definition:** Generics allow defining classes and methods with a placeholder for types to increase code reusability.
   - **Example:** A generic `List<T>` can store any type of object.
   - **Code Example (Java):**
     ```java
     import java.util.ArrayList;
     public class Main {
         public static void main(String[] args) {
             ArrayList<String> list = new ArrayList<>(); // Generic collection
             list.add("Hello");
         }
     }
     ```

