# Advanced Demo - Advanced Demo - Simple Site2Site VPN

![Stage1 - PNG](TBC)

- Stage 1 - Create Site2Site VPN <= `YOU ARE HERE`
- Stage 2 - Configure onpremises Router
- Stage 3 - Routing & Security
- Stage 4 - Testing
- Stage 5 - Cleanup

# Get IP Address for the onpremises Router

Go to the 1-click deployment cloudformation template https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks?filteringStatus=active&filteringText=&viewNested=true&hideStacks=false  
Click `infra` stack  
Click `Outputs` tab  
Note down the Router IP, you will need is soon  


# Create customer Gateway Object

Move to the `VPC` console, under `Virtual private network (VPN)` click `Customer Gateways`  
Click `Create Customer Gateway`  
For `Name tag` enter `A4L-onpremRouter`  
For `IP address` enter the IP address you noted down above  
Click `Create customer gateway`  

# Create VGW and Attach to the AWS VPC

Move to the `VPC` console, under `Virtual private network (VPN)` click `Virtual Private Gateways`  
Click `Create virtual private gateway`  
Under `Name tag` enter `awsVGW`  
Click `Create virtual private gateway`  
Select `awsVGW`, click `Actions` and `Attach to VPC`  
Click the `Available VPCs` dropdown, select `A4L-AWS` and click `Attach to VPC`  

# Create VPN Connection

Move to the `VPC` console, under `Virtual private network (VPN)` click `Site-to-Site VPN Connections`  
Click `Create VPN connection`  
