# Liskov Substitution Principle (LSP)

## 1. Definition

**LSP is the "L" in SOLID.**

> Objects of a subclass should be replaceable with objects of their superclass without breaking the application.

Simple meaning:

> If a child class replaces a parent class, the application should still work correctly.

---

## 2. Bad Example

```java
class Bird {

    public void fly() {
        System.out.println("Bird is flying");
    }
}
```

```java
class Penguin extends Bird {

    @Override
    public void fly() {
        throw new UnsupportedOperationException("Penguins cannot fly");
    }
}
```

Now:

```java
Bird bird = new Penguin();

bird.fly(); // Exception ❌
```

### Problem

The application expects every `Bird` to fly.

But a `Penguin` cannot fly.

Therefore, replacing `Bird` with `Penguin` breaks the application.

This violates LSP.

---

## 3. Good Design

Put only common behavior in the parent class.

```java
class Bird {

    public void eat() {
        System.out.println("Bird is eating");
    }
}
```

Create a separate interface:

```java
interface Flyable {

    void fly();
}
```

Flying birds:

```java
class Sparrow extends Bird implements Flyable {

    @Override
    public void fly() {
        System.out.println("Sparrow is flying");
    }
}
```

```java
class Eagle extends Bird implements Flyable {

    @Override
    public void fly() {
        System.out.println("Eagle is flying");
    }
}
```

Non-flying bird:

```java
class Penguin extends Bird {
}
```

Now:

```text
Bird
 │
 ├── Sparrow → Can Fly
 ├── Eagle → Can Fly
 └── Penguin → Cannot Fly
```

This follows LSP.

---

## 4. Main Idea

Always ask:

> Can I replace the parent object with any child object without breaking the application?

Example:

```java
Bird bird = new Sparrow();
```

Works correctly ✅

The child behaves according to the contract of the parent.

---

## 5. Common Signs of LSP Violation

Watch for:

```java
throw new UnsupportedOperationException();
```

inside overridden methods.

Other signs:

* Child classes completely change parent behavior
* Parent methods don't make sense for every child
* Too many `instanceof` checks
* Child classes require special handling

---

## 6. LSP and Inheritance

Inheritance means:

```text
Child IS-A Parent
```

LSP means:

> The child should behave like a valid version of the parent.

Just because a child extends a parent does not mean every behavior of the parent is suitable for the child.

---

## 7. Benefits

* Safer inheritance
* Better polymorphism
* Fewer runtime errors
* Less special-case code
* Better maintainability
* Better object-oriented design

---

## 8. Interview Answer

**Q: What is the Liskov Substitution Principle?**

> The Liskov Substitution Principle states that objects of a subclass should be replaceable with objects of their superclass without breaking the correctness of the application. A child class should follow the expected behavior and contract of its parent class.

---

## 9. Quick Revision

```text
L = Liskov Substitution Principle

Parent
   ↓
Replace with Child
   ↓
Application should still work
   ↓
No unexpected behavior
```

### Easy Way to Remember

> **If replacing the parent with the child breaks the program, the inheritance design is probably wrong.**
