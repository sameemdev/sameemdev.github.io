---
layout: post
title:  "Azure Fundementals"
date:   2025-10-02
categories: [Azure, m365]
tags: [AZ-900, azure-ad, m365]
description: "Microsoft Azure Fundementals learning material. AZ-900 prepp-material"
---

Azure Fundamentals Summary (AZ-900)

Cloud services and cloud computing
Cloud computing utilizes remote servers instead of on-premise infrastructure. It's in high demand due to its cost-effectiveness, security, and 24/7 availability. Major providers like Azure, Amazon, and Google offer a range of services including computing power, storage, AI, and networking.
Shared Responsibility between CSP and Consumer
In cloud computing, there's a shared responsibility model between the Cloud Service Provider (CSP) and the consumer. The CSP handles physical security and infrastructure, while the consumer manages data processing, access control, and configurations within the cloud services. This model ensures both parties contribute to maintaining the security and functionality of the cloud environment.
 
Types of cloud computing
Software as a service (SaaS): is a product that is run and managed by service provider. SaaS is really for customers. Example of SaaS would be office 365, gmail, skype for company and more which run in the cloud. 
Platform as a Service (PaaS): Focuses on the development and management of your apps and is actually for developers who build applications. You do not need to worry about provisioning, hardware or OS for your app to run on. Exampled would be Azure app service, google app engine or Heroku which is used for hosting web applications. PaaS supports entire web application lifecycle from building, deploying, maintaining and updating. 
Infrastructure as a Service (IaaS): The basic building block for cloud IT. This is provided by cloud platform providers and provide almost every IT service such as networking, storage, security, AI and computing power. Example of IaaS would be Azure, Amazon, GCP and more. 
Software as a Service is running on top of the Platform as a Service and Platform as a Service itself is running on top of the Infrastructure as a Service. So SaaS > PaaS > IaaS. 

Cloud deployment models: 
Public cloud: Everything built on the cloud provider platform. It is also known as native-cloud and is accessed through the internet. 
Private cloud: Everything built on on-premise (locally in companies datacenter). Can use some open source cloud solutions such as open stack.  Biggest advantage with private cloud or local cloud is that you have full control of your infrastructure. 
Hybrid cloud: A combination of both private and public cloud.

Azure Architecture
Azure architecture consists of two parts, Physical infrastructure and management infrastructure.
Physical infrastructure: is the azure datacenters that are spread around the world. These datacenters are not directly accessible because they are grouped together into azure regions and azure availability zones to provide resiliency and reliability. 
Azure Regions: is a geographical area on the planet that contains at least one but often several datacenters that are nearby (same region) and networked together. When you create an azure resource, you will often need to choose the region where you want your resource to be deployed. 
Azure Availability Zones:  Are physically separate datacenters within an azure region. Each availability zone consists of one or more datacenters that are equipped with independent power, cooling, and networking (so every availability zone has their own network, power and cooling resources). An availability zone is set up to be an isolation boundary so if one zone goes down, the other continues working. Azure availability zones are connected through high-speed private fiber optic networks.  There are at least three availability zones in an azure region that’s why azure stores three copies of your data for redundancy. However, not all azure regions support availability zones. So Azure availability zones are great for mission critical applications where you’ll one availability zone for the deployment and others for backup (replication). 
Availability zones are primarily for virtual machines, managed disks, load balancers, and SQL databases
Region pairs: Availability zones ensure redundancy at the zone level, meaning if one datacenter fails, others continue working seamlessly, preventing disruptions and data loss for end users. However, in the event of broader interruptions like natural disasters or civil unrest (war) affecting an entire region, no single availability zone can serve as a backup because all zones within that region may be impacted simultaneously. In such cases, Azure provides region pairs, allowing operations to fail over to another region, ensuring continuity. In summary, availability zones offer zone-level redundancy, while region pairs provide backup and redundancy at the region level.

Accessing azure resources and services
To create and manage Azure resources and services you can either use Azure portal which is a web based portal at portal.azure.com. You can also use Azure CLI, PowerShell or SDKs. s

