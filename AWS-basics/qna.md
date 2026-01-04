# Question related to AWS Basics

## Q1. What is Cloud Computing?

**Answer:**

Cloud computing is the on-demand delivery of computing resources such as servers, storage, databases, networking, and software over the internet. Instead of owning and maintaining physical infrastructure, users can provision resources instantly and pay only for what they use.

Cloud computing enables scalability, high availability, and faster development by shifting infrastructure management to cloud service providers.

**Example / Analogy:**
Cloud computing is like using electricity from the power grid instead of running your own generator—you consume what you need, scale easily, and don’t worry about maintenance.

---

## Q2. Why is Cloud Computing better than On-Premise Infrastructure?

**Answer:**

Cloud computing is better than on-premise infrastructure because it offers greater scalability, cost efficiency, and operational flexibility.

In on-premise systems, organizations must invest upfront in hardware, manage maintenance, and plan capacity in advance. In contrast, cloud systems allow resources to be scaled up or down instantly, reduce capital expenditure, and improve reliability through managed services and global data centers.

However, cloud computing also introduces challenges such as vendor lock-in, latency, and security configuration, which engineers must carefully design around.

---

## Q3: Types of Cloud Services

- **IaaS (Infrastructure as a Service):** Virtual machines, storage, and networking  
- **PaaS (Platform as a Service):** Platform to deploy applications without managing servers  
- **SaaS (Software as a Service):** Fully managed applications like email or document tools

---

## Q4. What is a Region?

**Answer:**

A **Region** is a geographically distinct area where a cloud provider operates data centers.  
Each region is independent and designed to isolate failures from other regions.

Regions allow organizations to:

- Deploy applications closer to users (lower latency)
- Meet data residency and compliance requirements
- Design disaster recovery across regions

**Example:**

- `us-east-1` (North Virginia)
- `asia-south1` (Mumbai)

## Q5. What is an Availability Zone (AZ)?

**Answer:**

An **Availability Zone** is an isolated data center (or group of data centres) within a region.  
Each AZ has independent power, cooling, and networking but is connected to other AZs in the same region via low-latency, high-speed links.

Availability Zones are used to:

- Achieve high availability
- Design fault-tolerant systems
- Prevent single points of failure

**Example:**

- `us-east-1a`, `us-east-1b`, `us-east-1c`

**Best Practice:**
Production systems are deployed across **multiple AZs** within the same region.

---

## Q6. What is an Edge Location?

**Answer:**

An **Edge Location** is a geographically distributed data center used to deliver content closer to end users.  
Edge locations primarily support content delivery, caching, and request routing.

They are commonly used for:

- Serving static content (images, videos, JS, CSS)
- Reducing latency
- Improving application performance globally

Edge locations are part of services like **CDNs (Content Delivery Networks)**.

---

## Q7 Why Does AWS Use Multiple Availability Zones (AZs)?

## Answer

AWS uses multiple **Availability Zones (AZs)** within a region to provide **high availability, fault tolerance, and reliability** for applications.

Each Availability Zone is an isolated data center (or group of data centers) with independent power, cooling, and networking. This isolation ensures that a failure in one AZ does not impact others.

By distributing applications across multiple AZs, AWS enables systems to continue operating even if one AZ experiences an outage.

---

## Key Reasons AWS Uses Multiple AZs

### 1. High Availability

Deploying applications across multiple AZs ensures services remain accessible even if one AZ fails.

### 2. Fault Isolation

AZs are physically separated to prevent failures caused by power outages, hardware faults, or natural disasters from spreading.

### 3. Disaster Recovery

Multi-AZ architectures reduce downtime and data loss, enabling fast recovery without requiring cross-region failover.

### 4. Scalability and Load Distribution

Traffic can be balanced across AZs, allowing applications to scale horizontally and handle higher loads efficiently.

### 5. Maintenance Without Downtime

AWS can perform maintenance on infrastructure in one AZ while applications continue running in other AZs.

---

## Example Scenario

If an application runs only in one AZ and that AZ goes down, the entire application becomes unavailable.  
If the same application runs across two or more AZs, traffic is automatically routed to healthy AZs, ensuring uninterrupted service.

---

## Key Takeaway

Multiple Availability Zones allow AWS to deliver highly available, fault-tolerant, and resilient cloud infrastructure, which is critical for running production-grade applications.

## Q8 What is IAM?

**IAM (Identity and Access Management)** is a cloud service that allows you to securely control **who can access what resources** in your cloud environment.

With IAM, you define:

- **Identities** (users, roles, services)
- **Permissions** (what actions they can perform)
- **Policies** (rules that grant or deny access)

IAM ensures that only authorized entities can access specific cloud resources.

---

## Q9 Why is IAM Important?

### 1. Security

IAM prevents unauthorized access to cloud resources by enforcing authentication and authorization rules.

### 2. Least Privilege Access

IAM allows you to grant only the minimum permissions required to perform a task, reducing the attack surface.

### 3. Centralized Access Control

All permissions are managed from a single place, making access management consistent and auditable.

### 4. Scalability

IAM scales easily as users, services, and applications grow, without manual permission handling.

### 5. Compliance and Auditing

IAM enables logging and tracking of access, helping meet compliance and regulatory requirements.

---

## Core IAM Components

- **Users:** Individual human identities
- **Roles:** Temporary permissions assumed by users or services
- **Policies:** JSON-based rules defining allowed or denied actions
- **Groups:** Collections of users with shared permissions

---

## Example Scenario

An application running on a cloud server needs access to a database.  
Instead of storing credentials in code, the application assumes an IAM role with limited permissions, ensuring secure and temporary access.

---

## Key Takeaway

IAM is critical for securing cloud environments by ensuring the right people and services have the right level of access at the right time.
