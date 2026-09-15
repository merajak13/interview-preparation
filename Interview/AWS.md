# Deloitte Software Engineer II – AWS Priority Interview Questions

> **Target:** Java Backend Developer / Software Engineer II  
> **Focus:** AWS questions relevant to the Deloitte Software Engineer II JD  
> **Priority:** 🔴 Must Know / 🟡 Important / 🟢 Conceptual

---

## 1. AWS Fundamentals

### 🔴 Must Know

- [ ] What is AWS and why is it used for backend applications?
- [ ] What are the main components of a typical AWS backend architecture?
- [ ] What is the difference between Region and Availability Zone?
- [ ] How would you design a highly available application in AWS?
- [ ] What is scalability vs elasticity in AWS?
- [ ] What is horizontal scaling vs vertical scaling?
- [ ] How do you make a backend application fault tolerant in AWS?
- [ ] What is the AWS Shared Responsibility Model?

---

## 2. EC2

### 🔴 Must Know

- [ ] What is Amazon EC2?
- [ ] What is an EC2 instance?
- [ ] What are AMIs?
- [ ] What are EC2 instance types?
- [ ] How would you choose an EC2 instance for a Java Spring Boot application?
- [ ] What is an EC2 Security Group?
- [ ] Security Group vs Network ACL.
- [ ] What is an Elastic IP?
- [ ] What is EC2 Auto Scaling?
- [ ] How does an Auto Scaling Group work?
- [ ] How would you deploy a Spring Boot application on EC2?
- [ ] How would you handle high traffic on an EC2-based application?
- [ ] What happens if an EC2 instance goes down?
- [ ] How would you troubleshoot a Spring Boot application running slowly on EC2?

### 🟡 Important

- [ ] EC2 Instance Store vs EBS.
- [ ] What is EBS?
- [ ] What are EBS snapshots?
- [ ] How do you monitor EC2 instances?
- [ ] How would you securely connect to an EC2 instance?
- [ ] How do you avoid exposing an EC2 instance directly to the internet?

---

## 3. ECS / EKS

### 🔴 Must Know

- [ ] What is Amazon ECS?
- [ ] What is Amazon EKS?
- [ ] ECS vs EKS.
- [ ] ECS vs EC2.
- [ ] Why would you use containers for microservices?
- [ ] How would you deploy a Spring Boot microservice using ECS?
- [ ] How would you deploy a Spring Boot microservice using EKS?
- [ ] What is a Kubernetes Pod?
- [ ] What is a Kubernetes Deployment?
- [ ] What is a Kubernetes Service?
- [ ] How does EKS help run microservices?
- [ ] How would you scale microservices running on EKS?
- [ ] How would you perform zero/minimal-downtime deployment on EKS?

### 🟡 Important

- [ ] EKS Node vs Pod.
- [ ] What is a Managed Node Group?
- [ ] What is the EKS Control Plane?
- [ ] Kubernetes ConfigMap vs Secret.
- [ ] Liveness vs Readiness Probe.
- [ ] What is Horizontal Pod Autoscaler?
- [ ] What is Rolling Deployment?
- [ ] How would you troubleshoot a Pod that keeps restarting?

---

## 4. AWS Lambda

### 🔴 Must Know

- [ ] What is AWS Lambda?
- [ ] Lambda vs EC2.
- [ ] When would you choose Lambda over EC2?
- [ ] What is a Lambda function?
- [ ] What triggers can invoke a Lambda?
- [ ] What are Lambda cold starts?
- [ ] How would you reduce Lambda cold-start problems?
- [ ] What are Lambda limitations?
- [ ] Can Lambda be used for backend APIs?
- [ ] How can API Gateway invoke Lambda?
- [ ] How would you handle errors and retries in Lambda?

### 🟡 Important

- [ ] What is Lambda concurrency?
- [ ] Reserved vs Provisioned Concurrency.
- [ ] What is Lambda timeout?
- [ ] How does Lambda memory configuration work?
- [ ] Lambda environment variables.
- [ ] Lambda + S3 use case.
- [ ] Lambda + asynchronous processing use case.

---

## 5. Elastic Beanstalk

### 🟡 Important

