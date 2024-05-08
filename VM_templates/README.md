# ELZ Simple VM Deployment Example
This ARM Template and accompanying UI Definition demonstrates how to deploy a VM using simplified form directly in the Azure Portal.

## Description
This ARM Template and accompanying UI Definition demonstrates how to deploy a VM using simplified form directly in the Azure Portal. This template is intended to be used as a **showcase** and **starting point** for creating your own custom Azure deployment templates.

## CreateUIDefinition.json
The `CreateUIDefinition.json` file defines the user interface for creating a virtual machine in Azure. It is used by the Azure portal and other Azure management tools to display a form for collecting input from the user.

## ARM Template for Virtual Machine Deployment
The `deploytemplate.json` ARM template deploys a virtual machine in Azure with the specified configuration.

### Prerequisites
Before deploying this ARM template, you must have the following:

- An Azure subscription
- A resource group in which to deploy the virtual machine
- An existing virtual network and subnet in the resource group
- An existing storage account in the resource group

### Deployment Steps
To deploy the virtual machine using this ARM template, follow these steps:

1. In the VM OS Management Dashboard, click the "Deploy VM | UI" button.

1. In the Azure portal, a custom UI will appear. Provide the required parameters for the deployment, such as the virtual machine name, size, and administrator credentials.

1. Review and accept the terms and conditions, then click "Purchase" to start the deployment.

1. Wait for the deployment to complete. This may take several minutes.

1. Once the deployment is complete, you can connect to the virtual machine using Remote Desktop or SSH.

### Parameters
This ARM template requires the following parameters:

- `virtualMachineName`: The name of the virtual machine to deploy.
- `virtualMachineSize`: The size of the virtual machine.
- `osversion`: The operating system version to use for the virtual machine.
- `networkInterfaceName`: The name of the network interface to use for the virtual machine.
- `osDiskType`: The type of storage account to use for the virtual machine's OS disk.
- `evidenmanaged`: A tag indicating whether the virtual machine is managed by Eviden.
- `evidenbackup`: A tag indicating whether the virtual machine is backed up by Eviden.
- `evidenpatchingschedule`: A tag indicating the patching schedule for the virtual machine.

### Outputs
This ARM template provides the following outputs:

- `virtualMachineName`: The name of the deployed virtual machine.
- `virtualMachineId`: The ID of the deployed virtual machine.
- `virtualMachinePublicIp`: The public IP address of the deployed virtual machine.

### License
This ARM template is licensed under the MIT License. See the LICENSE file for details.