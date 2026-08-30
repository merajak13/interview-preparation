# Dependency Inversion Principle (DIP)

## 1. Definition

**DIP is the "D" in SOLID.**

> High-level modules should not depend on low-level modules. Both should depend on abstractions.

> Abstractions should not depend on details. Details should depend on abstractions.

Simple meaning:

> **Depend on interfaces or abstractions, not concrete classes.**

---

## 2. Bad Example

```java
class EmailService {

    public void sendEmail() {
        System.out.println("Email sent");
    }
}
```

```java
class NotificationService {

    private EmailService emailService = new EmailService();

    public void sendNotification() {
        emailService.sendEmail();
    }
}
```

### Problem

`NotificationService` directly depends on `EmailService`.

```text
NotificationService
        ↓
   EmailService
```

If we want to use SMS instead:

```text
NotificationService
        ↓
Modify Existing Code ❌
```

This creates tight coupling.

---

## 3. Good Design

Create an abstraction:

```java
interface Notification {

    void send();
}
```

Create implementations:

```java
class EmailService implements Notification {

    @Override
    public void send() {
        System.out.println("Email sent");
    }
}
```

```java
class SmsService implements Notification {

    @Override
    public void send() {
        System.out.println("SMS sent");
    }
}
```

Now depend on the abstraction:

```java
class NotificationService {

    private final Notification notification;

    public NotificationService(Notification notification) {
        this.notification = notification;
    }

    public void sendNotification() {
        notification.send();
    }
}
```

---

## 4. How It Works

We can now use:

```java
Notification email = new EmailService();

NotificationService service =
        new NotificationService(email);

service.sendNotification();
```

Or:

```java
Notification sms = new SmsService();

NotificationService service =
        new NotificationService(sms);

service.sendNotification();
```

`NotificationService` does not care whether it is Email or SMS.

It only depends on:

```text
Notification Interface
```

This follows DIP.

---

## 5. Main Idea

Bad design:

```text
High-Level Class
       ↓
Concrete Implementation
```

Good design:

```text
High-Level Class
       ↓
   Abstraction
       ↑
Concrete Implementations
```

Example:

```text
             Notification
                  ↑
             Interface
             /         \
            /           \
    EmailService      SmsService

             ↑
             │
    NotificationService
```

---

## 6. DIP in Spring Boot

DIP is used heavily in Spring Boot through **Dependency Injection**.

Example:

```java
@Service
class OrderService {

    private final PaymentService paymentService;

    public OrderService(PaymentService paymentService) {
        this.paymentService = paymentService;
    }
}
```

Spring injects the dependency.

The important idea is that we should preferably depend on an abstraction:

```java
interface PaymentService {
    void pay();
}
```

```java
@Service
class CardPaymentService implements PaymentService {

    public void pay() {
        System.out.println("Card payment");
    }
}
```

```java
@Service
class OrderService {

    private final PaymentService paymentService;

    public OrderService(PaymentService paymentService) {
        this.paymentService = paymentService;
    }
}
```

Now `OrderService` depends on the interface, not a specific payment implementation.

---

## 7. DIP vs Dependency Injection

These are related but different.

### Dependency Inversion Principle

A **design principle**.

```text
Depend on abstractions
Not concrete implementations
```

### Dependency Injection

A **technique** used to provide dependencies.

```text
Constructor Injection
Setter Injection
Field Injection
```

Spring Boot commonly uses Dependency Injection to help implement DIP.

---

## 8. Benefits

* Loose coupling
* Easy to replace implementations
* Easy to test
* Better maintainability
* More flexible design
* Easier to extend

---

## 9. Interview Answer

**Q: What is the Dependency Inversion Principle?**

> The Dependency Inversion Principle states that high-level modules should not depend directly on low-level modules. Both should depend on abstractions. In simple terms, we should depend on interfaces or abstractions instead of concrete implementations.

---

## 10. Quick Revision

```text
D = Dependency Inversion Principle

High-Level Module
       ↓
   Abstraction
       ↑
Low-Level Module

Depend on
Interfaces / Abstractions

Not on
Concrete Classes
```

### Easy Way to Remember

> **Depend on what something does, not on how it does it.**