Azure Cloud Shell: is a browser-based shell accessible within Azure portal for managing Azure resources using either PowerShell or Bash. Azure cloud shell is running on top of the Azure CLI.
Azure CLI: is a cross-platform command-line tool for managing Azure Resources. Azure CLI is available on Windows, MacOS and Linux using commands written in Python. Azure CLI is running under the cloud shell. 
Azure Powershell: Azure resources could also be managed by using ready to use PowerShell modules. It gives more flexibility then the Azure CLI. 
Azure Resource Manager (ARM):  
Whenever you create, delete or update azure resources they would be handled by the Azure Resource Manager in the backend regardless of whatever method you use for example if it is azure portal, azure command-line, Cloudshell and more.    
Azure resources and workloads: Resources are single components in Azure such as databases, networking resources, virtual machines and more whereas workloads are a specific task or application that runs on Azure such as a web application running on Azure is workload or an AI model running on Azure is a workload.

Azure resource health and status
Azure Advisor: Is a feature in Azure which offers you actionable recommendations about security, reliability, operational excellence, performance, and cost for your Azure resources. It recommends Azure best practices for your Azure workloads. 
Azure Service Health: inform us about outages or planned maintenance on Azure Services that we are using.
Azure Monitoring: inform us about how our application performs and provides us with information to identify and track issues inside our app and take actions upon it. 
Azure Monitor is a platform that collects metric and logging data, such as CPU percentages.

Important Cloud Terms: 
1.	Availability: high availability is the core of the cloud computing which means that resources and services are available all the time ensuring that they are consistently accessible and operational when needed. 
2.	Elasticity: means scalability in cloud computing both scaling up when more resources are needed and scaling down when some resources are no longer needed. For example, adding or removing VMs and other resources. There are two types of scalabilities in cloud computing namely horizontal and vertical. 
Horizontal Scalability means adding more cloud resources such as VMs. 
Vertical Scalability means adding more computing power such as RAM, CPU, storage and more to already existing resources. For example, adding more RAM to existing VMs. 
3.	Reliability: means fault tolerance and disaster recovery of cloud workloads. 

4.	Resilience: means that ability of a system to recover from failure and continue function normally for example cyber resilience m eans that systems are able to operate normally even after being hit by cyber-attack. 

5.	Predictability: means predictable performance and costs. For example, you know in advance that your cloud workloads are auto-scaled, load-balanced and always available when needed. And you also know specifically in advance that how much cloud resources are going to cost you while using those resources, so that there is no cost surprises or hesitations. Azure provides a clear view of how much every cloud resource costs, so you can always make an accurate price calculation from the point.

-	Governance in Cloud means regulatory requirements and audits for compliance.   

Economy of Cloud computing: 
1.	Capital Expenditure (Capex): is buying hardware outright, paid upfront as one time purchase. Such as buying physical servers for the corporate which you only pay once for. 
2.	Operational Expenditure (OpEx): is ongoing costs needed to run your business. Such as electricity and monthly costs for using cloud computing.   
3.	Consumption-based Pricing: is based on pay-as-you-go basis where you pay only for what you use.  

Serverless (Azure Functions):
Serverless doesn’t mean that there are no servers involved but rather you do not need to manage any servers to deploy, maintain and run your application, you just need to write the  code and that’s it. Azure Functions is a great example of serverless computing. Serverless is even more flexible than PaaS but PaaS (Platform as a service) gives more control to the developer to choose what to do with managing their applications. PaaS using azure app service  is a great fit for a full-fledged web applications  whereas serverless is great for lightweight applications such as serverless API endpoints for third-party applications, AI Chatbots, scheduled tasks and background processing and more. 
Azure Marketplace: is like an Appstore for azure resources where you can install other resources for your workloads and bring them into your subscription. 
Resource Groups: Every azure resource belongs to a resource group. A resource group is a logical container which contains one or several related azure resources. Azure resource groups exists to simplify resource management, deployment, billing and security in terms of access control to related resources living inside. For example, a web server, database server, VMs and more living in a single resource group. 
A resource can only be placed in one resource group, and you cannot put one resource group into another so they cannot be nested. Resource groups provide a convenient way to group together cloud resources. If apply some settings to resource group, then those settings are applied to all resources within that resource group. For example, if you grant access/deny rules to a resource then you have granted access/deny rules to every resource in that resource group. 
Furthermore, if you delete a resource then all resources in that resource group will be deleted. For example, you can create a testing resource group to do tests and labs when you are done with your testing then you can simply delete the resource group and which means that all resources in that testing resource group will be automatically deleted. 