- [ ] What is AWS Elastic Beanstalk?
- [ ] Elastic Beanstalk vs EC2.
- [ ] Elastic Beanstalk vs ECS/EKS.
- [ ] How would you deploy a Spring Boot application using Elastic Beanstalk?
- [ ] What AWS resources does Elastic Beanstalk manage?
- [ ] When would you prefer Elastic Beanstalk over ECS/EKS?

---

## 6. API Gateway

### 🔴 Must Know

- [ ] What is Amazon API Gateway?
- [ ] Why would you use API Gateway in a microservices architecture?
- [ ] API Gateway vs Load Balancer.
- [ ] How does API Gateway route requests?
- [ ] How would you secure API Gateway?
- [ ] How can API Gateway integrate with Lambda?
- [ ] How can API Gateway integrate with backend microservices?
- [ ] How would you implement rate limiting?
- [ ] How would you handle authentication at API Gateway?
- [ ] How would you handle throttling?
- [ ] How would you version APIs?
- [ ] How would you monitor API Gateway requests?

### 🎯 Scenario

- [ ] You have Customer, Account, Payment and Transaction microservices. How would you use API Gateway in front of them?

---

## 7. Application Load Balancer (ALB)

### 🔴 Must Know

- [ ] What is an Application Load Balancer?
- [ ] Why do we need a load balancer?
- [ ] ALB vs API Gateway.
- [ ] ALB vs NLB.
- [ ] How does ALB distribute traffic?
- [ ] What is a Target Group?
- [ ] What is a Listener?
- [ ] What are health checks?
- [ ] How would ALB route traffic to Spring Boot microservices?
- [ ] How would you achieve high availability using ALB?
- [ ] How does ALB work with Auto Scaling?
- [ ] How would you troubleshoot HTTP 502/503 errors behind an ALB?

### 🎯 Scenario

- [ ] Design an architecture where an ALB distributes traffic across multiple Spring Boot instances running in different Availability Zones.

---

## 8. RDS – PostgreSQL / MySQL

### 🔴 Must Know

- [ ] What is Amazon RDS?
- [ ] Why use RDS instead of installing MySQL/PostgreSQL on EC2?
- [ ] Which relational databases does RDS support?
- [ ] RDS vs DynamoDB.
- [ ] How would you configure a Spring Boot application to connect to RDS?
- [ ] How would you secure an RDS database?
- [ ] What is Multi-AZ deployment?
- [ ] What is a Read Replica?
- [ ] Multi-AZ vs Read Replica.
- [ ] How would you scale an RDS database?
- [ ] Vertical vs horizontal scaling for RDS.
- [ ] How would you troubleshoot a slow RDS database?
- [ ] How would you monitor RDS?
- [ ] How would you handle database connection limits?
- [ ] How does connection pooling help with RDS?

### 🎯 Scenario

- [ ] Your Spring Boot API is becoming slow because database queries are taking longer. How would you troubleshoot the issue in AWS RDS?

---

## 9. DynamoDB

### 🟡 Important

- [ ] What is Amazon DynamoDB?
- [ ] DynamoDB vs RDS.
- [ ] SQL database vs NoSQL database.
- [ ] What is a partition key?
- [ ] What is a sort key?
- [ ] What is a composite primary key?
- [ ] How does DynamoDB scale?
- [ ] What are DynamoDB indexes?
- [ ] GSI vs LSI.
- [ ] When would you choose DynamoDB over PostgreSQL?
- [ ] What are DynamoDB consistency models?
- [ ] How would you design a DynamoDB table for a high-volume application?
- [ ] What problems can occur with poor partition-key design?

---

## 10. IAM

### 🔴 Must Know

- [ ] What is AWS IAM?
- [ ] User vs Role vs Policy.
- [ ] What is an IAM Policy?
- [ ] Identity-based vs Resource-based policies.
- [ ] What is the Principle of Least Privilege?
- [ ] Why should applications avoid hardcoded AWS access keys?
- [ ] How would an EC2 application securely access S3?
- [ ] How would a Spring Boot application running on AWS access other AWS services securely?
- [ ] IAM Role vs IAM User.
- [ ] How would you troubleshoot an AccessDenied error?

### 🎯 Scenario

- [ ] A Spring Boot service running on EC2 needs to read files from S3. How would you give it permission securely?

---

## 11. Cognito

### 🟡 Important

