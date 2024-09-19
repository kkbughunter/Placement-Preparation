## Overloading VS Overriding

Overloading and overriding are two fundamental concepts in Java that involve methods with similar names but different implementations. Here’s a detailed explanation with examples for each:

### **Method Overloading**

**Definition**: Method overloading occurs when multiple methods in the same class have the same name but different parameter lists (different type, number, or both).

**Key Points**:
- Methods must have different parameter lists.
- Return type alone is not sufficient to distinguish overloaded methods.
- Overloading is resolved at compile-time (static polymorphism).

**Example**:

```java
public class OverloadExample {
    // Method with one integer parameter
    public void display(int num) {
        System.out.println("Number: " + num);
    }

    // Overloaded method with two integer parameters
    public void display(int num1, int num2) {
        System.out.println("Numbers: " + num1 + ", " + num2);
    }

    // Overloaded method with a string parameter
    public void display(String text) {
        System.out.println("Text: " + text);
    }

    public static void main(String[] args) {
        OverloadExample obj = new OverloadExample();
        
        obj.display(10);               // Calls the method with one integer parameter
        obj.display(10, 20);           // Calls the method with two integer parameters
        obj.display("Hello World");    // Calls the method with a string parameter
    }
}
```

**Explanation**:
- The `display` method is overloaded with different parameter lists.
- Depending on the arguments provided, the appropriate `display` method is called.

### **Method Overriding**

**Definition**: Method overriding occurs when a subclass provides a specific implementation of a method that is already defined in its superclass. The method in the subclass must have the same name, return type, and parameter list as the method in the superclass.

**Key Points**:
- The method in the subclass must have the same signature as the method in the superclass.
- Overriding is used to provide a specific implementation for a method that is already defined in the superclass.
- Overriding is resolved at runtime (dynamic polymorphism).

**Example**:

```java
class Animal {
    // Method in superclass
    public void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    // Overriding the method from superclass
    @Override
    public void makeSound() {
        System.out.println("Dog barks");
    }
}

public class OverrideExample {
    public static void main(String[] args) {
        Animal myAnimal = new Animal();
        Animal myDog = new Dog();
        
        myAnimal.makeSound(); // Calls the method in Animal class
        myDog.makeSound();    // Calls the overridden method in Dog class
    }
}
```

**Explanation**:
- `Animal` class has a method `makeSound()`.
- `Dog` class extends `Animal` and overrides the `makeSound()` method to provide a specific implementation.
- At runtime, `myDog.makeSound()` calls the overridden method in the `Dog` class, demonstrating dynamic polymorphism.

### **Differences**

| Aspect            | Overloading                                   | Overriding                                           |
|-------------------|-----------------------------------------------|------------------------------------------------------|
| **Definition**    | Multiple methods with the same name but different parameters in the same class. | Redefining a method in a subclass that is already defined in the superclass. |
| **Method Signature** | Must differ in the number or type of parameters. | Must have the same name, return type, and parameter list as the method in the superclass. |
| **Return Type**   | Return type can be different, but it cannot be used to distinguish overloaded methods. | Return type must be the same as in the superclass method. |
| **Inheritance**   | Not required; can be in the same class.       | Requires inheritance; subclass must extend superclass. |
| **Polymorphism**  | Compile-time (static) polymorphism.           | Runtime (dynamic) polymorphism. |
| **Purpose**       | To provide multiple ways to perform an action. | To provide a specific implementation of a method in a subclass. |
