# Deloitte Software Engineer II – Priority Interview Questions

> Target: Java Backend Developer / Software Engineer II
> Focus: Java + Spring Boot + Microservices + SQL + JPA + Project + Coding

---

## 🔴 Tier 1 – Must Master

### 1. Core Java

- [ ] Explain OOP principles with real-world examples.
- [ ] Encapsulation vs Abstraction.
- [ ] Interface vs Abstract Class.
- [ ] Method Overloading vs Method Overriding.
- [ ] Compile-time vs Runtime Polymorphism.
- [ ] `==` vs `equals()`.
- [ ] Why must `equals()` and `hashCode()` be consistent?
- [ ] Why is String immutable in Java?
- [ ] Explain String Pool.
- [ ] String vs StringBuilder vs StringBuffer.
- [ ] `final` vs `finally` vs `finalize`.
- [ ] Static keyword and its use cases.
- [ ] Constructor and constructor chaining.
- [ ] Shallow copy vs Deep copy.
- [ ] How would you create an immutable class?
- [ ] Composition vs Inheritance.
- [ ] Explain SOLID principles.
- [ ] What is clean code?
- [ ] How do you refactor existing code safely?

---

### 2. Collections

- [ ] List vs Set vs Map.
- [ ] ArrayList vs LinkedList.
- [ ] How does HashMap work internally?
- [ ] How does HashMap handle collisions?
- [ ] HashMap vs Hashtable.
- [ ] HashMap vs ConcurrentHashMap.
- [ ] HashSet internal implementation.
- [ ] TreeMap vs HashMap.
- [ ] Comparable vs Comparator.
- [ ] Fail-fast vs Fail-safe.
- [ ] What happens if a mutable object is used as a HashMap key?
- [ ] Time complexity of common Collection operations.

---

### 3. Java 8

- [ ] What are Functional Interfaces?
- [ ] Explain Lambda Expressions.
- [ ] Predicate vs Function vs Consumer vs Supplier.
- [ ] What is Stream API?
- [ ] Intermediate vs Terminal operations.
- [ ] `map()` vs `flatMap()`.
- [ ] `filter()` vs `map()`.
- [ ] `reduce()` with example.
- [ ] `findFirst()` vs `findAny()`.
- [ ] `groupingBy()` vs `partitioningBy()`.
- [ ] Optional and its best practices.
- [ ] Sequential vs Parallel Streams.

---

### 4. Concurrency

- [ ] Process vs Thread.
- [ ] Thread lifecycle.
- [ ] Runnable vs Callable.
- [ ] `synchronized` keyword.
- [ ] What is a race condition?
- [ ] What is `volatile`?
- [ ] Deadlock and how to prevent it.
- [ ] What makes code thread-safe?
- [ ] ExecutorService and Thread Pool.
- [ ] Future vs CompletableFuture.
- [ ] CompletableFuture chaining.
- [ ] ConcurrentHashMap.
- [ ] Atomic classes.
- [ ] Lock vs synchronized.

---

## 🔴 Spring Boot + REST

### 5. Spring Core

- [ ] What is Spring Framework?
- [ ] What is IoC?
- [ ] What is Dependency Injection?
- [ ] Constructor Injection vs Field Injection.
- [ ] `@Autowired`, `@Qualifier`, `@Primary`.
- [ ] What is a Spring Bean?
- [ ] Bean lifecycle.
- [ ] Singleton vs Prototype scope.
- [ ] ApplicationContext.
- [ ] Circular dependency.
- [ ] `@PostConstruct`.
- [ ] Spring Proxy.
- [ ] AOP and its use cases.

---

### 6. Spring Boot

- [ ] Spring vs Spring Boot.
- [ ] Explain `@SpringBootApplication`.
- [ ] How does Spring Boot Auto Configuration work?
- [ ] What are Spring Boot Starters?
- [ ] Embedded Tomcat.
- [ ] application.properties vs application.yml.
- [ ] Spring Profiles.
- [ ] `@Value` vs `@ConfigurationProperties`.
- [ ] Spring Boot Actuator.
- [ ] Health checks.
- [ ] Spring Boot startup flow.
- [ ] How do you troubleshoot a Spring Boot startup failure?

---

### 7. REST API

