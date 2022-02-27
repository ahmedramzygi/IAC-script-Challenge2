# IAC-script-Challenge2
Creating the required Infrastructure-as-code scripts for a new cloud environment in AWS of the following diagram with the following resources and properties:-
Write a CloudFormation script that:

1)Creates a VPC.

2)It will accept the IP Range -also known as CIDR block- from an input parameter.

3) Creates and attaches an Internet Gateway to the VPC.

4)Creates Two Subnets within the VPC with Name Tags to call them “Public” and “Private”

5) These will also need input parameters for their ranges, just like the VPC.

6) The Subnet called “Public” needs to have a NAT Gateway deployed in it.

7) This will require you to allocate an Elastic IP that you can then use to assign it to the NAT Gateway.

8)The Public Subnet needs to have the MapPublicIpOnLaunch property set to true. Use this reference for help

9) The Private Subnet needs to have the MapPublicIpOnLaunch property set to false

10)Both subnets need to be /24 in size

11)You will need 2 Routing Tables, one named Public and the other one Private

Assign the Public and Private Subnets to their corresponding Routing table

Create a Route in the Public Route Table to send default traffic ( 0.0.0.0/0 ) to the Internet Gateway you created

Create a Route in the Private Route Table to send default traffic ( 0.0.0.0/0 ) to the NAT Gateway

Finally, once you execute this CloudFormation script, you should be able to delete it and create it again, over and over in a predictable and repeatable manner, this is the true verification of working Infrastructure-as-Code
