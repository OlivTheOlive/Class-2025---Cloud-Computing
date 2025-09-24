[Course](https://brightspace.algonquincollege.com/d2l/home/825141)

### Week 1
What is Cloud Computing
- the on-demand availability of computing resources over the internet (storage and infrastructure)
- eliminate need to self-manage physical resources and only pay for what we use
Traditional monolithic design
- build everything, cost to build and maintain infra
- very high cost to start
- straight-foward to build, deploy, test, debug and vertically scale
- Difficult to scale horizontally
- miantenance challenges due to large codebase
- lower availabilty
- limited flexibility 
- complex and time-consuming deployment processes

### Week 2
![[Pasted image 20250910194621.png]]
### Week 3
##### Microservices
Is an architectural style that structures an application as a collection of loosely coupled, independently deployable services.
- **Definition:** A set of principles, patterns, and constraints that guide how software systems are structured.
- **Purpose:** Describes how components are organized, how they interact, and what trade-offs are accepted.
- **Examples:** Monolithic, layered, client-server, and microservices architectures.
###### Loosely Coupled
- **Loose Coupling Definition:** Each component operates independently with minimal dependencies on other components.
- **Loose Coupling Benefits:** Enables flexibility for independent service evolution and resilience against failures.
- **Loose Coupling Mechanism:** Services interact through **well-defined interfaces or APIs.**
###### Organized Around Business Capabilities
- **Microservice Organization:** Each microservice is **built around a specific business function or capability**.
- **Business Alignment:** This organization **reflects real-world business needs**, ensuring development aligns with company goals.
- **Example:** A Product Service manages products, while a Shipping Service handles shipping logistics.
###### Owned by a Small Team
- **Team Structure: Small, cross-functional teams** own and maintain each microservice.
- **Team Autonomy:** Teams have **autonomy to develop, deploy, and operate** their service independently.
- **Benefits of Autonomy:** Supports **agility** and fosters **accountability**.
###### Product Focused
- **Service Ownership:** The team responsible for developing a service **also handles its operation and maintenance** in production.
- **Service Lifecycle:** Services are treated as products with their own lifecycle, requiring continuous updates, support, and enhancements.
- **Value Focus: The emphasis is on delivering real value** to end users**, treating the service as a long-term product.
####### **Advantages**
- **Scalability Benefits:** Services can be scaled individually, leading to better resource efficiency.
- **Development Flexibility:** Teams can use different technologies for different services.
- **Fault Tolerance:** Isolated failures prevent system-wide outages.
####### **Challenges**
- **Challenges of Microservices:** Increased complexity in deployment, monitoring, testing, and data management.
- Data Consistency: Maintaining data consistency and transactions across multiple services is complex.
- **Inter-service Communication:** Requires robust mechanisms for reliable communication, **especially in distributed systems.**
##### Modern Design: The Twelve-Factor Application
- **Methodology for Cloud Applications:** Twelve-Factor Application is a methodology for building cloud-based applications.
- **Focus of the Methodology:** Portability across environments and declarative automation.
- **Benefits of the Methodology:** Rapid deployment, scaling, and feature addition.
![[Pasted image 20250917191730.png]]

##### Microservices Architecture: 
###### Microservices
- Each core functionality is separated into an independent service. 
- **Microservices Definition:** A modern architectural approach where an application is built as a collection of small, self-contained services.
- **Microservices Characteristics:** Independently deployable, use API communication, loosely coupled, organized around business capabilities, owned by a small team, and product-focused.
- **Service Communication:** Services communicate over the network using protocols like HTTP/HTTPS, WebSockets, and AMQP.
![[Pasted image 20250917194924.png]]
###### Client Apps
- **Client Types:** Mobile App (smartphone) and Traditional Web App (HTML-based).
- **Client-Backend Interaction:** Clients interact with the backend system through the API Gateway.
- **WebApp Functionality**: Serves HTML pages and handles browser client interactions for the traditional web application.
###### API Gateway
- **API Gateway Role:** Acts as a centralized entry point for client requests, routing them to the appropriate backend services.
- **Client Interaction:** Clients interact with a single, unified API, unaware of the multiple services working behind the scenes.
- **API Gateway Functionality:** Performs routing, authentication, rate limiting, and other operations on incoming requests.
###### Event Bus
- **Messaging Pattern:** Implements a **publish/subscribe messaging pattern**.
- **Microservice Communication:** Allows microservices to **communicate asynchronously**.
- **Coupling:** Helps achieve **loose coupling**.
###### Container Host
- **Containerization Benefits:** Portability, scalability, and isolation of services.
- **Microservice Deployment:** Each microservice and the web app run as **Docker containers**.
###### Independently Deployable
- **Service Deployment:** Each service can be deployed and updated independently, minimizing downtime and simplifying the deployment process.
- **Data Management:** Each service maintains **its own database**, preventing central bottlenecks.
- **Deployable Units:** Services can be deployed as **executable JAR files**, operating system executables, or **Docker container images**.
###### API Communication
- **Communication Protocols:** Micro-services communicate through protocols like **HTTP/HTTPS, WebSockets, or AMQP**.
- Protocol Advantages and Challenges: Each protocol has its own strengths and weaknesses, influencing performance, scalability, and resilience.
- Protocol Selection: A well-designed architecture often uses **a combination of protocols** to optimize performance.
##### **Microservices communication:**
###### Synchronous
![[Pasted image 20250917201349.png]]
- **Communication Style:** Synchronous communication between services.
- **Service Dependency:** Tight coupling where each service relies on the availability and response of downstream services.
- **Performance Impact:** Latency and failure **propagation can impact** the entire request chain **if services are slow or unavailable.**
###### Asynchronous one-to-one
![[Pasted image 20250917201336.png]]
- **Asynchronous Communication: Services communicate without waiting for immediate responses, enabling independent processing.**
- **Loose Coupling:** Services interact through message queues, promoting flexibility and reducing dependencies.
- Resilience and Scalability: Message queues enhance fault tolerance and allow services to scale independently based on demand.
 ###### **Publish/Subscribe**
 ![[Pasted image 20250917201319.png]]
- **Publish/Subscribe Model:** Decouples services by allowing one service to **publish** a message and multiple services to **subscribe** and react to it.
- Event-Driven Architecture: Services react to events rather than calling each other directly, enabling broadcasting and loose coupling.
- **Scalability and Flexibility:** Easily add new services without modifying existing architecture**, suitable for real-time systems or systems with multiple services reacting to** the same event.
##### Micro-services vs Monoliths
- **Monolithic Architecture: Single codebase**, all functionalities **managed and served together**.
- **Micro-services Architecture: Loosely coupled**, **independently deployable** services
##### Cloud Services:
###### Azure Service Bus
- **Purpose:** **Fully managed** messaging system for reliable communication between microservices.
- **Messaging Models:** Supports **queues** (point-to-point) and **topics/subscriptions** (publish/subscribe).
- **Use Case: Microservice-to**-microservice communication where reliability and guaranteed delivery are critical.
###### Azure Events Hub
- **Performance:** Capable of handling **millions of events per second** with low latency.
- **Use Cases:** Real-time data ingestion and event streaming.
- **Scalability: Ideal for Publish/Subscribe at massive scale**.
### Week 4
#### Containers
- **Container Benefits:** Lightweight, portable, and consistent execution environment.
- **Container Advantages over VMs:** Isolate services with less overhead, start faster, and enable microservices at scale.
- **Container Impact:** Independent deployment, faster scaling, and efficient resource use.
#### VMs
**Benefits**:
- **Resource Optimization:** Divides one physical machine into multiple virtual machines for better resource utilization.
- **Scalability:** Offers easier scaling and rapid elasticity.
- **Cost Efficiency:** Employs a pay-as-you-go model for virtual machines in the cloud.
**Limitations**:
- **Resource Consumption of VMs:** Each VM requires CPU, storage, RAM, and a guest operating system.
- **Impact of Multiple VMs:** Running more VMs leads to increased resource consumption.
- **Guest OS Overhead:** Guest operating systems contribute to resource wastage.

#### OS Virtualization: Containerization
- **Container Architecture:** Containers share the host OS kernel and often binaries and libraries, making them lightweight and fast to start.
- **Resource Efficiency:** Containers are exceptionally lightweight, typically in the megabyte range, and start in seconds.
- **Shared Resources:** Containers share the host OS kernel and, usually, the binaries and libraries, which are read-only.
##### Containers
- **Container Benefits:** Lightweight, portable, and consistent execution environment.
- **Container Advantages vs VMs:** Isolate services with less overhead, start faster, and enable microservices at scale.
- **Container Impact:** Independent deployment, faster scaling, and efficient resource use.

##### Do Containers Run on Linux or Windows?
- **Container Operating System:** Containers primarily run on Linux.
- **Linux Container Prevalence:** Linux containers are the standard and most widely used form of containers.
- **Windows Container Limitations:** Windows containers are less common, workload-specific, and use different isolation models.
##### How Containers Are Implemented
- **Container Implementation:** Containers are implemented using a combination of existing Linux kernel features and modern tooling.
- **Isolation Mechanism:** *Namespaces* provide isolation for containers by separating resources like process IDs, network interfaces, and file systems.
- **Resource Management:** *Control groups (cgroups)* allow for the management of resource allocation, preventing any single container from monopolizing resources.
- **Union File Systems (e.g., OverlayFS) (layered filesystems):**  
	- Container images are built in layers (base OS, dependencies, app code).  
	- Layers are shared across containers, saving space and speeding up deployment.
###### Container Engine
- A platform for creating, deploying, and running containerized applications.
- **Examples:** Docker, containerd, and CRI-O.

###### Containers: a great enabler of cloud-native!
- An isolated environment for running applications.
- **Container Image:** A read-only template used to launch a container.
	- A template or blueprint for creating a running container.
	- Image is like a recipe, and container is like a dish.
	- **Dockerfile:** A simple text file used to build Docker images.
- **Container Image Content:** Includes code, runtime, system tools, libraries, and settings.
##### Containerized Microservice
- **Containerization Process:** Packaging code, dependencies, and runtime into a container image. 
- **Image Storage:** Images are stored in a container registry, acting as a repository.
- **Registry Location:** Registries can be local, on-premises, or in the cloud, with Docker Hub being a public option.
- **Container Instance Lifecycle:** Application starts or scales by transforming the container image into a running container instance.
- **Container Instance Portability:** The instance runs on any computer with a container runtime engine installed.
- **Container Instance Scalability**: You can have as many instances of the containerized service as needed.
