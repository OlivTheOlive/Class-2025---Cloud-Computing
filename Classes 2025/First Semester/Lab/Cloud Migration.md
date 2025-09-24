[BrightSpace](https://brightspace.algonquincollege.com/d2l/home/825144)

### Week 2
[Case-Study](https://www.microsoft.com/en/customers/story/787511-vipps-banking-azure)
##### Lab 1
1. Pick a case study and come up with a 1 page migration plan that includes
    - What are the company's motivators of migration to the cloud?
		- International expansion (Scaling)
		- strong partnership and accelerated innovation
		- “It was essential for us to maintain business momentum while we scaled up,”
    - What questions will you ask to understand more about the company infrastructure?
	    - What are the expected and potential international growth metrics?
	    - What are you building? 
	    - What are your consumer needs/requirement?
	    - Will you need to ReHost?
	    - What are the security compliance?
	    - Hybrid, Public, Private or Multi-cloud cloud model?
    - Produce a RACI matrix for the migration stakeholders

| Stakeholder     | Planning | Design | Implementation | Testing/Validation | Cost |
| --------------- | -------- | ------ | -------------- | ------------------ | ---- |
| Dev Team        | C        | R      | R              | A                  | I    |
| Project Manager | R        | A      | A              | I                  | A    |
| QA Team         | I        | C      | C              | R                  | I    |
| CEO             | A        | I      | I              | I                  | R    |


    - Describe the most likely migration approach that will suit the chosen company.
	    - This company will most likely do a rehost migration where they will host the current implementation with minimal changes to the design. However, the business will make use of the Azure services in their implementation. 
    - Produce a high level schedule for the migration process
		- ~2 Years
		-  Plan --> Ready --> Adopt
			- Assess Workload --> Deploy Workload --> Release Workload
    - What are the main decision criteria for the chosen company?
	    - I like finance.



### Week 3

client ->> traffic manager --> firewall --> load balancer --> virtual network(front end <--> MT <--> DB) 
##### Lab 2
**Scenario:** The following application consists of a Web Server written in Flask. A UI front end written in React. A database layer consisting of Postgres.

##### On-Prem
[![On prem](https://mermaid.ink/img/pako:eNp9U02P2jAQ_SvWnEAKKJgkkGjVQ3fbE6tW20qVSjhM4kmwNnGQcfqF-O_rxIGSA-uLPfPe88wb2SfIG0GQAOp8Lw3lptU0y8hgqlLF7Cp10x7YkfQv0hO3Tbff-p19UeyrpnrnmB0oc2KFbpSZSGVIKzLT7ecuZp-U2DGphpvGCpFNBBrM8EjT7dNwusvOMH8lJa7NDPGIP1ZUDYqbhjY2ZB-xQpWTvlumkJp-Y1XdOrGpHzZ1V2M0FoXMbyTfXYY9o8LynWp5JWk0tcc-sWMXLyJLNuxhNvvAXpLLCBzSzzt5ceAmGWGdcws5pCcOmsHcFeuIDho8_FcNVIe6Pq_gQHYYeFBqKcBmW_KgJl1jF8Kpw1Mwe6ophcQeBerXFFJ1tpoDqp9NU19k9r2V-0vQHuzDoCeJpUbLKLA6dhTrj_Rj0yoDSbSO-zsgOcEfSDjn8yBY8HARhctVHHnwF5JlxOcxXy_8cBXwiPvB2YN_fU1_vor8OF6F8TLw-TrioQckpGn0s_sY_f84vwGVcgmu?type=png)](https://mermaid.live/edit#pako:eNp9U02P2jAQ_SvWnEAKKJgkkGjVQ3fbE6tW20qVSjhM4kmwNnGQcfqF-O_rxIGSA-uLPfPe88wb2SfIG0GQAOp8Lw3lptU0y8hgqlLF7Cp10x7YkfQv0hO3Tbff-p19UeyrpnrnmB0oc2KFbpSZSGVIKzLT7ecuZp-U2DGphpvGCpFNBBrM8EjT7dNwusvOMH8lJa7NDPGIP1ZUDYqbhjY2ZB-xQpWTvlumkJp-Y1XdOrGpHzZ1V2M0FoXMbyTfXYY9o8LynWp5JWk0tcc-sWMXLyJLNuxhNvvAXpLLCBzSzzt5ceAmGWGdcws5pCcOmsHcFeuIDho8_FcNVIe6Pq_gQHYYeFBqKcBmW_KgJl1jF8Kpw1Mwe6ophcQeBerXFFJ1tpoDqp9NU19k9r2V-0vQHuzDoCeJpUbLKLA6dhTrj_Rj0yoDSbSO-zsgOcEfSDjn8yBY8HARhctVHHnwF5JlxOcxXy_8cBXwiPvB2YN_fU1_vor8OF6F8TLw-TrioQckpGn0s_sY_f84vwGVcgmu)
##### Question IaaS

In a IaaS implementation, the application will need to manage almost everything except hardware. This includes maintaining the firewall, VNet, load balancing, front-end and back-end integration, and the database. However, a IaaS platform like Azure likely provides tools and documentation on scaling this using various technologies such as VMs or containers, offering much more control over your app compared to a PaaS.
[![](https://mermaid.ink/img/pako:eNptU0uP2jAQ_iuWTyAFlOeGWFUPsK1UiVbVbtVDCQcTz4JFsNHgsG0R_72OHXaz2-SQeL7HZGZsX2ilBVBGOVY7aaAyDcJkA4aXithni7o5kqrWjRi593i1aD_kC-eP5DvqsxSA6774rEYnwDPgePVToml4Tb6Beda4XxOpfK5SeUcrlBWQJ9TKjKQygArMePW5jcknJUjkTOchfTxoiAcNYjMS3PANP8F4dd-tBpW-9pcW5rzag0376OJBR6256JWytCGZ85qrqmd4V79EeOZ13e-gg_pD6luqWsKbGS0csL6lFhu2JB8mk4_kgfniPe5GxR48tfyfii3XUvM3VNtTRyyZ0_XwucN_eDzucnXlv5hapad85a_ZOiUN6BaloMxgAwE9AB54G9JLayup2cEBSsrsUnDcl7RUV-s5cvVL68PNZo_cdncLmqPdZLiXfIvcKp54fWoldv8AF7pRhrK4cCkou9DfNppF0yLK8yyaJbM0SfKA_qEsCbNpmhdRmoR3YXIXZek1oH_dT8NplkZFPgvDKCvSLE2ygIKQRuNXf4_cdbr-AzSaF3s?type=png)](https://mermaid.live/edit#pako:eNptU0uP2jAQ_iuWTyAFlOeGWFUPsK1UiVbVbtVDCQcTz4JFsNHgsG0R_72OHXaz2-SQeL7HZGZsX2ilBVBGOVY7aaAyDcJkA4aXithni7o5kqrWjRi593i1aD_kC-eP5DvqsxSA6774rEYnwDPgePVToml4Tb6Beda4XxOpfK5SeUcrlBWQJ9TKjKQygArMePW5jcknJUjkTOchfTxoiAcNYjMS3PANP8F4dd-tBpW-9pcW5rzag0376OJBR6256JWytCGZ85qrqmd4V79EeOZ13e-gg_pD6luqWsKbGS0csL6lFhu2JB8mk4_kgfniPe5GxR48tfyfii3XUvM3VNtTRyyZ0_XwucN_eDzucnXlv5hapad85a_ZOiUN6BaloMxgAwE9AB54G9JLayup2cEBSsrsUnDcl7RUV-s5cvVL68PNZo_cdncLmqPdZLiXfIvcKp54fWoldv8AF7pRhrK4cCkou9DfNppF0yLK8yyaJbM0SfKA_qEsCbNpmhdRmoR3YXIXZek1oH_dT8NplkZFPgvDKCvSLE2ygIKQRuNXf4_cdbr-AzSaF3s)

##### Question PaaS

In a PaaS implementation, the application requires less hands-on implementation and integration. Using a cloud provider like Azure and its PaaS tools, users have less control over the environment but gain access to more prebuilt configurations. In our scenario, users won’t create their own firewall or load balancer. Instead, they can use an auto-scalable web app for the front end, an auto-scalable app services (backend), and connect to their integrated database service.
[![](https://mermaid.ink/img/pako:eNptU0uP2jAQ_iuWTyABynMDVtUDbHuiq2q36qGEg4lnwSLYaHDY7SL-e_0I22ybHBLPfI_MjO0LrbQAyijHaicNVKZBGG_A8FIR-2xRN0dS1boRA_8erhbuQ76jPksBuO7yzmpwAjwDDlc_JZqG1-QBzIvG_ZpIFWxKFRSOKCsgz6iVGUhlABWY4eqri8kXJUjsRec-ftIrSHoFYjMQ3PANP8Fwdd-uepmh9vcW5rzag7V98nGvotZcdEpZ2pDMec1V1RH8U79EeOF13e2gTXWH1JVUtYQPM1r4xPpmLTZsST6Nx5_JIwvFh7wfFXsM0PJ_KLGYg-YfINdTCyyZ53Xyc5__EfJJ69WW_y5yzACFyv-6tUw6oluUgjKDDYzoAfDAXUgvTlZSs4MDlJTZpeC4L2mprlZz5OqX1oebzB657e4WNEe7yXAv-Ra5ZTzz-uQodv8AF7pRhrK7OPcelF3oK2XJNJ7M4qLI42k6zdK0GNHflKVRPsmKWZyl0V2UWkl2HdE3_9dokmfxrJhGUZzPsjxLrR0IaTR-C3fIX6XrHzwNFi4?type=png)](https://mermaid.live/edit#pako:eNptU0uP2jAQ_iuWTyABynMDVtUDbHuiq2q36qGEg4lnwSLYaHDY7SL-e_0I22ybHBLPfI_MjO0LrbQAyijHaicNVKZBGG_A8FIR-2xRN0dS1boRA_8erhbuQ76jPksBuO7yzmpwAjwDDlc_JZqG1-QBzIvG_ZpIFWxKFRSOKCsgz6iVGUhlABWY4eqri8kXJUjsRec-ftIrSHoFYjMQ3PANP8Fwdd-uepmh9vcW5rzag7V98nGvotZcdEpZ2pDMec1V1RH8U79EeOF13e2gTXWH1JVUtYQPM1r4xPpmLTZsST6Nx5_JIwvFh7wfFXsM0PJ_KLGYg-YfINdTCyyZ53Xyc5__EfJJ69WW_y5yzACFyv-6tUw6oluUgjKDDYzoAfDAXUgvTlZSs4MDlJTZpeC4L2mprlZz5OqX1oebzB657e4WNEe7yXAv-Ra5ZTzz-uQodv8AF7pRhrK7OPcelF3oK2XJNJ7M4qLI42k6zdK0GNHflKVRPsmKWZyl0V2UWkl2HdE3_9dokmfxrJhGUZzPsjxLrR0IaTR-C3fIX6XrHzwNFi4)

### Week 4
### Section 1: On-Premises Solution Design
**Scenario**:  
A mid-sized retail company currently runs a traditional on-premises solution consisting of:

- Web Application (Monolithic) hosted on physical servers.
- Backend database on an SQL server.
- File storage using a local file system.
- Basic networking handled by company-operated routers and firewalls.
- email services for client notification 

#### **Solution**
[![](https://mermaid.ink/img/pako:eNpVUm1vmzAQ_ivWfU6yOiEkoGnS0gxpUqp25UOkQTU5cA3WwEZnsyyL8t9nQ-jWD4Cfl3t8PnyBQpcIMbzW-lRUgizbPeeKsftaorLZ8GEb0ieD9OKVr8oiKbTZuHCs5013OJJoK_aonggbadD82AorCvS-LIdHNR0F9k_IoU9lLNlniSQ8ibpmH9iz7uxtQ8b2eMjcwz63LXuqzkYWomYp0i8kc7NsN1n6bXcj-_iDMDhGp9lO-5pE1sjSs7HYpFaTOI6OByHr7Evj3n2ELAYBVTkc7jaHj9Ppp7cB_D-MQUn2nkv2A3IdD8W-9Z7Zbt7BJB3hgH0TMIEjyRJiSx1OoEFyTTkIF-_NwVbYYA6xW5aCfuaQq6uraYX6rnUzlpHujhXEr6I2DnVtKSxupXD_p3ljyR0O6V53ykLMV9G8T4H4Ar8hnq6j2XrJV0GwCMOI8_lyAmdni1azKOLLMFgFd3y-mAfXCfzpN-YzHoZrzqNgcbcMeOTzsJRuyg_DDesv2vUvHn7HAA?type=png)](https://mermaid.live/edit#pako:eNpVUm1vmzAQ_ivWfU6yOiEkoGnS0gxpUqp25UOkQTU5cA3WwEZnsyyL8t9nQ-jWD4Cfl3t8PnyBQpcIMbzW-lRUgizbPeeKsftaorLZ8GEb0ieD9OKVr8oiKbTZuHCs5013OJJoK_aonggbadD82AorCvS-LIdHNR0F9k_IoU9lLNlniSQ8ibpmH9iz7uxtQ8b2eMjcwz63LXuqzkYWomYp0i8kc7NsN1n6bXcj-_iDMDhGp9lO-5pE1sjSs7HYpFaTOI6OByHr7Evj3n2ELAYBVTkc7jaHj9Ppp7cB_D-MQUn2nkv2A3IdD8W-9Z7Zbt7BJB3hgH0TMIEjyRJiSx1OoEFyTTkIF-_NwVbYYA6xW5aCfuaQq6uraYX6rnUzlpHujhXEr6I2DnVtKSxupXD_p3ljyR0O6V53ykLMV9G8T4H4Ar8hnq6j2XrJV0GwCMOI8_lyAmdni1azKOLLMFgFd3y-mAfXCfzpN-YzHoZrzqNgcbcMeOTzsJRuyg_DDesv2vUvHn7HAA)
Our current On-Premises datacenter solution has a basic data flow implementation. Clients make internet requests, which are routed through the firewall to access the web app. From there, they make necessary requests and actions using the backend services. This implementation can be easily migrated to a mainly PaaS setup with some refactoring. However, since the application was made monolithically, the integration may be more intricate than expected. Despite this, I still believe a mostly PaaS setup would be beneficial for the organization’s size and the simplicity of their product. This means they don’t need full control over every system. Below is the suggested migration:
- Web App --> PaaS - Azure App Service
- Backend SQL --> PaaS - Azure SQL Database
- File Storage --> PaaS - Azure Blob Storage
- Networking --> Cloud Networking, not needed to migrate, platform will manage 
- Email Services --> SaaS - Azure Communication Services

### Section 2: Migration Strategies

#### **Solution**
##### Migration Strategy
###### Web App --> PaaS - Azure App Service = *Refactor*
###### Backend SQL --> IaaS - Azure VM = *Rehost*
###### File Storage --> PaaS - Azure Blob Storage = *Refactor*
###### Networking --> Cloud Networking = *Rebuild*
###### Email Services --> SaaS - Azure Communication Services = *Replace*

##### Migration Plan
###### Step 1: Assess current solution needs
Inventory existing infrastructure, analyze networking, and establish an Azure migration plan.
###### Step 2: Networking (Rebuild)
Design and deploy Azure VNet, subnets, NSGs, and configure connectivity for hybrid stage. Set up load balancer, firewall, and access policies.
###### Step 3: Backend Database (Rehost)
Setup Azure VM for SQL Server on On-Prem systems using local Azure private VMs.
###### Step 4: File Storage (Refactor)
Azure Blob Storage account creation, data migration and application code refactoring.
###### Step 5: Web Application (Refactor)
Azure App Service integration and deployment. The user will be able to configure scaling, monitoring, and custom domain.
###### Step 6: Email Services (Replace)
Configure Azure Communication Services for email delivery.
###### Step 7: Optimization & Transition
Monitor and scale performance, optimize VM sizing, enable backups, strengthen governance, and decommission on-prem resources as needed or migrate back if the cloud solution isn't fulfilling business needs.

---