- [ ] REST principles.
- [ ] GET vs POST.
- [ ] PUT vs PATCH.
- [ ] DELETE.
- [ ] Idempotency.
- [ ] Important HTTP status codes.
- [ ] `@PathVariable` vs `@RequestParam`.
- [ ] `@RequestBody`.
- [ ] ResponseEntity.
- [ ] DTO vs Entity.
- [ ] Request validation.
- [ ] Global Exception Handling.
- [ ] `@ControllerAdvice`.
- [ ] API versioning.
- [ ] Pagination and sorting.
- [ ] Filtering.
- [ ] REST API security.
- [ ] Swagger/OpenAPI.
- [ ] How would you improve API performance?

---

## 🔴 Microservices

### 8. Microservices Fundamentals

- [ ] Monolith vs Microservices.
- [ ] Advantages and disadvantages of Microservices.
- [ ] How do you define service boundaries?
- [ ] Database per service.
- [ ] Inter-service communication.
- [ ] REST vs gRPC.
- [ ] Synchronous vs Asynchronous communication.
- [ ] API Gateway.
- [ ] Service Discovery.
- [ ] Load Balancing.
- [ ] Circuit Breaker.
- [ ] Retry mechanism.
- [ ] Timeout.
- [ ] Bulkhead pattern.
- [ ] Saga Pattern.
- [ ] Distributed Transactions.
- [ ] Data Consistency in Microservices.
- [ ] Distributed tracing.
- [ ] Correlation ID.
- [ ] Handling downstream service failure.

### 9. Microservices Design Scenarios

- [ ] Design Customer + Account + Transaction microservices.
- [ ] Design a Banking Transaction API.
- [ ] Design a scalable REST API.
- [ ] Design a Notification Service.
- [ ] Design a Payment Service.

---

## 🔴 SQL + JPA/Hibernate

### 10. SQL

- [ ] Primary Key vs Foreign Key.
- [ ] INNER JOIN vs LEFT JOIN.
- [ ] GROUP BY and HAVING.
- [ ] WHERE vs HAVING.
- [ ] Subquery.
- [ ] CTE.
- [ ] Window Functions.
- [ ] Indexes.
- [ ] Composite Index.
- [ ] Query performance troubleshooting.
- [ ] Database normalization.
- [ ] 1NF, 2NF, 3NF.
- [ ] ACID properties.
- [ ] Transaction isolation levels.
- [ ] Database locking.
- [ ] Deadlocks.
- [ ] EXPLAIN / execution plan.
- [ ] How would you optimize a slow SQL query?

### 11. SQL Coding

- [ ] Find second-highest salary.
- [ ] Find Nth-highest salary.
- [ ] Find duplicate records.
- [ ] Delete duplicate records.
- [ ] Find highest salary per department.
- [ ] Find employees earning more than their manager.
- [ ] Find departments having more than N employees.
- [ ] Running total.
- [ ] Ranking using Window Functions.
- [ ] Find consecutive records.

---

### 12. JPA / Hibernate

- [ ] JPA vs Hibernate.
- [ ] Entity lifecycle.
- [ ] `@Entity`, `@Id`, `@GeneratedValue`.
- [ ] One-to-One relationship.
- [ ] One-to-Many relationship.
- [ ] Many-to-Many relationship.
- [ ] Lazy vs Eager loading.
- [ ] N+1 problem.
- [ ] Cascade types.
- [ ] orphanRemoval.
- [ ] `@Transactional`.
- [ ] First-level vs Second-level cache.
- [ ] Optimistic vs Pessimistic locking.
- [ ] JPQL vs Native Query.
- [ ] Pagination with JPA.
- [ ] Hibernate performance optimization.

---

# 🔴 EY Project – Must Prepare

- [ ] Explain your current project in 2 minutes.
- [ ] Explain the business problem.
- [ ] Explain the overall architecture.
- [ ] What exactly did YOU work on?
- [ ] Explain the APIs you developed.
- [ ] Explain PostgreSQL usage.
- [ ] Explain Practice Balance.
- [ ] Explain V1/V2 structure.
- [ ] Explain FAID and Branch levels.
- [ ] Explain the API performance improvement.
- [ ] Why was table flattening required?
- [ ] What was your Kafka use case?
- [ ] Why Kafka instead of REST?
- [ ] Explain Swagger usage.
- [ ] Explain Cucumber testing.
- [ ] Explain your gRPC work.
- [ ] Explain the Java library you worked on.
- [ ] Describe a challenging technical problem.
- [ ] Describe a production issue you handled.
- [ ] How did you troubleshoot the issue?
- [ ] How did you improve API performance?
- [ ] What was the biggest technical challenge?
- [ ] How did you interact with the client/business team?

