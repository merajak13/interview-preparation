# Open/Closed Principle (OCP)

## 1. Definition

**OCP is the "O" in SOLID.**

> Software entities should be **open for extension but closed for modification**.

Simple meaning:

> We should be able to add new functionality without modifying existing working code.

---

## 2. Bad Example

```java
class PaymentService {

    public void processPayment(String paymentType) {

        if (paymentType.equals("CARD")) {
            System.out.println("Processing Card Payment");

        } else if (paymentType.equals("UPI")) {
            System.out.println("Processing UPI Payment");
        }
    }
}
```

### Problem

Whenever a new payment method is added, we need to modify `PaymentService`.

For example:

```text
New Payment Method
        ↓
Modify Existing Code ❌
        ↓
Risk of Breaking Existing Functionality
```

This violates OCP.

---

## 3. Good Example

Create an abstraction:

```java
interface Payment {
    void pay();
}
```

Create implementations:

```java
class CardPayment implements Payment {

    @Override
    public void pay() {
        System.out.println("Processing Card Payment");
    }
}
```

```java
class UpiPayment implements Payment {

    @Override
    public void pay() {
        System.out.println("Processing UPI Payment");
    }
}
```

Use the abstraction:

```java
class PaymentService {

    public void processPayment(Payment payment) {
        payment.pay();
    }
}
```

---

## 4. Adding New Functionality

Suppose we want to add PayPal.

```java
class PayPalPayment implements Payment {

    @Override
    public void pay() {
        System.out.println("Processing PayPal Payment");
    }
}
```

We only add a new class.

```text
Existing Code
       ↓
No Modification Needed ✅

New Class
       ↓
New Functionality Added ✅
```

This follows OCP.

---

## 5. Open vs Closed

### Open for Extension

We can add new functionality.

### Closed for Modification

We should avoid changing existing tested and working code.

---

## 6. How OCP Works

OCP is commonly achieved using:

* Interfaces
* Abstract classes
* Polymorphism
* Abstraction
* Dependency Injection

---

## 7. Real-World Example

Payment methods:

```text
Payment
   │
   ├── CardPayment
   ├── UpiPayment
   └── PayPalPayment
```

When a new payment method is needed:

```text
Add New Implementation
        ↓
No Change to Existing Code
```

---

## 8. Benefits

* Easy to extend
* Reduces risk of breaking existing code
* Better maintainability
* Better scalability
* Reduces large if-else blocks
* Encourages clean architecture

---

## 9. OCP and Design Patterns

OCP is commonly used in:

* Strategy Pattern
* Factory Pattern
* Decorator Pattern
* Template Method Pattern

---

## 10. Interview Answer

**Q: What is the Open/Closed Principle?**

> The Open/Closed Principle states that software entities should be open for extension but closed for modification. We should be able to add new functionality without modifying existing tested and working code. This makes applications easier to maintain and extend.

---

## 11. Quick Revision

```text
O = Open/Closed Principle

Open
↓
Extend functionality

Closed
↓
Avoid modifying existing working code

Common Solution
↓
Interface + Abstraction + Polymorphism
```

### Easy Way to Remember

> **Add new functionality by extending the system instead of repeatedly modifying existing code.**
