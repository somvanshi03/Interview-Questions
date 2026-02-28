# AWS

### 📋 Common AWS Resources and Their Functionality

| Resource Name | Category | Short Description / Key Functionality |
| :--- | :--- | :--- |
| **Amazon EC2 (Elastic Compute Cloud)** | Compute | IaaS service providing secure, resizable virtual servers in the cloud. You have full control over the OS and software . |
| **AWS Lambda** | Compute | Serverless compute service that runs your code in response to events and automatically manages the underlying compute resources . |
| **AWS Elastic Beanstalk** | Compute | PaaS service for automatically deploying and scaling applications (Java, .NET, PHP, etc.) on familiar servers like Apache and IIS . |
| **Amazon ECS (Elastic Container Service)** | Containers | A fully managed container orchestration service that simplifies running and scaling containerized applications . |
| **Amazon EKS (Elastic Kubernetes Service)** | Containers | A managed Kubernetes service to run Kubernetes on AWS without needing to install and operate your own Kubernetes control plane . |
| **Amazon S3 (Simple Storage Service)** | Storage | Highly scalable, durable, and secure object storage for any type of data (backups, media, static assets). It is not a file system that can be mounted . |
| **Amazon EBS (Elastic Block Store)** | Storage | Provides persistent, block-level storage volumes for use with EC2 instances. It's like a virtual hard drive in the cloud . |
| **Amazon EFS (Elastic File System)** | Storage | A fully managed, scalable, and elastic Network File System (NFS) for use with AWS services and on-premises resources. It can be mounted on multiple EC2 instances simultaneously . |
| **Amazon S3 Glacier** | Storage | A secure, durable, and extremely low-cost storage service for data archiving and long-term backup . |
| **Amazon VPC (Virtual Private Cloud)** | Networking | Lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define . |
| **Amazon Route 53** | Networking | A scalable and highly available Domain Name System (DNS) web service. It translates domain names to IP addresses and can route traffic globally . |
| **Amazon CloudFront** | Networking | A fast global Content Delivery Network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency . |
| **Elastic Load Balancing (ELB)** | Networking | Automatically distributes incoming application traffic across multiple targets, such as EC2 instances, containers, and IP addresses, in one or more Availability Zones . |
| **Amazon RDS (Relational Database Service)** | Databases | A managed service that makes it easy to set up, operate, and scale a relational database in the cloud (supports engines like MySQL, PostgreSQL, SQL Server, etc.) . |
| **Amazon Aurora** | Databases | A MySQL and PostgreSQL-compatible relational database built for the cloud, combining the performance and availability of high-end commercial databases with the simplicity and cost-effectiveness of open-source databases . |
| **Amazon DynamoDB** | Databases | A fast and flexible NoSQL database service for any scale. It's a key-value and document database that delivers single-digit millisecond performance . |
| **Amazon ElastiCache** | Databases | A managed, in-memory caching service supporting Redis and Memcached. It helps improve the performance of web applications by allowing you to retrieve information from fast, in-memory caches . |
| **Amazon Redshift** | Databases | A fast, fully managed, petabyte-scale data warehouse service. It is designed for analytical processing (OLAP) . |
| **AWS IAM (Identity and Access Management)** | Security & Identity | A web service that helps you securely control access to AWS resources. It is used to manage users, groups, and permissions . |
| **AWS KMS (Key Management Service)** | Security & Identity | A managed service that makes it easy for you to create and control the encryption keys used to encrypt your data . |
| **AWS WAF (Web Application Firewall)** | Security & Identity | Helps protect your web applications from common web exploits that could affect application availability, compromise security, or consume excessive resources . |
| **Amazon GuardDuty** | Security & Identity | A threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts, workloads, and data . |
| **Amazon SQS (Simple Queue Service)** | Application Integration | A fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications . |
| **Amazon SNS (Simple Notification Service)** | Application Integration | A fully managed pub/sub messaging service for sending notifications (email, SMS, etc.) and messages to distributed services . |
| **Amazon API Gateway** | Application Integration | A fully managed service for creating, publishing, maintaining, monitoring, and securing REST, HTTP, and WebSocket APIs at any scale . |
| **AWS CloudFormation** | Management & Governance | An Infrastructure as Code (IaC) service that allows you to model and provision AWS resources using templates, so you can manage infrastructure in a declarative and repeatable way . |
| **Amazon CloudWatch** | Management & Governance | A monitoring and observability service for AWS resources and applications. It collects and tracks metrics, collects and monitors log files, and sets alarms . |
| **AWS CloudTrail** | Management & Governance | A service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. It logs every API call made in the account . |
| **AWS Trusted Advisor** | Management & Governance | An online tool that inspects your AWS environment and makes recommendations for saving money, improving system performance, and closing security gaps . |

### 🗺️ The AWS Global Infrastructure

When designing with these services, it's also important to understand the foundational concepts of the AWS Global Infrastructure :

*   **Regions**: These are geographical areas (e.g., US East, EU Ireland) where AWS has multiple data centers. You choose a region to deploy your resources based on data sovereignty laws and latency to users.
*   **Availability Zones (AZs)**: Each region consists of multiple, isolated locations known as Availability Zones. Each AZ has independent power, cooling, and networking. By deploying your resources across multiple AZs, you can build highly available and fault-tolerant applications.
*   **Edge Locations**: These are a global network of sites used by CloudFront to cache copies of your content closer to your end-users, dramatically reducing latency for content delivery.

### 💡 How to Use This Information

As an architect, you will combine these resources to build solutions. For example, to host a scalable web application, you might use **EC2** instances or **Lambda** functions for compute, set up a **VPC** for networking, use **ELB** to distribute traffic, store data in **RDS** and static files in **S3**, and manage it all with **CloudFormation** templates .

I hope this curated list provides a solid foundation for your AWS learning. Are there any specific categories, like networking or security, you would like to explore in more detail?