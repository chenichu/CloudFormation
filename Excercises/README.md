# Excercise 1 - Create a template that:
  * Creates an Instance and a security group
  * Takes as parameters the SSH Key, AMI Id, and CIDR that can SSH to the Instance
  * Assign an EIP to the Instance
  * Display the EIP output

# Excercise 2 - Create a template that:
  * Create a VPC
  * 2 Public Subnets
  * 2 Private Subnets with no Internet Routing
  * A NAT Instance in one of the Public Subnet 
  * 2 Private subnets with Internet Routing through the NAT instance.
  * Bonus point 1: use a map to select the AMI for the NAT instance
  * Bonus point 2: use conditions to create 3 subnets in regions that have 3 AZs or more

# Excercise 3 - Create a template with:
  * 1 ELB
  * 2 Instance using stock AMZN Linux AMI
    * On the instance install Apache and PHP using cfn-init (UserData+AWS::CloudFormation ::Init)
    * Use a WaitCondition to signal success on the instance.
  * Bonus: Replace teh static instance with ASG 
    * Same as before using cfn-init to setup the instance 
    * Use a creation policy instead of a WaitCondition to signal success
    * Ensure you have all the alarms and scale policies
