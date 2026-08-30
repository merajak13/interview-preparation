# Single Responsibility Principle (SRP)

## 1. Definition

**SRP is the "S" in SOLID.**

> A class should have only **one responsibility** and **one reason to change**.

In simple words:

> **One class should focus on one responsibility.**

---

## 2. Example

### ❌ Bad Design

```java
class UserManager {

    public void registerUser() {
    }

    public void sendEmail() {
    }

    public void generateReport() {
    }
}
```

Here, `UserManager` has multiple responsibilities:

* User registration
* Email sending
* Report generation

Therefore, it violates SRP.

### ✅ Good Design

Separate responsibilities into different classes:

```java
class UserService {
    public void registerUser() {
    }
}

class EmailService {
    public void sendEmail() {
    }
}

class ReportService {
    public void generateReport() {
    }
}
```

Each class now has a single responsibility.

---

## 3. "One Reason to Change"

This is the most important concept in SRP.

If a class can change because of multiple unrelated requirements, it probably violates SRP.

Example:

```text
UserService
 ├── Database changes
 ├── Email changes
 └── Report changes
```

Multiple reasons to change ❌

After applying SRP:

```text
UserService     → User management
EmailService    → Email management
ReportService   → Report generation
```

One responsibility per class ✅

---

## 4. Important Point

SRP does **NOT** mean:

> One class should contain only one method.

It means:

> Methods inside a class should belong to the same responsibility.

For example, these methods can exist together:

```java
class UserService {

    createUser();
    updateUser();
    deleteUser();
    getUser();
}
```

Because all of them belong to **User Management**.

---

## 5. Benefits

* Easier to maintain
* Easier to test
* Better readability
* Lower coupling
* Easier debugging
* Better code reusability

---

## 6. Spring Boot Example

Instead of putting everything inside `OrderService`:

```text
OrderService
 ├── Payment
 ├── Inventory
 ├── Notification
 └── Invoice
```

Separate them:

```text
OrderService          → Order management
PaymentService        → Payment processing
InventoryService      → Inventory management
NotificationService   → Notifications
InvoiceService        → Invoice generation
```

---

## 7. Interview Answer

**Q: What is SRP?**

> The Single Responsibility Principle states that a class should have one responsibility or one reason to change. It helps create maintainable, testable, readable, and loosely coupled code.

---

## 8. Quick Revision

```text
S = Single Responsibility Principle

One class
    ↓
One responsibility
    ↓
One reason to change
    ↓
Maintainable & testable code
```
