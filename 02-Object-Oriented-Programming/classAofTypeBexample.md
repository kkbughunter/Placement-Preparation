## Object type to other class example.

### **Example**

Let's create two classes: `B` and `A`. The `A` class will contain an instance of the `B` class as a member variable.

#### **Class B**

```java
public class B {
    private String data;

    // Constructor
    public B(String data) {
        this.data = data;
    }

    // Method to display data
    public void displayData() {
        System.out.println("Data in class B: " + data);
    }
}
```

#### **Class A**

```java
public class A {
    private B b; // Object reference to class B

    // Constructor
    public A(B b) {
        this.b = b; // Initializing the B object
    }

    // Method to use the B object
    public void useB() {
        System.out.println("Using class B object from class A:");
        b.displayData(); // Calling method from the B object
    }
}
```

#### **Main Class**

```java
public class Main {
    public static void main(String[] args) {
        // Create an instance of B
        B bObject = new B("Hello from B");

        // Create an instance of A, passing the B object
        A aObject = new A(bObject);

        // Use the B object through A
        aObject.useB();
    }
}
```

### **Explanation**

1. **Class `B`**:
   - Defines a `B` class with a `data` attribute and a method `displayData()` to print the data.

2. **Class `A`**:
   - Contains a member variable of type `B` (`b`).
   - Initializes the `B` object through its constructor and provides a method `useB()` that interacts with the `B` object by calling its `displayData()` method.

3. **Main Class**:
   - Creates an instance of `B` with some data.
   - Creates an instance of `A`, passing the `B` object to it.
   - Calls the `useB()` method of `A`, which then interacts with the `B` object.

### **Output**

```
Using class B object from class A:
Data in class B: Hello from B
```

In this example:
- The `A` class holds a reference to an instance of `B` and uses it within its methods.
- This demonstrates how one class (`A`) can include another class (`B`) as a member, allowing `A` to interact with `B` and leverage its functionality.
