# Interface Segregation Principle (ISP)

## 1. Definition

**ISP is the "I" in SOLID.**

> Clients should not be forced to depend on interfaces they do not use.

Simple meaning:

> A class should not be forced to implement methods that it does not need.

Instead of creating one large interface, create smaller and focused interfaces.

---

## 2. Bad Example

Suppose we have a large interface:

```java
interface Worker {

    void work();

    void eat();

    void sleep();
}
```

Now:

```java
class HumanWorker implements Worker {

    @Override
    public void work() {
        System.out.println("Human is working");
    }

    @Override
    public void eat() {
        System.out.println("Human is eating");
    }

    @Override
    public void sleep() {
        System.out.println("Human is sleeping");
    }
}
```

This is fine for a human.

But consider a robot:

```java
class RobotWorker implements Worker {

    @Override
    public void work() {
        System.out.println("Robot is working");
    }

    @Override
    public void eat() {
        throw new UnsupportedOperationException();
    }

    @Override
    public void sleep() {
        throw new UnsupportedOperationException();
    }
}
```

### Problem

A robot can work, but it does not need to eat or sleep.

However, `RobotWorker` is forced to implement unnecessary methods.

This violates ISP.

---

## 3. Good Design

Split the large interface into smaller interfaces.

```java
interface Workable {

    void work();
}
```

```java
interface Eatable {

    void eat();
}
```

```java
interface Sleepable {

    void sleep();
}
```

Now a human can implement all required interfaces:

```java
class HumanWorker implements Workable, Eatable, Sleepable {

    @Override
    public void work() {
        System.out.println("Human is working");
    }

    @Override
    public void eat() {
        System.out.println("Human is eating");
    }

    @Override
    public void sleep() {
        System.out.println("Human is sleeping");
    }
}
```

A robot only implements what it needs:

```java
class RobotWorker implements Workable {

    @Override
    public void work() {
        System.out.println("Robot is working");
    }
}
```

This follows ISP.

---

## 4. Main Idea

Instead of:

```text
One Large Interface
        ↓
Many Unnecessary Methods
        ↓
Classes Forced to Implement Them ❌
```

Use:

```text
Small Focused Interfaces
        ↓
Classes Implement Only What They Need ✅
```

---

## 5. Real-World Example

Consider a printer system.

Bad design:

```java
interface Machine {

    void print();

    void scan();

    void fax();
}
```

A simple printer only needs:

```text
Print
```

But it is forced to implement:

```text
Scan
Fax
```

Better design:

```java
interface Printer {
    void print();
}
```

```java
interface Scanner {
    void scan();
}
```

```java
interface Fax {
    void fax();
}
```

Now each machine implements only the required interfaces.

---

## 6. Benefits

* Smaller and focused interfaces
* Less unnecessary code
* Better maintainability
* Better flexibility
* Reduced coupling
* Easier testing
* Easier to understand

---

## 7. ISP and LSP

ISP and LSP are often related.

If a class is forced to implement a method that it does not support:

```java
throw new UnsupportedOperationException();
```

It can indicate:

* ISP violation → Interface is too large
* Possibly LSP violation → Child cannot properly support expected behavior

---

## 8. Interview Answer

**Q: What is the Interface Segregation Principle?**

> The Interface Segregation Principle states that clients should not be forced to depend on or implement methods they do not use. Large interfaces should be divided into smaller and more specific interfaces.

---

## 9. Quick Revision

```text
I = Interface Segregation Principle

Large Interface
      ↓
Split into
      ↓
Small Focused Interfaces
      ↓
Implement Only What You Need
```

### Easy Way to Remember

> **Do not force a class to implement methods it does not need.**
