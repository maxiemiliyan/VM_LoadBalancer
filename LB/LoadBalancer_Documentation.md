Project Title: VM Load Balancer

Project Description:
The "VM Load Balancer" project is an Azure-based cloud infrastructure solution designed to improve the availability, scalability, and performance of web applications hosted on multiple virtual machines (VMs). By leveraging an Azure Load Balancer, this project ensures that incoming network traffic is efficiently distributed across VMs, providing fault tolerance and enhanced load management.

Key Components:

Azure Resource Group:

The entire project is organized within a resource group named demo, located in the East US region, to manage and monitor all related Azure resources cohesively.
Virtual Network (VNet):

Deployment: The virtual network (vnet.json) is deployed first, providing a secure and isolated environment where the VMs and load balancer reside.
Configuration: The VNet is configured with necessary subnets, ensuring efficient routing of traffic between the load balancer and the VMs.
Virtual Machines (VM1 and VM2):

VM Deployment: Two Windows-based VMs (vm1.json and vm2.json), each with associated parameter files (vm1.parms.json and vm2.parms.json), are deployed within the VNet. These VMs serve as backend servers in the load balancing setup.
Network Interfaces: Each VM is equipped with a network interface (NIC) for connectivity within the VNet, along with dynamic public IP addresses and Network Security Groups (NSGs) configured to allow HTTP and RDP traffic.
Security: Inbound security rules are applied to allow traffic on ports 3389, 80, and 443, ensuring secure communication with the VMs.
Azure Load Balancer:

Load Balancer Deployment: The load balancer is deployed using the ARM template (lb.json) and its parameter file (lb.parms.json), ensuring that traffic is effectively distributed between VM1 and VM2.
Frontend IP Configuration: A static public IP is assigned to the load balancer, which acts as the entry point for all inbound traffic.
Backend Address Pools: The VMs are added to the load balancer’s backend address pool, allowing for traffic distribution based on their health and availability.
Health Probes and Load Balancing Rules: Health probes are configured to monitor the availability of each VM, and load balancing rules are established to manage traffic routing, ensuring consistent and reliable access to the application.
Deployment Process:

Authentication: The deployment process begins with authenticating to Microsoft Azure using the Connect-AzAccount command.
Resource Group Creation: A new Azure resource group named demo is created in the East US region using New-AzResourceGroup.
Resource Deployments:
The virtual network is deployed first using the vnet.json template.
VM1 and VM2 are deployed next, each using their respective template and parameter files (vm1.json, vm1.parms.json, vm2.json, and vm2.parms.json).
Finally, the load balancer is deployed, linking it with the previously created resources.
Outcome:
The project successfully demonstrates the deployment and configuration of a scalable and reliable cloud infrastructure using Azure services. The Azure Load Balancer effectively manages traffic across multiple VMs, ensuring high availability and improved performance for hosted applications. This deployment showcases proficiency in using ARM templates for automated resource provisioning and highlights key skills in cloud architecture and network management.