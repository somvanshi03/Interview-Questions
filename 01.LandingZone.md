# Landing Zone 

A landing zone is a pre-configured, secure, and scalable foundation in a cloud environment (like Azure, AWS, or GCP) designed to host your workloads. Think of it as a "starter kit" or a "blueprint" for your cloud, built according to the provider's best practices, which ensures your applications are deployed in a well-architected and governed manner from day one .

While the core concept is the same across providers, the implementation and terminology have slight variations.

### 🏗️ The Core Concept: A Well-Structured Foundation

At its heart, a landing zone solves the common challenge of cloud adoption at scale: how to move from a single, simple account to a complex, secure, and manageable multi-account or multi-subscription environment. It provides:

*   **A Starting Point**: It's the initial environment from which you can quickly and confidently launch new workloads .
*   **Best Practices Built-in**: It incorporates a cloud provider's recommendations for security, networking, identity, and governance .
*   **Scalability and Modularity**: It's designed to grow with your organization. You can start with the essentials and add more components as your needs evolve .
*   **Separation of Concerns**: It typically separates the infrastructure that runs *applications* from the infrastructure that provides *shared services* (like security and networking) .

This last point is crucial. A landing zone often distinguishes between:
*   **Platform Landing Zone**: A central environment (often a dedicated subscription or account) that provides shared services like identity management, network connectivity (hub VPC/VNet), and centralized logging for all other environments .
*   **Application Landing Zones**: Individual, secure environments (subscriptions or accounts) where you deploy your specific applications and workloads. These connect to and leverage the services from the platform landing zone .

### ☁️ How Each Cloud Provider Implements Landing Zones

Here is a comparison of how the three major cloud providers approach landing zones:

| Feature | **Microsoft Azure** | **Amazon Web Services (AWS)** | **Google Cloud Platform (GCP)** |
| :--- | :--- | :--- | :--- |
| **Core Definition** | A multi-subscription environment that follows key design principles across eight design areas to enable application migration, modernization, and innovation at scale . | A well-architected, multi-account environment that is scalable and secure, serving as a starting point to deploy workloads . | A modular and scalable configuration (also called a cloud foundation) that enables organizations to adopt Google Cloud for their business needs . |
| **Key Components & Structure** | Built around **Management Groups** for governance, with a clear separation of **Platform** and **Application** subscriptions. Key design areas include identity, resource organization, and network topology . | Based on a multi-account strategy using **AWS Organizations**. Core accounts include **Management**, **Log Archive**, and **Audit**. Often uses a "hub-and-spoke" VPC model . | Centers on the **Resource Hierarchy** (Organization -> Folders -> Projects). Key elements include **Shared VPCs**, **Cloud Identity**, and organization policies for security . |
| **Primary Deployment Tool / Managed Service** | **Azure Landing Zone Accelerators** (Infrastructure as Code via Portal, ARM, Bicep, or Terraform) . | **AWS Control Tower** (a managed service that automates landing zone setup) . For more complex needs, the **Landing Zone Accelerator on AWS** is available . | **Enterprise Foundation Blueprint** (an opinionated Terraform example) and the **Setup Guide** in the Google Cloud console . |
| **Key Benefits of Using One** | Provides a repeatable, predictable method to apply a templatized implementation with baked-in security and governance best practices . | Simplifies the complex task of setting up a multi-account environment. It automates the setup of core accounts, security baselines, and applies "guardrails" for compliance . | Provides a dynamic foundation that grows as you adopt more workloads. It's designed to be secure and includes tools for governing internal cost distribution . |

In short, while the terminology and specific services differ (e.g., AWS "accounts" vs. Azure "subscriptions"), the purpose is identical: to provide a robust, secure, and scalable foundation for your cloud journey.

