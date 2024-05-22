# Azure-Virtual-Machines


### To begin our Azure Honeynet project, we’ll set up virtual machines (VMs) as the foundation. Azure Virtual Machines act like cloud-based computers and will be essential for our honeynet. Here are the steps we’ll follow in Microsoft Azure:


**1 . Sign in to the Azure portal:**


Visit the Azure portal(https://portal.azure.com/).
Log in using your existing Azure account credentials.
If you don’t have an account yet, create one here. With an Azure free account, you’ll get 12 months of free services, access to over 40 services that are always free, and a $200 credit to explore additional services within 30 days. It’s a great way to get started with Azure! 😊🔐🌐


<details close> 
<summary> 2. Create a virtual machine: </summary>

- After you log in to the Azure portal, navigate to the 'Virtual machines' section. 
  
  **Azure Portal Home**

<img width="1280" alt="Screenshot 2024-05-16 at 8 01 39 PM" src="https://github.com/mahin12/Azure-Virtual-Machines/assets/27288616/99a83e57-b10a-44f3-818b-c17b14453508">

- Click on 'Create', then 'Virtual machine'. This is where we'll set up our new VM!
  
<img width="1280" alt="Screenshot 2024-05-21 at 8 48 25 PM" src="https://github.com/mahin12/Azure-Virtual-Machines/assets/27288616/763f3d03-9e60-4b33-bf4d-8bc1f0a7fe3a">


</details>

<details close> 


<summary> 3. Configure the VM settings: </summary>

  
  - **Subscription and resource group:** Let’s proceed by selecting the Azure subscription and resource group (Which is way to group and manage resources in Azure!). For the purpose of the project, I already created created a resource group called ```RG-Mahin-Lab```


<img width="1280" alt="Screenshot 2024-05-22 at 10 55 46 AM" src="https://github.com/mahin12/Azure-Virtual-Machines/assets/27288616/4a0da8e2-8f25-423d-949e-a44c93d31a44">


  
  - **Virtual Machine Name:** Now, I am going to name this VM, ```windows-vm```, which is necessary.
  
  <img width="903" alt="Screenshot 2024-05-22 at 11 03 11 AM" src="https://github.com/mahin12/Azure-Virtual-Machines/assets/27288616/5dc69308-b17b-4ec1-b22c-4387b8851d53">


  - **Region:** I am going to choose the region, ```(US) East US 2```
  
  - **Image:** Now let's select ```Windows 10 Pro, version 21H2 - x64 Gen2```
  
  
  <img width="1271" alt="Screenshot 2024-05-22 at 10 52 20 AM" src="https://github.com/mahin12/Azure-Virtual-Machines/assets/27288616/0828c934-1ab8-4721-a048-fbd9120c0bc3">

  - **Networking**: When creating the virtual network, we will be leaving it to the default settings. For the purpose of this lab, I called mine ```Mahin-VNet```.
  


  </details>