Scale Sets: Scale Sets in Azure allow for automatic scaling of virtual machines (VMs) based on predefined criteria such as CPU usage, memory consumption, or custom metrics. When the workload requires more resources (meaning running out of memory, CPU and etc), Azure will automatically add new VM instances to handle the increased demand. Conversely, if the demand decreases, Azure will scale down the number of VM instances to conserve resources and reduce costs. This dynamic scaling ensures that your application can efficiently handle varying levels of traffic or workload without manual intervention, thereby maintaining availability and optimizing resource utilization. Scale sets don’t have any additional costs so you only pay for what you use on Azure. 

Application Gateway: is a higher-level load balancer for internet traffic. A normal load balancer distributes inbound internet traffic based on IP and Port to the backend resources while an application Gateway can distribute incoming traffic on additional attributes such as URI path (web address) and host headers (Requested data). For example, application gateway will forward incoming http requests for images https://.../images to specific servers which handle the load while distributing other requests to other servers. 
Azure Storage: is Microsoft cloud-based storage solution that is highly scalable, durable and reliable storage. Azure normally keeps three copies of your data for redundancy purposes so that the data is available even if it fails in one location. Azure offers several storage solutions such as Blobs, File Storage, Dis Storage, Queue Storage and more. 
Blob Storage: is used to store massive amounts of unstructured data in the cloud such as text or binary data (video, audio) and more. A storage account has to be created first to store data in blobs (containers). 
Disk Storage: is used to provide cloud-based block storage for virtual machines running in cloud. 
File Storage: is used to provide storage for file shares. 
Azure ARC: If you have a multi-cloud environment such as cloud services from different cloud providers for example Amazon web services and azure then you can use Azure Arc to facilitate the user of cloud services between different cloud providers. Even if you use hybrid clouds meaning private and public clouds then you can use Azure Arc to felicitate the interaction between private and public clouds. 
Azure Interactive: auto-completes the commands you type. It makes resource management a lot easier. 

Sovereign Regions: In addition to regular regions Azure also has sovereign regions. Sovereign regions are fully isolated from the main Azure instance. They provide enhanced control over data and workloads, particularly for compliance and legal requirements. Some governments already use sovereign regions for this reason, as they offer greater isolation and control compared to regular Azure regions. 

Azure Management Groups: With Azure Management Groups you can manage access, policies and compliance for multiple subscriptions at the same time and in a centralized and comfortable way. If you have a single subscription then you can apply policies, compliance and manage access to it directly at the subscription level but if you have multiple subscriptions which could be in multiple geographies then you will need Azure Management Groups to manage those subscriptions. 

Azure resources live inside Resource Groups and Resource Groups live inside Subscriptions and multiple subscriptions live inside Azure Management Groups. Azure lets you manage access and apply policies and compliance to your resources in each hierarchical layer. For example, you can manage access to resources in a resource group, subscriptions, and Azure management groups. Meaning if you have multiple resource groups then you can manage those in subscriptions and if you have multiple subscriptions then you can manage them in Azure Management Groups. 

Roll Based Access Control (RBAC) vs Conditional Access (CA): RBAC focuses on controlling access to Azure resources based on assigned roles and permissions, while Conditional Access focuses on enforcing access policies such as MFA, device compliance, specific location and so on based on contextual factors such as user, device, and environment. While RBAC governs who can perform what actions on Azure resources, Conditional Access governs under what conditions access to those resources is allowed. They can be used together to provide comprehensive access control and security for your infrastructure. 

Azure Virtual Desktops vs Azure VMs: 
Azure Virtual Machines are VMs created and running in the cloud and fulfil diverse needs like web hosting and big data processing, databases and more and could be created using different operating systems like Windows and Linux. 
Azure Virtual Desktop which is a Microsoft VDI (Virtual Desktop Infrastructure) solution provides fully managed Windows 10 virtual desktops (meaning a fully functional and ready windows computer) accessible from anywhere, catering to scenarios where a user needs a fully functional windows computer like remote work and distance learning that demand dedicated, centralized desktop environments.