- [ ] What is Amazon Cognito?
- [ ] What problem does Cognito solve?
- [ ] Cognito User Pool vs Identity Pool.
- [ ] How does Cognito authentication work?
- [ ] How would Cognito integrate with a REST API?
- [ ] Cognito vs implementing authentication completely inside Spring Security.
- [ ] How would you validate a JWT issued by Cognito?
- [ ] How would you implement role-based authorization?

---

## 12. VPC

### 🔴 Must Know

- [ ] What is Amazon VPC?
- [ ] What is a subnet?
- [ ] Public subnet vs Private subnet.
- [ ] What is an Internet Gateway?
- [ ] What is a NAT Gateway?
- [ ] What is a Route Table?
- [ ] What is a Security Group?
- [ ] What is a Network ACL?
- [ ] How would you design a VPC for a Spring Boot microservices application?
- [ ] Why should RDS generally be placed in private subnets?
- [ ] How can an application in a private subnet access the internet?
- [ ] How would you allow an application server to communicate with RDS securely?

### 🎯 Scenario

- [ ] Design a VPC where the ALB is public, Spring Boot services are private, and PostgreSQL RDS is also private.

---

## 13. Secrets Manager / Parameter Store

### 🔴 Must Know

- [ ] Why should database passwords not be stored in application.properties?
- [ ] What is AWS Secrets Manager?
- [ ] What is AWS Systems Manager Parameter Store?
- [ ] Secrets Manager vs Parameter Store.
- [ ] How would a Spring Boot application retrieve database credentials securely?
- [ ] How would you rotate database credentials?
- [ ] How would IAM control access to secrets?
- [ ] How would you avoid exposing secrets in application logs?

### 🎯 Scenario

- [ ] Your Spring Boot application needs PostgreSQL username/password in production. How would you design the configuration securely?

---

## 14. S3

### 🔴 Must Know

- [ ] What is Amazon S3?
- [ ] What is an S3 Bucket?
- [ ] What is an S3 Object?
- [ ] S3 vs EBS.
- [ ] How would a Spring Boot application upload a file to S3?
- [ ] How would you secure an S3 bucket?
- [ ] What is an S3 Bucket Policy?
- [ ] IAM Policy vs Bucket Policy.
- [ ] What is S3 Versioning?
- [ ] What is S3 Lifecycle Management?
- [ ] How would you handle large file uploads?
- [ ] How would you generate secure temporary access to an S3 object?

---

## 15. CloudFront

### 🟡 Important

- [ ] What is Amazon CloudFront?
- [ ] Why use CloudFront with S3?
- [ ] What is a CDN?
- [ ] How does CloudFront improve performance?
- [ ] CloudFront vs S3.
- [ ] How would you serve static frontend files using S3 + CloudFront?
- [ ] How would CloudFront improve performance for users located far from the AWS Region?
- [ ] What is caching in CloudFront?
- [ ] How would you invalidate cached content?

### 🎯 Scenario

- [ ] Design an architecture for a React/Angular frontend hosted on S3 and delivered globally using CloudFront.

---

## 16. CloudWatch

### 🔴 Must Know

- [ ] What is Amazon CloudWatch?
- [ ] Logs vs Metrics vs Alarms.
- [ ] How would you monitor a Spring Boot application in AWS?
- [ ] How would you monitor CPU and memory?
- [ ] How would you create an alert for high CPU usage?
- [ ] How would you troubleshoot a 500 error using CloudWatch?
- [ ] How would you troubleshoot a 504 Gateway Timeout?
- [ ] How would you monitor API latency?
- [ ] How would you monitor application errors?
- [ ] How would you create production alerts?

### 🎯 Production Scenarios

- [ ] Your API suddenly starts returning 500 errors in production. What AWS tools would you use to investigate?
- [ ] CPU usage of an EC2 instance suddenly reaches 95%. What would you check?
- [ ] API latency increases from 200 ms to 5 seconds. How would you troubleshoot it?
- [ ] ALB starts returning 504 errors. How would you investigate?
- [ ] RDS CPU reaches 90–100%. What would you check?

---

## 17. CI/CD – AWS + Jenkins / GitHub Actions

### 🔴 Must Know

