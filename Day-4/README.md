docker:


what is dev environment?
It is a server where we are able to run our application.

Testing environment?
where software testing team can perform the functional test cases ,non functional test cases and perform the performance testing , load testing and all the test cases will run in this environment.

UAT ENVIRONMENT:
BEFORE RELEASING THE PRODUCT INTO THE MARKET , WE HAVE TO SHOW PROTOTYOPE OF THE APPLICATION TO THE CLIENT

production encironment :

where we can actually deploy the application where users can access the application.

what is meant by container ?
container is a virtual machine where you are actually going to run the application.

docker file is a text document , it contains set of instructions how to run the application in the container.
docker file is used to create docker iamge.

docker image is a template , it scontains what u need to run the application. that means it contains your source code, dependencies, configuration files, libarayr files , on which platfor u want to run the application (build once , run anywhere).

what is docker hub?
docker hub is a registry or library where we can store all the docker images.

what deamon containers ? or detached board?

every microservice works in different port numbers.

__________________________________________________________________________________________________________________________________________

1] create a ec2 instance -> create a key-pair -> edit security group to your name -> open putty and connect to the instance -> now in putty terminal ->sudo su-> service docker status -> service docker start -> now create a docker container (check screenshots) ->

if u execute docker ps -a : it is going to show all docker containers , despite the state.

docker ps : will show running containers.
(check screenshots)

ctrl + p + q to come oout without stopping the container.

-p : to specify port number
hostport number : it is a user choice , we can give any port number whichever the user likes.
This port number defines how to access the application from the server.

after creating a container fopr muralimohan 

open aws -> click instance id ->copy the public ip address and paste in browser , now go to security -> EDIT INBOUND RULES -> ADD ALL TCP -> ANY WHERE VP4. DONE.




DOCKER FILE INSTRUCTIONS:

1]FROM INSTRUCTION : IT WILL DEFINE BASE IMAGE OR PARENT IMAGE OF THE APPLICATION. EVERRY DOCKER FILE MUST START BY FROM INSTARUCTION
2]COPY INSTRUCTION : TO COPY A FILE OR A DIRECTORY FROM LOCAL MACHINE INTO DOCKER IMAGE.
3]ADD COMMAND : SAME AS COPY INSTRUCTION, TO DOWNLOAD PACKAGES FROM THE INTERNET TO DOCKER IMAGE.
4]RUN COMMAND : IT IS GOING TO HELP DOWNLOAD THE DEPENDENCY PACKAGES , OR INSTAL THE PACKAGES OR INSTALL DEPENSDENCIRES IN A CONTAINER.
5].DOCKER.IGNORE  : IF U WANT TO REMOVE UNNESECARY PACKAGES OR FILES WHILE UR BUILDING A DOCKER IMAGE . WE ARE GOING TO USE .DOCKER.INGORE .
6]CMD COMMAND : CMD INSTRUCTION DEFINES WHICH CODE OR ARTIFACT U WANT TO RUN IN A CONTAINER.
7]ENTRYPOINT : DEFINES THE ENTRY OF THE APPLICATION . [ CMD INSTRUCTIONS WILL ALLOW RUNTIME ARGUMENTS, ENTRY POINT WILL NOT ALLOW THE RUNTIME ARGUMENTS ]
8]EXPOSE : IT DEFINES ON WHICH PORT NUMBER U WANT TO ACCESS THE APPlication.
9]ENV :DEFINES ENVIRONMENT VARIABLES OF THE APPLICATION.
10]WORKDIR : IT DEFINES KEEP THE FILES INSIDE THE CONTAINER.
11]USER : IF YOU WANT TO CREATE USSER ACCOUNTS U ARE GOIMNG TO USE USER INSTRUCTION.


1] fork the repository -> clone to local machine -> open terimal -> git clone -b master https://github.com/Arnil10/Dimple-CapsuleProject.git

2] now in the server , clone the repo -> go inside the repo -> build a docker image -> see screenshots (inspect) -> hub.docker.com download -> see screenshots -> then push to docker hub -> 



__________________________________________________________________________________________________________________________________________

notes:

as a devops engineer , we have to collect endpoint ,port numbers and environments variables.

same container port number as given in the application. (in .env file)

when writing a docker file , follow six steps . 
the first step is to identify the base image of the application,
create a work directory , 
copy the dependency into docker image,
install the dependency 
copy the source code from local to docker image,
define the expose port number,
mention which code we have to run in a container.





assignment for tomorrow:  create a web project using chatgpt and write a docker file for the application , deploy in a nignex web server.

identify the problems with the containers.

docker compose.


