[BrightSpace](https://brightspace.algonquincollege.com/d2l/le/content/825146/Home)
### Lab 2
Course: Cloud Solution Architecture
Name: Olivie Bergeron
Student ID: 041068227
##### Screenshot:
Resource Group creation
![[Pasted image 20250918171404.png]]
Virtual Networks
![[Pasted image 20250918174144.png]]
Peering configuration
![[Pasted image 20250918174710.png]]
![[Pasted image 20250918174641.png]]
VM deployments
![[Pasted image 20250918175741.png]]
PowerShell Test-NetConnection results
VM0-->VM1
![[Pasted image 20250918180819.png]]
VM0-->VM2
![[Pasted image 20250918180938.png]]
VM1-->VM2
![[Pasted image 20250918181756.png]]

DELETING RESSOURCES
![[Pasted image 20250918182046.png]]
##### **Findings & Analysis**:
###### **Why VNet peering is important**
VNet peering is important because it creates a private, high-bandwidth connection between virtual networks, enabling them to function as one by isolating itself from the public network.
###### **How private IP communication was established**
Private IP was created to solve the shortage of public IP addresses.
###### **Benefits of global peering (performance & security)**
- Low latency by shortening the data path
- High level of security because its the peering is isolated from public transit

