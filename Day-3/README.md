 
docker
Kubernetes
git


_________________________________________________________________________________________________________________________________________

terraform:


terraform -> it is a iac (infrastructure as a code). whatever resources(ec2,vpc,load balancers,dbs) u want to create by using automation or script on cloud (swa, azure) we use terraform.

terraform helps to create a script whuich can be used several times.

terraform uses HCL (hashi corp language).

when u write in terraform files we have to use different blocks. 

diff bloakcs are :

1] provider block defines which block your doing automation.
2] resource block (what kind of resource you want to create on cloud)(ec2,dbs,vpc)
3] variable blocks (you want to pass any paramets as variable , we have use something called variable block)
output.tf file (if u want to print output in console like public ip address , private ip address, vpc name , vpc address)


WHEN YOU CREATE  AN INSTANCE USING TERRAFORM SCRIPT, MAKE SURE FIVE PARAMETERS ARE PASSED:

1]amazonID
2]instance type
3]key pair name 
4]storage
5]instance name

ARN - amazon resource Name



!!!!!!!!!!!START!!!!!!!!!!!!!!

step 1: install terraform on your windows.

step 2: set terraform path on your windows machine.

step 3: configure AWS credentials from CLI. Install AWS CLI first.



1]open aws -> securitity , identity -> IAM -> users -> create user -> name it -> select last box -> ec2 full access -> vpc full acces -> 
next -> create -> download csv -> open cli -> command aws configure -> copy secret key and key region none -> open vscode create a folder called terraform-scripts -> create a file named ec2.tf -> download terraform EXTENSION -> START TYPING CODE -> (ami id) from aws in ec2 launch instance -> create key pair copy the name to script and sledct ppk-> type more code -> terminal [terraform init] (command will initialize backend configuration with cloud provider API, it is going to generate one license key to authenticate cloud provider API as well as it is going to create .terraform folder which contains the license and the nessecary files)-> in terminal terraform validate (to check syntax)-> terraform plan (it will tell you about what exactly happens in the cloud , shows our plan )-> terraform apply -> terraform destroy (will automatically delete all resources created by the terraform scripts).


2] when you execute a command called terraform plan , it will create terraform.tf state file which contains current state of the instracture . if hacker can hack this file ,he can create whatever instcnaces he want. so it has to be protected.

3] terraform apply

-----------------------------------------------------------------------------------------------------------------------------

VPC - virtual private cloud

whenever creating vpcs , vpc should contain 

subnets are blocks of VPC 

whenever done modififcations , type terraform init, then terraform validate , terraform plan , terraform apply

1] chatgpt prompt

2]paste

3] now vpc and subnet will be availaba in vpc , and subnets. 


_______________________________________________________________________________________________________________________________________


Docker -- it is a containerization tool which can help us to create portable applications to use resources effectively , to create platform independent applications, we are going with docker.(video in youtube)

docker is going to perform OS level virtualization techniques.

we are going to use docker to reduce the cost of the server , to run the application whereve ypu want we are going to use docker.

application will be divided into modules called microservices , each and evry microserervice will ahve a serparaste doicker file,separate image , separate docker container .

eervy microservce applicatrion will deploy in a container


two types:

monolithic is a single tier architecture which means webserver , application server , datsabse server are combined together and we are deploying in a single server.

issues with monolithic :

1]if any module goes down , the entire application goes . why beacise it ahs tightly coupled nature.
if one service goes dwon the entire application goes dwon . thats the reason we are moving towards microervices.


what is microservices??
we will break down appicatoiob  ibnto independent services tht is called loosely coupled applications. if any one service goes dwon , the customer wont get that particular service , the remaing service s cam stil be accessed .

there are some issues with the microservices . each microservice requires a single srver . taht is why the costing is high.


to reduce the cost, to create platfrom independent applications , to create protable applications. we use docker .

build once , run anywhere . that is why we are moving towards docker.



pre-requisites:
1] wsl


