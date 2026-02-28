# Azure

### 📋 Common Azure Resources and Their Functionality

| Resource Name | Category | Short Description / Key Functionality |
| :--- | :--- | :--- |
| **Azure Virtual Machines** | Compute | IaaS service for creating and managing VMs (Windows/Linux) with full control over the OS and software . |
| **Azure App Service** | Compute | PaaS service for hosting web apps, REST APIs, and mobile back ends. Supports auto-scaling and multiple languages (.NET, Java, etc.) . |
| **Azure Functions** | Compute | Serverless compute service for running event-driven code without managing infrastructure. Pay only for execution time . |
| **Azure Kubernetes Service (AKS)** | Containers | Managed Kubernetes service for deploying and orchestrating containerized applications at scale . |
| **Azure Container Apps** | Containers | Serverless platform for running microservices and containerized apps, abstracting away Kubernetes complexity . |
| **Azure Virtual Network** | Networking | Fundamental building block for private networks in Azure, enabling secure communication between resources . |
| **Azure Load Balancer** | Networking | Layer-4 load balancer that distributes inbound traffic across healthy VM instances . |
| **Azure Application Gateway** | Networking | Layer-7 load balancer with SSL termination and Web Application Firewall (WAF) capabilities . |
| **Azure Blob Storage** | Storage | Object storage solution for massive amounts of unstructured data (images, videos, backups) . |
| **Azure Files** | Storage | Managed file shares accessible via SMB protocol, ideal for lift-and-shift migrations . |
| **Azure SQL Database** | Databases | Fully managed, intelligent PaaS offering of SQL Server. Handles updates, backups, and high availability . |
| **Azure Cosmos DB** | Databases | Globally distributed, multi-model NoSQL database with single-digit millisecond response times . |
| **Azure Cache for Redis** | Databases | Managed in-memory data store based on Redis, used to boost app performance and as a message broker . |
| **Azure Key Vault** | Security & Identity | Centralized cloud service for storing and managing application secrets, keys, and certificates securely . |
| **Microsoft Entra ID** (formerly Azure AD) | Security & Identity | Cloud-based identity and access management service, providing authentication and authorization . |
| **Azure Service Bus** | Integration | Fully managed enterprise message broker for decoupling applications via queues and pub/sub topics . |
| **Azure Logic Apps** | Integration | Low-code/no-code platform to automate workflows and integrate apps, data, and services across enterprises . |
| **Azure DevOps** | Developer Tools | Suite of services for planning, collaborating, and delivering code, including pipelines, repos, and boards . |
| **Azure Monitor** | Management & Governance | Comprehensive solution for collecting, analyzing, and acting on telemetry from cloud and on-premises environments . |
| **Azure AI Services** | AI + Machine Learning | Pre-built, ready-to-use APIs for adding AI capabilities like vision, speech, language, and decision-making to apps . |

### 🗺️ Navigating the Azure Landscape

Beyond individual services, understanding the management hierarchy is key to organizing and governing these resources effectively .

-   **Management Groups**: These sit at the top of the hierarchy and are used to manage access, policy, and compliance across multiple subscriptions. For example, you can apply a policy to a management group that limits the Azure regions where VMs can be created, and all subscriptions under that group will inherit it .
-   **Subscriptions**: An Azure subscription is both a billing unit and a boundary for access management. It logically organizes resource groups and helps separate environments like development, testing, and production for cost tracking or security purposes .
-   **Resource Groups**: These are containers that hold related resources for an Azure solution. Resources that share the same lifecycle (deployed, updated, and deleted together) should be in the same resource group. Deleting a resource group deletes all resources within it, which is useful for cleaning up test environments .
-   **Resources**: These are the manageable items or services available in Azure, such as the VMs, databases, and networks listed in the table above. Each resource must belong to a resource group .

### 💡 How to Use This Information

As you design solutions on Azure, you will combine these resources. For instance, to host a scalable web application, you might use **Azure App Service** for the application code, **Azure SQL Database** for relational data, **Azure Cache for Redis** for session state, and **Azure Front Door** for global load balancing . All these resources would be organized within a specific **resource group**, likely inside a subscription dedicated to "Production" workloads.

