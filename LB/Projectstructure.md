Project Structure

The project structure is designed to provide clarity and organization for easy navigation and understanding of the Load balancer in Azure with Azure VM Load Balancer project.

#Directory Structure

docs/: Contains the project documentation files.

LoadBalancer_Documentation.md: Main project documentation file.

ARM_Templates/ : Contains all the ARM templates and parameter files for deploying the virtual network, VMs, and load balancer.
vnet.json:       : ARM template for Virtual Network deployment.
vm1.json         : ARM template for VM1 deployment.
vm1.parms.json   : Parameter file for VM1 deployment.
vm2.json         : ARM template for VM2 deployment.
vm2.parms.json   : Parameter file for VM2 deployment.
lb.json          : ARM template for Load Balancer deployment.
lb.parms.json    : Parameter file for Load Balancer deployment.

Deployment_Scripts/: Includes the PowerShell script used to deploy all the resources in sequence.

Technologies-used.md: Lists the technologies used in the project.

license.md: This library is licensed under the MIT-0 License. See the LICENSE file.
