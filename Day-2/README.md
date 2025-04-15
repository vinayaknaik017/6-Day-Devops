4 factors important to business:

1]fast delivery
2]quality
3]lesser spending
4]availabilty


cloud :

is a remote service 
all services accessed over the internet

datacenter -- is a collection of servers


cloud services:

1]iaas
2]paas
3]saas


aws 3 services:

1]auto scaling
2]availability of services(99.11)
3]on demand


important services for us :

1]Computing--> EC2 service (to create remote servers in the cloud) elastic compute
2]Containers-->
3]DataBase--> DynamoDB RDS
4]game
5]iot platform
6]management and governace
7]cloudwatch
8]networking and content delivery --> VPC Route53
9]quantum computing (ongoing future)
10]Storage



!!!!!1st practical:(Computing - EC2)!!!!!

pre requisites:

download putty 

making a server requires:
1] OS
2] storage
3] configuration of ur server

virtual machine means remote machine

in Linux to give permission we need to make changes in visudo files

what is webserver?

3 tiers:
webserver
application server
database server

in Linux sever two families:
1]red hat family -> amazon Linux , oracle Linux, SUSC , RHCL.(whenever use red hat family, install httpd(daemon server))
2]Debian family -> ubuntu OS, Debian OS.(whenever use Debian, install apache 2 server or igenex server)

whenever you want to install any packages in Linux use (yum).{update delete everrything}.

for others to use public ip address
private ip adress


steps:

1]computing -> EC2 -> launch instance -> name it -> select amazon 5.10 -> create new key pair -> name , select .ppk -> edit network settings
-> arnil-security copy paste -> 30 gb -> 2 instances -> launch.

2] view instances -> slect and connect -> ssh client -> copy link and paste in putty -> apperence -> font size 14 -> connection -> keep alive -> 60 -> ssh -> auth -> select ppk file -> open -> accept


3]In linux server, viduso and then sudo su (to swuitch users)  PERFORM MANY COMMANDS SEE SCREENSHOTS

4] to come back :wq

5] click on instance copy the public ip address , dopes not open in website. 
now click security in link , then edit inboud rules , add rule , HTTP (ANYONE CAN ACCES), then anywhere ipv4 , save.



!!!!!LOAD BALANCING!!!!!!!

TWO TYPES:

1]L4 balancing 
2]L7 balancing



steps:

1] load balncers -> classic load balancer -> name it -> selct two regions -> add security group from last experiment -> advanced health ->
make healthy threshaold 2 -> attach two server sto load balancer.


