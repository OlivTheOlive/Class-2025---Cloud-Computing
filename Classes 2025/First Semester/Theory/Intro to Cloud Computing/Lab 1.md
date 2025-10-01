Olivie Bergeron
### **Due on Oct 5, 2025 11:59 PM**
Go over these main tasks for Azure:
Step 1 - Create an Azure blob/Storage account for region US East and select local redundant storage.
- Screenshot should show the creation of Storage account, in the specified region and settings. Go to the storage account you created and Overview tab and take a screenshot showing those settings.
![[Pasted image 20250928113817.png]]
US East was not available, Canada central was.

---

Step 2 – Add file named sample_container.csv objects to containers via GUI.
- Screenshot should show that csv file has been added to the container

![[Pasted image 20250928114240.png]]


---

Step 3 - Create file share.
- Screenshot should show that file share has been created
![[Pasted image 20250928114500.png]]

---
Step 4 – Work with objects in the containers, using AzCopy and download sample_container.csv file to a local folder, take screenshot of AzCopy commands and output - NO USE OF SAS TOKEN IN COMMAND.
- Screenshot should show terminal with command downloading csv file and file being downloaded, show entirety of the output
- Screenshot should show the csv file in your file explorer or whatever folder you’ve downloaded it to

![[Pasted image 20250929205609.png]]
![[Pasted image 20250929205658.png]]

---
Step 5 – Add file named sample_fc.json to file share using SAS token via command line, take screenshot of steps and output.
- Screenshot should show you uploading the .json file via SAS token, so show where you found the SAS token in the azure portal
- Screenshot of command uploading .json file via SAS token and successful output command
- Screenshot of the azure portal showing file has been uploaded
![[Pasted image 20250928120647.png]]
![[Pasted image 20250928121240.png]]
![[Pasted image 20250929210215.png]]

---

Step 6 – Check your current IAM policy for yourself.
- Screenshot should show your current IAM policy that you have for that storage account
![[Pasted image 20250929210311.png]]
---
Step 7 – Create IAM policy for storage account, that is relevant to the service that would allow you to view all resources, but does not allow you to make any changes.![[Pasted image 20250929210153.png]]
- Show each step of giving yourself the correct role
![[Pasted image 20250929205847.png]]
![[Pasted image 20250928121609.png]]
![[Pasted image 20250929205808.png]]

---
Step 8 – After lab, delete container and contents created.
- Show you deleting storage account or resource group and successful deleted message
![[Pasted image 20250928121813.png]]
![[Pasted image 20250928122041.png]]