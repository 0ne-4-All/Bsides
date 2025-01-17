Manual Azure setup: 

Step 1. [Create an Azure Subscription](https://azure.microsoft.com/en-us/free/) - First, you will need a subscription. This subscription will be tied to an email address and used to build the resources within. Azure offers a $200 credit for the first 30 days of use and is plenty of time to test and understand the concepts. Click [here](https://azure.microsoft.com/en-us/free/) to begin this process.

![Github Logo](/Screenshots/Azure_free.PNG)

Step 2. [Create a Resource Group](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal) - The next thing is to create a resource group. The resource group is where all of our resources (VM's, V-Net, and many others) will be kept within the subscription. It is often best practice to create a resource group for different environments. Maybe one is for your production environment while the other is for the development environment. In this case this resource group will be for our lab. So make sure to place everything going forward in this resource group. After logging into your new Azure Portal go ahead and click on the resource group image and create one. Keep in mind latency and trying to keep the data center as close to your location as possible. 

![Github Logo](/Screenshots/resource.PNG)

Step 3. [Create a V-Net](https://docs.microsoft.com/en-us/azure/virtual-network/quick-create-portal) - The first thing we want to create in our resource group is the virtual network. This will allow our resources within to communicate and create a virtual entity. Search at the top of the portal for virtual network and create a new one. Keep in mind to link it to the resource group. 

![Github Logo](/Screenshots/VNET_Create.PNG)

You can use the default address space given during creation as shown below.

![Github Logo](/Screenshots/VNET_IP.PNG)

The following image displays the overview of the newly created virtual network as an example.

![Github Logo](/Screenshots/VNET_Overview.PNG)

Step 4. [Create a Network Security Group](https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-filter-network-traffic) - Next we want to create a a Network Security Group. We will create rules to allow or diallow traffic into our network and out of our network. For instance in the examples below we created two rules inbound so our Public IP's could have ingress into the network and establish connections to the VM's. You can use a great website called [IPChicken](https://ipchicken.com/) to quickly retrieve it. The screenshots belopw show an overview of how we set the NSG up. 

Just like previous resources fill in the relevant information. 

![Github Logo](/Screenshots/NSG_Create.PNG)

The following NSG rules show the two inbound rules we created for the NSG. Make sure to use your Public IP. 

![Github Logo](/Screenshots/NSG_Rules.PNG)