---

# 🔴 Coding – Must Practice

### Arrays / HashMap / Strings

- [ ] Reverse a String.
- [ ] Check Palindrome.
- [ ] Find Maximum and Minimum.
- [ ] Find Second Largest Element.
- [ ] Remove Duplicates.
- [ ] Move Zeroes to End.
- [ ] Find Missing Number.
- [ ] Find Duplicate Number.
- [ ] Two Sum.
- [ ] Valid Anagram.
- [ ] First Non-Repeating Character.
- [ ] Character Frequency using HashMap.
- [ ] Group Anagrams.
- [ ] Longest Substring Without Repeating Characters.
- [ ] Maximum Subarray.
- [ ] Merge Two Sorted Arrays.
- [ ] Rotate Array.
- [ ] Product of Array Except Self.

### Linked List

- [ ] Reverse Linked List.
- [ ] Detect Cycle.
- [ ] Find Middle Node.
- [ ] Merge Two Sorted Linked Lists.
- [ ] Remove Nth Node From End.

### Stack / Queue

- [ ] Valid Parentheses.
- [ ] Min Stack.
- [ ] Next Greater Element.
- [ ] Implement Queue using Stack.
- [ ] Implement Stack using Queue.

---

# 🟡 Tier 2 – Important

## Spring Security

- [ ] Authentication vs Authorization.
- [ ] Spring Security architecture.
- [ ] SecurityFilterChain.
- [ ] JWT structure.
- [ ] JWT authentication flow.
- [ ] Access Token vs Refresh Token.
- [ ] OAuth2.
- [ ] CORS.
- [ ] CSRF.
- [ ] Role vs Authority.
- [ ] Secure REST APIs.
- [ ] API Gateway authentication.

## Kafka

- [ ] What is Kafka?
- [ ] Topic.
- [ ] Partition.
- [ ] Producer.
- [ ] Consumer.
- [ ] Consumer Group.
- [ ] Offset.
- [ ] Message ordering.
- [ ] Replication.
- [ ] `@KafkaListener`.
- [ ] Retry and failure handling.
- [ ] Dead Letter Topic.
- [ ] At-least-once delivery.
- [ ] Exactly-once semantics.
- [ ] Kafka vs REST.
- [ ] Explain your Kafka use case.

## AWS

- [ ] EC2.
- [ ] ECS vs EKS.
- [ ] Lambda.
- [ ] Elastic Beanstalk.
- [ ] API Gateway.
- [ ] ALB.
- [ ] RDS PostgreSQL/MySQL.
- [ ] DynamoDB.
- [ ] IAM.
- [ ] VPC.
- [ ] Security Groups.
- [ ] Secrets Manager.
- [ ] Parameter Store.
- [ ] S3.
- [ ] CloudFront.
- [ ] CloudWatch.
- [ ] CI/CD on AWS.

---

# 🟡 Tier 3 – Know the Concepts

- [ ] Docker image vs container.
- [ ] Dockerfile.
- [ ] Docker networking.
- [ ] Docker volumes.
- [ ] CMD vs ENTRYPOINT.
- [ ] Kubernetes Pod.
- [ ] Deployment.
- [ ] Service.
- [ ] ConfigMap.
- [ ] Secret.
- [ ] Liveness vs Readiness Probe.
- [ ] HPA.
- [ ] Rolling Deployment.
- [ ] Jenkins Pipeline.
- [ ] Jenkinsfile.
- [ ] CI vs CD.
- [ ] JUnit 5.
- [ ] Mockito.
- [ ] Unit vs Integration Testing.
- [ ] System Design basics.
- [ ] Agile/Scrum.
- [ ] Behavioral questions.

---

# 🎯 Final Revision Strategy

## Round 1 – Learn
Complete all 🔴 questions.

## Round 2 – Practice
Solve all 🔴 coding questions without looking at the solution.

## Round 3 – Project
Practice explaining the EY project in:
1. 30 seconds
2. 2 minutes
3. 5 minutes

## Round 4 – Mock Interview
Randomly pick questions from:
- Core Java
- Spring Boot
- REST  
- Microservices
- SQL
- JPA/Hibernate
- Kafka
- EY Project
- Coding

## Final Goal

> Be able to explain every 🔴 question confidently,
> solve the coding problems without assistance,
> and explain your project with clear ownership and technical depth.