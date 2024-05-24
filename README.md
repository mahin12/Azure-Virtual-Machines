# Azure-Virtual-Machines


### To begin our Azure Honeynet project, we’ll set up virtual machines (VMs) as the foundation. Azure Virtual Machines act like cloud-based computers and will be essential for our honeynet. Here are the steps we’ll follow in Microsoft Azure:


**1 . Sign in to the Azure portal:**


Visit the Azure portal(https://portal.azure.com/).
Log in using your existing Azure account credentials.
If you don’t have an account yet, create one here. With an Azure free account, you’ll get 12 months of free services, access to over 40 services that are always free, and a $200 credit to explore additional services within 30 days. It’s a great way to get started with Azure! 😊🔐🌐


<summary> 2. Create a virtual machine: </summary>

- After you log in to the Azure portal, navigate to the 'Virtual machines' section. 
  
  **Azure Portal Home**

<img width="1280" alt="Screenshot 2024-05-16 at 8 01 39 PM" src="https://github.com/mahin12/Azure-Virtual-Machines/assets/27288616/99a83e57-b10a-44f3-818b-c17b14453508">

- Click on 'Create', then 'Virtual machine'. This is where we'll set up our new VM!
  
<img width="1280" alt="Screenshot 2024-05-21 at 8 48 25 PM" src="https://github.com/mahin12/Azure-Virtual-Machines/assets/27288616/763f3d03-9e60-4b33-bf4d-8bc1f0a7fe3a">


</details>



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



<summary> 4. Inbound Security Rule Configuration: </summary>

When it comes to securing your Azure Virtual Machines, Network Security Groups (NSGs) play a crucial role. Let’s break down the steps for configuring inbound security rules:
 
  - **Navigate to the Network Security Group (NSG):** In the Azure portal, search for 'Network Security Groups' in the search bar at the top. Once there, select the NSG associated with the VM.
  
  - **Create an inbound security rule:** Inside the NSG, you'll find a section for 'Inbound security rules'. This is where we control what kind of traffic is allowed to reach our VM. Click on 'Add' to create a new rule.
    
  - **Configure the rule:** We'll be prompted to input some details about our new rule.
  
  - **Source:** This defines where the incoming traffic is coming from. We can set this to ```Any``` to allow traffic from any location.
  
  - **Source port ranges:** This specifies the ports on the source (the computer initiating the connection) that are allowed. Again, we can set this to ```*``` or ```Any``` to allow all ports.

  - **Destination:** This defines where the traffic is going to. Since we want the traffic to reach our VM, we can set this to ```Any```.
  
  - **Destination port ranges:** This specifies the ports on our VM that are allowed to receive traffic. We can set this to ```*``` or ```Any``` to open all ports.
    
  <img width="588" alt="Screenshot 2024-05-22 at 11 43 51 AM" src="https://github.com/mahin12/Azure-Virtual-Machines/assets/27288616/8025b447-716f-4d0a-8ac4-ff4abdbba4eb">

  - **Priority:** Setting priorities in Network Security Groups (NSGs) is an essential step. The priority determines the order in which rules are applied. Rules with lower priority numbers are processed before rules with higher priority numbers because the lower the number, the higher the priority. For the purpose of this lab, I set the priority to ```300``` to ensure that this honeypot functions as intended!

  - **Action:** We'll set this to ```Allow```, which means that traffic matching this rule will be allowed to reach our VM. 
  

  
  - **Review & Create:** After i've input and configured all the details we need for this inbound rule, click 'Add' to create the rule. e


# Conclusion

# By setting up our virtual machines (VMs) and establishing open inbound security rules, we're effectively leaving our VM's entrance unguarded. Typically, this isn't a practice you'd employ in a genuine production setting due to the high risk of attack it presents. Yet, within the framework of our honeynet, this is precisely the behavior we desire. It enables us to lure in potential attackers and monitor their behavior within a managed setting.
 
 
 
 
 
 
 
 
</details>