Azure VMs vs Azure Containers: 
companies use containers because they are lightweight, agile, scalable, and resource-efficient deployment of modern, cloud-native applications, particularly in microservices architectures. Containers are often used for application testing where you need to test an application on different systems because they are more robust and resource efficient. Containers share the same operating system. An example of containers is Docker and with Azure containers you can create fully managed containers offered through PaaS. 
On the other hand, virtual machines are preferred for running legacy applications, stateful workloads, and scenarios where stronger isolation, security and full control over the environment are necessary. VMs do not share the same operating system but are rather different and fully isolated systems with their own OS kernel. VMs are mainly used for production applications.
Many companies use a combination of containers and VMs to leverage the strengths of each approach based on their specific use cases and requirements.

Azure Kubernetes Service (AKS): Azure Kubernetes Service is a container orchestration service. A container orchestration service is used to manage the lifecycle of containers. When you deploy multiple containers, AKS makes the management of those containers a lot easier and efficient.
Microservice Architecture: containers are very often used to test and deploy microservices. Microservice architecture is where you break a solution into multiple smaller and independent pieces. For example, your company needs to build a web application so using Microservices architecture you will split the web application into a container hosting the frontend, another container hosting the backend and third container hosting the database. This split allows you to separate portions of your app into logical sections that can be maintained, scaled, or updated independently which means that you scale or update each component anytime without affecting the other components. 

Azure Virtual Networking
Azure Virtual Networking is the underline networking infrastructure for Azure resources for example when you create your azure resources and workloads they will need networking so that you can privately (via VPN) or publicly (via internet) access them. Azure virtual networking is used to make your resources to be able to communicate with each other in a secure and isolated way. 
Key components of Azure virtual networking include Virtual Networks (VNets) for segmentation, Subnets for resource organization, Network Security Groups (NSGs) for traffic control, Virtual Network Peering for inter-VNet connectivity, VPN Gateway and ExpressRoute for hybrid  (on Prem to cloud) connectivity, and Azure Load Balancer for traffic distribution. These features enable you to design complex network architectures, ensuring secure and efficient communication between Azure resources and on-premises networks.
Virtual Network Peering: You can link virtual networks together by using virtual network peering. Peering enables resources in each virtual network to communicate with each other.
For example if you  need to allow resources on two different Azure virtual networks to communicate with each other you must use peering on azure. 
Service endpoints are used to expose Azure services to a virtual network, providing communication between the two. ExpressRoute is used to connect an on-premises network to Azure. NSGs allow you to configure inbound and outbound rules for virtual networks and virtual machines. Peering allows you to connect virtual networks together.
Azure Reservations offers discounted prices on certain Azure services. Azure Reservations can save you up to 72 percent compared to pay-as-you-go prices

Azure Storage Redundancy: 
Azure storage always stores at least three copies of your data in different locations based on the redundancy storage subscription you have on Azure. Azure provides the following redundancy storage options for your data. Choosing the right one is always a trade-off between costs and availability. Critical applications may need the highest redundant storage whereas trivial applications may just need the least storage redundancy such as LRS. 
1. Locally Redundant Storage (LRS): Data is replicated synchronously within a single datacentre to ensure high durability and availability. It protects against hardware failures within the datacentre.
2. Zone-Redundant Storage (ZRS): Data is replicated synchronously across multiple availability zones within a region to protect against datacentre-level failures. It provides higher resilience than LRS.
3. Geo-Redundant Storage (GRS): Data is replicated asynchronously to a paired region, ensuring data durability and availability even in the event of a regional disaster. It offers redundancy across regions for disaster recovery.
4. Geo-Zone-Redundant Storage (GZRS): Combines the features of ZRS and GRS, providing synchronous replication across availability zones within a region and asynchronous replication to a paired region for disaster recovery. It offers the highest level of redundancy and resilience.
Azure data migration options

Data migration means migrating data from on-prem infrastructure to Clouds, vice versa or between cloud providers. Azure supports both real-time migration of infrastructure, applications, and data using Azure Migrate and as well as offline migration of data using Azure Data Box. 
Azure Migrate includes several components:
Discovery and Assessment: prior to data being migrated this component discovers and assesses servers running on on-prem VM-ware, Hyper-V or physical servers. 
Server Migration: Migrate VMware VMs, Hyper-V VMs, physical servers, other virtualized servers and public cloud VMs to Azure. 
Data migration Assistant: this is a stand-alone tool to assess SQL servers. It helps identify potential problems blocking migration. 
Azure Database Migration Service: is  used to migrate on-prem databases to Azure VMs running SQL server, Azure SQL Database or SQL Managed Instances. 
Azure App Service Migration Assistant: helps assessing on-prem websites using .NET and PHP for migration to Azure App Service. 