- [ ] What is CI/CD?
- [ ] Explain a CI/CD pipeline for a Spring Boot application.
- [ ] How would Jenkins build a Spring Boot application?
- [ ] Where would Maven fit in the pipeline?
- [ ] How would you run unit tests in CI?
- [ ] How would you build a Docker image?
- [ ] How would you push a Docker image to a container registry?
- [ ] How would you deploy the application to AWS?
- [ ] Jenkins vs GitHub Actions.
- [ ] AWS CodePipeline vs Jenkins.
- [ ] AWS CodeBuild.
- [ ] How would you implement rollback?
- [ ] How would you achieve zero-downtime deployment?

### 🎯 Scenario

- [ ] Developer pushes code to GitHub → Jenkins builds the application → tests run → Docker image is created → image is pushed → application is deployed to AWS. Explain the complete flow.

---

## 18. Docker + AWS

### 🔴 Must Know

- [ ] Why containerize a Spring Boot application?
- [ ] Docker Image vs Container.
- [ ] How do you create a Dockerfile for Spring Boot?
- [ ] How would you pass environment-specific configuration to a container?
- [ ] Where would you store Docker images in AWS?
- [ ] How does Docker integrate with ECS/EKS?
- [ ] How would you troubleshoot a container that keeps restarting?
- [ ] How would you reduce Docker image size?

---

## 19. AWS Security Scenarios

### 🔴 Must Know

- [ ] How would you secure a production Spring Boot application on AWS?
- [ ] How would you protect APIs from unauthorized access?
- [ ] How would you protect database credentials?
- [ ] How would you secure communication between services?
- [ ] How would you restrict access to RDS?
- [ ] How would you secure S3?
- [ ] How would you implement least-privilege IAM?
- [ ] How would you prevent secrets from being committed to Git?
- [ ] How would you investigate an unexpected AccessDenied error?
- [ ] How would you secure a public API exposed through API Gateway?

---

# 20. Deloitte-Style AWS Architecture Questions

### 🔴 High Priority

- [ ] Design a highly available Spring Boot application on AWS.
- [ ] Design a scalable Java microservices architecture on AWS.
- [ ] Design Customer, Account, Payment and Transaction microservices on AWS.
- [ ] Design a banking application using Spring Boot + AWS.
- [ ] Design a REST API using API Gateway + ALB + Spring Boot.
- [ ] Design a Spring Boot application using EC2 + ALB + RDS.
- [ ] Design a microservices platform using Docker + EKS.
- [ ] Design a file-upload service using Spring Boot + S3.
- [ ] Design a globally available frontend using S3 + CloudFront.
- [ ] Design a secure application using VPC + IAM + Secrets Manager.
- [ ] Design a highly available PostgreSQL architecture using RDS.
- [ ] Design an application that can handle sudden traffic spikes.
- [ ] Design monitoring and alerting for a production microservices application.

---

# ⭐ Top 25 AWS Questions to Master First

If interview time is limited, **do these first**:

1. [ ] What is AWS Region vs Availability Zone?
2. [ ] EC2 and when to use it.
3. [ ] ECS vs EKS.
4. [ ] EC2 vs Lambda.
5. [ ] API Gateway and its role in microservices.
6. [ ] API Gateway vs ALB.
7. [ ] ALB and Target Groups.
8. [ ] RDS and why to use it.
9. [ ] Multi-AZ vs Read Replica.
10. [ ] RDS vs DynamoDB.
11. [ ] IAM User vs Role vs Policy.
12. [ ] Principle of Least Privilege.
13. [ ] VPC.
14. [ ] Public vs Private Subnet.
15. [ ] Security Group vs Network ACL.
16. [ ] Internet Gateway vs NAT Gateway.
17. [ ] Secrets Manager vs Parameter Store.
18. [ ] S3 and securing S3.
19. [ ] S3 + CloudFront architecture.
20. [ ] CloudWatch Logs/Metrics/Alarms.
21. [ ] How to troubleshoot high CPU on EC2.
22. [ ] How to troubleshoot 500/504 errors.
23. [ ] Docker + ECS/EKS deployment.
24. [ ] CI/CD pipeline for Spring Boot on AWS.
25. [ ] Design a highly available Spring Boot microservices application on AWS.

---

# 🎯 AWS Interview Preparation Rule

For every AWS service, prepare these **5 things**:

1. **What is it?**
2. **Why do we need it?**
3. **When would you use it?**
4. **What are the alternatives/trade-offs?**
5. **How would you use it in a Java/Spring Boot production architecture?**

> Do not memorize AWS definitions only.

> For Deloitte, be able to explain AWS services as part of a **real backend architecture**.