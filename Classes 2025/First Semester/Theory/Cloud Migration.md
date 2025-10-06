[BrightSpace](https://brightspace.algonquincollege.com/d2l/home/825144)

#### Week 2
- over the internet
- infra --> vms, storage, databases, networking
- cloud services expands --> IoT, ML and AI
- allow on-demand increase and decrease in IT capabilities due to space and location constraints

CapEX(less tax advantageous): one time, upfront expenditure to purchase or secure tangible resources --> buying assets...
OpEX (tax advantageous): is spending money on services or products over time --> renting, leasing, subscription...

Cloud migration Approaches (5 Rs)
- Rehost = Lift-And-Shift migration
- reBuild
- replace
- refactor
- rearchitect

Shared responsibility model --> exam question

#### Week 3
Developing a cloud adoption strategy
1. Identify motivations  
	1. Migration
	2. Innovation
2. Document business outcomes  
	1. **Fiscal outcomes:** Financial or fiscal performance is the cleanest business outcome for many business leaders, but not the only one.  
	2. **Agility outcomes:** Today's fast-changing business environment places  a premium on time. The ability to respond to and drive market change quickly is the fundamental measure of business agility.  
	3. **Reach outcomes:** In a constantly shrinking market, global reach (ability to support global customers and users) can be measured by compliance in geographies that are relevant to the business.
3. Financial considerations  
4. Technical considerations 
	1. **Scalability:** Right-sizing resources and utilizing auto-scaling, matching the scalability needs, turning off workloads outside of business hours and scaling only when necessary have the added benefit of driving more sustainable workloads
	2. **Availability:** On-premises, it's more costly to build highly available infrastructure. It's less costly to architect highly available infrastructure in the cloud.
	3. **Security and compliance:** When it comes to security and compliance, Microsoft is continually expanding our security infrastructure and toolsets to keep you on par with what's transpiring with respect to security threats on global networks.
	4. **Capacity optimization:** Capacity optimization, where you only pay for the resources you utilize over time, is another technical benefit of the cloud.
6. Organizational alignment and skills readiness plans  
7. Creating a business case

#### Week 4
##### Understand your digital estate
- **Cloud Strategy:** A mix of workload migration, modernization, and cloud-native approaches.
- **Digital Estate:** Applications, data, and VMs that need to be understood for a successful cloud strategy.
- **Innovation Potential:** The cloud unlocks innovative potential for technology portfolios.
##### Evaluation digital estate
- **Initial Step:** Identify on-premises infrastructure, applications, and dependencies.
- **Workload Identification:** Use Azure Migrate’s server assessment tool to identify workloads, dependencies, and optimization opportunities.
- **Cost Projection:** Gather optimized cost projections for workloads to be migrated to Azure.
##### The Discovery and Assessment tools  
- **Azure Readiness Assessment:** Evaluates the readiness of on-premises machines for migration to Azure.
- **Azure Sizing and Cost Estimation**: Estimates the size and cost of running on-premises servers in Azure.
- **Dependency Analysis:** Identifies cross-server dependencies and optimization strategies for migrating interdependent servers to Azure.
##### Identifying workloads in use
- **Azure Migrate Appliance Function:** Performs agentless discovery of on-premises VMs and physical servers.
- **Data Collected by Appliance:** Machine, disk, NIC metadata; installed applications, roles, and features; performance data (CPU, memory, disk IOPS, throughput).
- **Discovery Process:** Continuous discovery collects machine configuration information and performance metadata.
##### Dependencies between workloads
- **[Dependency Analysis](https://learn.microsoft.com/en-us/azure/migrate/concepts-dependency-visualization?view=migrate-classic) Benefits:** Visualize and identify cross-server dependencies to understand optimization strategies for moving interdependent servers to Azure.
- **Dependency Analysis Purpose:** Helps determine if machines are in use or can be decommissioned, ensuring nothing is left behind and avoiding outages during migration.
- **Next Step After Analysis:** Create high-confidence groups of servers and start assessing them.
##### Readiness and suitability analysis
- **Azure Readiness Categories:** Ready, Conditionally ready, Not ready, and Readiness unknown.
- **Readiness Report Export:** Allows filtering and understanding of Azure readiness for machines.
- **Machine Migration Guidance:** Provided based on the readiness category, with varying levels of required changes.
##### Sizing
- **Azure Readiness Assessment:** Provides sizing recommendations for Azure VMs and disks based on performance history or on-premises settings.
- **Database Assessment Recommendations:** Offers suggestions for database SKU, pricing tier, and compute level.
##### Evaluate gaps and blockers
- **Migration Planning:** Analyze downtime constraints and operational dependencies to ensure RTO and minimal data loss.
- **Compatibility Check:** Review and mitigate compatibility issues or unsupported features before migration.
- **Assessment Tools:** Utilize server assessment reports and database assessment tools for compatibility analysis.

##### Prioritize workloads
- **Migration Prioritization:** Consider factors like complexity, time-to-migrate, business urgency, production considerations, compliance, security requirements, and application knowledge.
- **Migration Strategy:** Adopt an “apply and learn” approach to migrate applications systematically and controllably.
- **Initial Migration Focus:** Identify and migrate applications and workloads based on collected inventory information.
##### Finalizing the migration plan
- **Migration Plan:** Create a plan that includes application and database availability, downtime constraints, migration milestones, data copy time, and post-migration testing.
- P**ost-Migration Testing:** Conduct functional, integration, security, and performance testing to ensure applications work as expected and data is transferred successfully.
- **Migration Roadmap:** Build a roadmap that includes a maintenance window for minimal downtime and to limit operational and business impact.

#### Week 5

##### Rehosting/Lift and Shift
- A migration option that moves existing applications to Azure without code changes, allowing for quick cloud migration.
- **Rehosting Advantages:** Enables quick cloud migration, avoids code changes, and allows apps to leverage Azure IaaS scalability.
- **Rehosting Process:** Prepare Azure and on-premises VMs, replicate VMs, and then migrate them to Azure.