Azure Data Box. Use Azure Data Box products to move large amounts (80 TB) of offline data. Azure Data Box is ideally suited to transfer data sizes larger than 40 terabytes with no or limited network connectivity. 

Despite large scale migration services Azure provides like Azure Migrate and Azure Data Box, Azure also provides tools that help you move individual files or small file groups. These tools for moving or copying very small amount of data are: AzCopy, Azure Storage Explorer and Azure File Sync. 

1.	AzCopy: Command-line utility for copying blobs or files to/from Azure storage, supporting various tasks like upload, download, and synchronization.

2.	Azure Storage Explorer: Graphical interface to manage files and blobs in Azure Storage Accounts, available on Windows, macOS, and Linux, utilizing AzCopy for backend operations.

3.	Azure File Sync: Synchronizes local Windows servers with Azure Files, creating bidirectional sync for enhanced flexibility and accessibility.

Hybrid Identity Infrastructure: means when organizations have both on-prem active directory and cloud-based (Entra ID) at the same time.  Hybrid Identity is used to create a common user identity for authentication and authorization to all resources, regardless of location. 
To keep the on-prem Active directory updated and in sync with Entra ID we can use AD Connect. For example, using AD Connect we can use  Single Sign-Ons, MFA, self password resets and more on the same user regardless of the location whether it is on-prem or cloud. 

Entra ID managed domain Services: Domain services is a core part of active directory such as GPO, authentication, authorization, trust-relationship, replication and more. On of the best things with Entra ID (cloud-based AD) is that when managing domain services, you do not need to configure a domain controller by yourself, Azure takes care of it. So, when creating GPO and other domain services in Entra ID, Azure will deploy windows servers automatically and take care of their deployment, management and patching itself so you do not have to worry about that. This is called managed domain services since Azure takes care of the management. 
All information is then synchronized using AD Connect (Entra Connect). Otherwise, there will be one-way synchronization from Entra ID to Microsoft Entra Domain Services and not vice versa if AD connect is not used. 

Authentication and Authorization:
Single Sign-on (SSO): means when the user sign-ins one time and then gets authenticated across all services and resources. So when the user later on sign-ins the user will not need to enter their password because SSO will sign-in them automatically. The security here is as strong as the initial (first time) authentication. It provides great convenience. 
Multifactor Authentication (MFA): means when the user is required to perform an extra step to get authenticated. It improves security to an incredible extent but may be reduce convenience too because the user has to be providing that extra step every time they sign-in.  
MFA falls into three categories:

1.	Something the user knows – this might be a challenge question (such as where you grew up).
2.	Something the user has – this might be a code that's sent to the user's mobile phone.
3.	Something the user is – this is typically some sort of biometric property, such as a fingerprint or face scan.


Passwordless Authentication means when you do not need to enter a password at all. 
Passwordless authentication methods are more convenient because the password is removed and replaced with something you have, plus something you are, or something you know. Such as Facial recognition, PIN, fingerprints and more instead of passwords. 
For example using device + Pin to provide Passwordless. When a user device is enrolled in Entra ID, it then obtains some trust and along with PIN or device password the user can sign-in to every application and service without entering a password. Because that device is already registered and trusted and along with the device pin/password the authentication is trusted. However, Passwordless is often used with MFA and SSO to provide both connivence and enterprise-level security. 

Azure external identities: An external identity is a person, device, service, etc. that is outside your organization. Microsoft Entra External ID refers to all the ways you can securely interact with users outside of your organization such as third party users, suppliers, collaborators and more. 

Defense-in-depth: means securing users, devices and services at each layer. These layers are:

