[BrightSpace](https://brightspace.algonquincollege.com/d2l/home/825142)
### Week 1

Core components of cloud solution architecture (Basic):
- Front end (client)
- Back end (Server/storage)
- Cloud base delivery 
- Network
 Core Components breakdown:
 1. Client Infrastructure
 2. Application
 3. Service:
	 1. SAAS : Software as a Service
	 2. PAAS : Platform as a Service
	 3. IAAS : Infrastructure as a Service
4. Runtime Cloud: execution and runtime env to VM
5. Storage: store and manage data
6. Infrastructure: host, network and application level (hardware and software)
7. Management: Manages apps, services, runtime cloud, storage, infa and other security
8. Security: implementing different security and recovery measures

![[Pasted image 20250903205017.png]]
##### Infrastructure as a Service (IaaS):
- IaaS is basically the process of renting a data center from a cloud provider.  
- IaaS is not the service model of choice to accomplish a digital transformation, but there are couple of scenarios that we can tackle with IaaS:  
	- The lift-and-shift of existing workloads to the cloud.  
	- IaaS is a good alternative for smaller companies that can’t invest in their own data center.  
- In the context of a disaster recovery strategy, when adding a cloud-based data center to your existing on-premises servers.  
	- To speed up the time to market, providing some legacy practices and processes were adjusted upfront to align with the cloud delivery model.

##### Platform as a Service (PAAS):
- fully managed serviced model that helps you build solutions

##### Software as a Service (SaaS)
- Fully managed business suite of software (ZOHO, Google web Software)

##### Benefits of Cloud Architecture
- Elimination of the capital expenditure involved in using an on-premise server, storage, and networking infrastructure
- Cloud architecture allows organizations to shift their IT resources to the public cloud.  
- Cloud solves latency issues and improves data processing requirements  
- Cloud helps businesses to easily scale up scale down cloud resources  
- Cloud encourages remote working and promotes team collaboration  
- Cloud automatically updates its services  
- It results in better disaster recovery and provides high security  
- It gives businesses a competitive advantage
[Cloud Adoption Framework](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/overview)

##### Public Cloud
- A public cloud deployment is identified that don’t own any hardware or infrastructure ; all the resources are provided by a cloud  service provider.  
- The biggest advantage of the cloud services are elastic scalability, resource efficiency, and reducing upfront capital investment.  It’s optimized for performance, but this is less cost-effective.  
- AWS, Azure, IBM cloud and Google Cloud are all popular public cloud providers.
Advantage
- Built to support workload of virtually any scale
- Ease of use without upfront cost
- massive catalog of services
Disadvantage
- shared tenancy 
- data residency/privacy reg
- pay for everything you use
##### Private Cloud
- The private cloud is a dedicated environment for a single enterprise or organization.
- Hardware and resources are not shared outside your company.  
- There is a possibility to get a private cloud from a public cloud provider.  
- Resources are dedicated to a single organization.  
- Some well-known private cloud providers are: Red Hat Open Stack, Rackspace, Microsoft Azure Stack and VMware Private Cloud
Advantage:
- less risk of exposing data
- greater control
- more restrictive access
Disadvantage:
- more restrictive catalog in services
- more expensive

##### Hybrid Cloud
- Hybrid Cloud is the combination of a public and private cloud.  
- Creating a hybrid cloud means that an organization is using the public cloud but also owns on-premises systems  
- Due to security requirements or data protection, some companies can’t operate only in the public cloud, so they choose the hybrid cloud
Advantages:
- enable migration from on premise to scalable solution
- reduce the pain and cost in cloud migration while you run out the cost of your datacenter
- Keep your sensitive data on premise and greater controle over privacy concerns
Disadvantages:
- Infrastructure management is complex and challenging
- Migrating between on-premises and cloud services is not always a one-to-one mapping
- Scalability of on-premise systems is still challenging and can cap the scalability of your system
- Outages may be harder to diagnose and debug as the cloud architecture is more complex

##### Multi Cloud
- Multi cloud model uses more than one cloud provider at a time, where you use both the public and private cloud.
- In multi-cloud, instead of combining private with public, you’d use more than one public cloud. The motivations for a multi-cloud deployment are for redundancy or to optimize cost for preferred technology choices.  
- The most common reason for deploying multi-cloud is when you need a specific service from one public cloud provider and another service from another public cloud provider.  
Advantages:  
- Reduce vendor stickiness and lock-in  
- Potential increase in redundancy depending on your cloud architecture  
- Reduced limits in the catalog of cloud solutions available to you  
Disadvantages:  
- Moving data in the cloud costs you as you consume cloud service providers bandwidth  
- Requires cultivation of multiple deployment/pipeline strategies for delivering to multiple cloud service providers  
- Considerably more complex cloud architecture leads to difficult to observe and troubleshoot systems  
- Very challenging to optimize and find cost savings because of the distribution of costs and resources
### Week 2
###### Compute Services – Virtual Machines
- **Service Type:** Infrastructure as a Service (IaaS).
- **Control Level:** Total control over operating system and software.
- **Use Cases:** Custom software, lift-and-shift scenarios, web apps, databases, desktop applications, jumpboxes, and gateways.
###### Compute Services – Virtual Machine Scale Sets
- **Service Type:** Infrastructure as a Service (IaaS).
- **Scaling:** Built-in auto scaling features for manual and auto-scaled workloads.
- **Use Cases:** Web services, batch processing, and other workloads.
###### Compute Services – Container Instance 
- **Container Advantages:** Lightweight, quick to respond to demand changes, and versatile for various scenarios.
- **Container Instance:** Simplest way to run a container in Azure, suitable for small web apps, background jobs, and scheduled scripts.
- **Compute Services:** Azure offers PaaS and serverless container options.
###### Compute Services – Kubernetes Service(AKS)
- **Service Type:** Managed container orchestration service.
- **Technical Foundation:** Open-source container orchestration platform.
- **Service Model:** Platform as a Service (PaaS).
###### Compute Services – App Service
- **Service Type:** Platform as a Service (PaaS).
- **Functionality:** Hosts web applications, supports multiple programming languages and containers.
- **Integration:** Connects with over 50 connectors for enterprise systems like SAP and Salesforce.
###### Compute Services – Functions
- **Service Type:** Platform as a Service and Serverless.
- **Pricing Model:** Consumption-based plan and Dedicated plan.
- **Target User:** Micro/nano services.
###### Reference Architecture
- **Data Processing:** User behaviour data is loaded into Azure Databricks, prepared, and split into training and testing sets.
- **Model Training and Evaluation:** A Spark Collaborative Filtering model is trained and evaluated using rating and ranking metrics.
- **Recommendation Delivery:** Top recommendations are precomputed, cached in Azure Cosmos DB, and served to users via an API deployed on AKS.
- **Model Deployment:** AKS hosts the containerized model, providing scalability, identity and access management, and logging and health monitoring.
- **Data Storage:** Azure Cosmos DB stores the top 10 recommended movies for each user, providing low latency for read operations.
- **Model Management:** Machine Learning service tracks and manages machine learning models, and then packages and deploys these models to AKS.
### Week 3
###### Regions and Availability Zones  
- Azure/AWS Region Definition: A physical cluster of data centres in a specific geographic location.
- Region Selection Criteria: Chosen based on proximity to the customer to reduce network latency and improve service speed.
- Service Availability: Varies depending on the region.
###### Factors to choose Region
- **Region Selection Criteria:** Choose a region closest to you and your customers to minimize network latency.
- **Cost Consideration:** Use AWS calculators to estimate costs for different regions and make informed decisions.
- **Service Availability and SLA:** Ensure the region supports your required services and check SLA details to meet your needs.
###### Availability Zones
- **Availability Zone Definition:** Isolated and physically separate locations within a region, each with independent power, cooling, and networking.
- **High Availability and Redundancy:** Customers can deploy applications and data across multiple availability zones to ensure high availability and redundancy.
- **Disaster Recovery:** In case of a disaster, the cloud provider can automatically switch to another zone within the same region.
###### Cloud Networking
- **Cloud Networking Definition:**  Provides fully managed and scalable networking and connectivity options, including connecting on-premise data centres to the cloud.
- **Cloud Networking Services:** Enables secure virtual network infrastructure, application traffic management, DDoS protection, secure remote access, and global network connectivity routing.
- **Azure Networking Services Categories:** Connectivity (Azure VNet, ExpressRoute), Application Protection (Azure Load Balancer, Firewall), and Application Delivery.
- **Networking Resources for Application Delivery:** Azure CDN, Azure Front Door Service, Azure Traffic Manager, Application Gateway, and Internet Analyzer.
- **Network Monitoring Services:** Network Watcher, ExpressRoute.Monitor, Azure Monitor, or VNet Terminal Access Point (TAP).
###### Networking Services – Virtual Network
- **Virtual Network Function:** Fundamental building block for private networks in the cloud, enabling communication between cloud resources and on-premise environments.
- **Virtual Network Features:** Provides isolation, segmentation, communication, filtering, and routing between resources.
- **Virtual Network Peering:** Allows connectivity and resource sharing between virtual networks within the same region (local peering) or across different Azure regions (global peering).
###### Networking Services – Application Gateway
- **Traffic Management:** Manages web application traffic and makes routing decisions based on HTTP request attributes.
- **Traffic Routing:** Routes traffic to specific server pools based on URL paths, such as routing image requests to one pool and video requests to another.
- **Features:** Offers features like autoscaling, web application firewall, redirection, session affinity, URL routing, SSL termination, and integration with Azure Monitor.
###### Networking Services – Network Security Groups
- **Azure NSG Function:** Filters network traffic between Azure resources within an Azure virtual network.
- **NSG Security Rules:** Define inbound and outbound traffic rules for Azure resources or subnets.
- **Private Endpoint:** Provides a private and secure connection to Azure services using a private IP address from the virtual network.
###### Networking Services – Load Balancer
- **Load Balancing Functionality:** Distributes traffic evenly across backend resources for inbound and outbound scenarios.
- **Load Balancer Types:** Public load balancers for outbound connections and internal/private load balancers for traffic within a virtual network.
- **Benefits:** Improves resource distribution, availability, and scalability, supporting both TCP and UDP applications for external and internal traffic.
###### Networking Services – VPN Gateway
- **VPN Gateway Functionality: Sends encrypted traffic between Azure virtual networks and on-premise locations over the public internet.**
- **Site-to-Site VPN:** Creates a secure connection over IPsec/IKE VPN tunnel for cross-premises and hybrid configurations.
- **Point-to-Site VPN: Allows secure connections to a virtual network from individual client computers.**
###### Reference Architecture – Multi Region N-tier application
- **High Availability:** Use two regions, one primary and one secondary for failover, to achieve higher availability.
- **Traffic Routing:** Azure Traffic Manager routes incoming requests to the primary region and fails over to the secondary region if the primary region is unavailable.
- **Resource Organization:** Create separate resource groups for the primary region, secondary region, and Traffic Manager for flexible management.
###### Load balancer vs traffic manager in Azure
- **Azure Load Balancer:**  Distributes load within a single region, ensuring application availability.
- **Traffic Manager:** Distributes traffic across multiple Azure regions for global geographic availability.
- **Use Case Comparison:** Use Load Balancer for single-region load balancing and Traffic Manager for multi-region traffic routing.
### Week 4
##### Structured Data
- Structured Data: Tabular data represented by columns and rows in a database.
- Relational Database: Databases that hold tables of structured data.
- SQL Usage: Structured Query Language used for managing and querying structured data.
##### Semi Structured Data  
- **Semi-structured Data:** Information that lacks the rigid structure of relational databases but still possesses some organizational elements.
- **Examples:** JSON documents, key-value stores, and graph databases.
##### Unstructured Data
- Information without a pre-defined structure or data model.
- Characteristics: Text-heavy, may contain numbers, dates, and facts, and includes videos, audio, and binary files.
- Examples: Word documents, PDFs, text files, media logs.
##### Azure storage redundancy
- **Data Redundancy in Azure Storage:** Azure Storage always stores multiple copies of data to protect against data loss from various events.
- **Redundancy Considerations:** The decision on redundancy level depends on the specific scenario, balancing cost and availability.
- Factors for redundancy options include:
	- Data replication within the primary region.
	- Replication to a geographically distant secondary region.
	- The application’s need for read access to replicated data in case of primary region unavailability.
###### Redundancy in the primary region:
- Data is always replicated three times in the primary region.
- **Locally Redundant Storage (LRS):** Replicates data three times within a single data centre, offering the lowest cost and least durability.
- **Zone-Redundant Storage (ZRS):** Replicates data across three availability zones for high availability and data governance compliance.
###### Redundancy in the secondary region:
- **Data Durability:** Azure Storage offers GRS and GZRS for copying data to a secondary region for durability in case of catastrophic failure.
- **GRS (geo-redundant storage) Mechanism:** GRS synchronously copies data three times within a primary region’s physical location using LRS, then asynchronously copies it to a single location in the secondary region.
- **GZRS (geo-zone-redundant storage) Mechanism:** GZRS copies data across three availability zones in the primary region (like ZRS) and replicates it to a secondary region using LRS for regional disaster protection.
##### Storage Service 
###### Storage account
- Features: Provides a unique namespace for Azure Storage data, accessible globally via HTTP/HTTPS.
- Data Characteristics: Secure, highly available, durable, and massively scalable.
- Service Group and Usage: Includes Blob, Queue, Table, and File storage for files, messages, semi-structured data, and high-performance applications.
###### Blob storage
- Unstructured object storage solution for the cloud, designed for storing files of any kind.
- Blob Storage Advantages: Manages physical storage needs, allowing developers to focus on other tasks.
- Blob Storage Tiers: Offers different storage tiers (Hot, Cool, Cold, Archive) to optimize costs based on data access frequency and retention period.
###### Queue storage  
- Storage and processing of small data messages.
- Functionality: Access messages globally via authenticated HTTP/HTTPS calls, designed for scalable asynchronous processing.
- Common Use Cases: Event-driven architectures, workload processing, and decoupling systems.
###### Table storage
- Azure Table Storage Characteristics: NoSQL database designed for fast access to semi-structured data, offering key/attribute storage with a schema-less design.
- Azure Table Storage Use Cases: Ideal for storing structured, non-relational data with fast and cost-effective access.
- Azure Table Storage vs. Cosmos DB Table API: 
	- Cosmos DB offers
		- superior performance (10 million operations/second vs. 20,000), 
		- global distribution (up to 30 regions vs. single region with read-only secondary)
		- different billing models (storage volume vs. storage and operations).
###### File storage
- Azure Files Protocol Support: Supports SMB, NFS, and Azure Files REST API.
- Data Storage Type: Stores structured data.
- Use Cases: 
	- Extending on-premise file shares
	- deployment and testing
	- sharing files among multiple machines or users.
###### Disk storage
- Virtualized disks similar to physical disks in on-premises servers.
- Managed Disk Purpose: Provide persistent storage for Virtual Machines.
- Managed Disk Characteristics: Available in different sizes, types (SSD, HDD), and performance tiers.
##### Azure Data Lake Storage Gen2
- Data Handling: Designed for massive data sets in big data analytics and machine learning.
- Storage Capabilities: Combines Azure Blob Storage scalability with HDFS file system capabilities.
- Data Organization: Hierarchical namespace for efficient data structure and performance.
##### Azure Data Lake Storage Gen2 vs Azure blob

| Features       | ADLS gen 2          </font>                                                                                                           | Azure Blob                                                                               |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Data Structure | Hierarchical namespaces efficiently organize and store data.                                                                          | Flat data structure complicates data management.                                         |
| Data Analytics | Designed for big data analytics and machine learning, supporting integrations with Apache Spark, Hadoop, and Hive.                    | Designed for unstructured data, lacks analytics.                                         |
| Cost           | Azure Data Lake Storage Gen2 offers tiered storage options for flexibility and cost savings, but is more expensive than blob storage. | Azure blob storage is cheaper than ADLS.                                                 |
| Performance    | Azure Data Lake Storage Gen2 outperforms Azure Blob Storage in data access and query performance.                                     | Blob Storage is a cost-effective option for businesses without advanced analytics needs. |







 