1.	Physical Security: securing physical hardware and datacentres.
2.	Identity & Access: Securing identities (users, devices, and services) through MFA, SSO, complex passwords and more.
3.	Perimeter: Protecting against DDoS to filter large scale attacks before they can cause a business disruption. 
4.	Network Layer: Limits communication through resources through access control and segmentation. 
5.	Compute layer: secure access to virtual machines
6.	Application layer: secure applications so that they are free of security vulnerabilities. 
7.	Data layer: Control access to business and customer data (storage). 

Azure pricing and costs
Azure provides two ways to estimate costs and pricing for using its cloud products and services. These two tools are Azure Pricing Calculator and Azure Total Cost of Ownership Calculator (TCO calculator). 

Azure Pricing Calculator: is to used to give you an estimated cost of provisioning resources including compute, storage and associated network costs. The pricing calculator is a web-based tool which can be used as an example scenario to see an estimate of the Azure spend. For example, the customer wants to deploy a web-application on Azure and wants to know how much it would cost in total.  so you would add A virtual machine, database, and webserver to azure pricing calculator to see how much deploying a web application will cost for the customer on Azure. Using Azure Pricing Calculator is totally free. 

Total Cost of Ownership Calculator (TCO Calculator): is also a web-based tool which is used to compare how much your current on-prem infrastructure would cost if you move to Azure. With the TCO calculator, you enter your current infrastructure configuration, including servers, databases, storage, and outbound network traffic. The TCO calculator then compares the anticipated costs for your current environment with an Azure environment supporting the same infrastructure requirements. TCO calculator is used when a customer wants to move their infrastructure to the cloud and wants to know the cost of running their on-prem infrastructure in the cloud. 

Azure Cost Management is a set of tools by Azure which you can use to monitor and track your Azure spendings and costs. For example, you can set up thresholds when a certain cost is exceeded an alert will be generated letting you know that you have surpassed your budged threshold.  It's essential when you want to monitor and control your Azure expenses, set budgets, identify cost-saving opportunities, and ensure efficient resource utilization. Alert could be of type budget alert when it is surpassed or Azure Credit alert or department quota alert (department spending reaches a fixed threshold). 
Resource Tags: One way of organizing and easily managing your related Azure resources is using resource groups, subscriptions, and management groups and the second way is using resource tags.  Resource tags for your resources helps you stay organized and track usage based on metadata associated with the resources. Because then you can easily apply different policies and other management rules on your resources using resource tags as well.
For example, you may wanna tag all production servers as prod or test servers as test. Or you may wanna tag critical servers such as domain controllers as critical and so on.  

Microsoft Purview: 
Microsoft Purview is a family of data governance, risk, and compliance solutions that helps you get a single and unified view into your data and stay compliant. It can help with 
-	Automated data discovery
-	Sensitive data classification
-	End-to-end data lineage (tracking data from source to destination)
Resource locks: In order to avoid accidental deletion or changes to resources we can use resource locks. Resource lock will make it impossible to delete or change resources while locked. Such locks can be applied to resources, resource groups, subscriptions and so on. There are two types of locks. One preventing against deletion and one preventing against changing a resource (even called a read-only lock). 
When a resource is locked not even the resource owner can either delete or change the resource, so they must first remove the lock and then make changes or delete the resource. When a resource is locked, you cannot even create a new resource. 

Azure Policy: can help you prevent creation of non-compliant resources, without having to manually evaluate each resource.

Infrastructure as a code: 
Is a concept where you manage your infrastructure by using scripts and templates in the command-line. Azure PowerShell, Azure CLI and Azure Cloudshell are all examples of infrastructure as a code. It means that you can configure and manage the entire infrastructure using code and scripts in the command-line which is a great way of effectively managing cloud resources and workloads. For example, if you want to create 50 virtual machines you can use the scripts or templates to create all the 50 virtual machines at the same time rather than creating each at a time. 
ARM templates and Bicep are two examples of using infrastructure as code to maintain your environment.
ARM Templates are Json files which can be used to deploy and manage Azure resources using templates in a declarative manner. Declarative syntax means you declare what you want to deploy but don’t need to write the actual programming commands and sequence to deploy the resources. With the help of ARM templates, we can deploy and manage a large number of resources and workloads at the same time very efficiently. 

Bicep: does the same work as ARM templates meaning creating and managing cloud resources through templates and scripts. However, Bicep has more readable and maintainable syntax compared to JSON, making it easier to author and manage infrastructure as code.
