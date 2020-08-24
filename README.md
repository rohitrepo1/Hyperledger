                                           Hyperledger Fabric Installation Guide
This document will provide the overview and installation process of Hyperledger Fabric 
Hyperledger Fabric is an open source enterprise-grade permissioned distributed ledger technology (DLT) platform, designed for use in enterprise contexts, which was established under the Linux Foundation
This technology enables confidentiality through its channel architecture.
Fabric is comprised of the following components:
•	A pluggable ordering service.
•	A pluggable membership service provider.
•	peer-to-peer gossip service.
•	Smart contracts (“chaincode”) run within a container environment (e.g. Docker) for isolation.
•	A pluggable endorsement and validation policy enforcement that can be independently configured per application.
Hyperledger Fabric can be configured in multiple ways to satisfy the diverse solution requirements.


                                     
Below are the Pre-requisite to  get the infrastructure ready 
 
•	Hyperledger fabric Installation version (v1.4)
•	Visual studio code with extension  (for extension please follow the steps in the link https://code.visualstudio.com/docs/remote/ssh-tutorial )
•	Please have a oracle VM installed  with ubuntu 16.04
•	To SSH into the machine please have install openssh-client


Once you are ready with the above set up lets ssh and Start with the installation process.

           
 

Post SSH  we will have the visual studio code connected to the VM 

System requirements

•	Update  the machine  
sudo apt update
sudo apt -y upgrade

•	Installing Curl 
sudo apt install curl 

•	Next we will install GIT 
sudo apt install git 

•	Install Python 
sudo apt install -y python-minimal






Install Docker  and Docker compose 

sudo apt install apt-transport-https ca-certificates gnupg-agent software-properties-common 
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - 
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" 
sudo apt update
sudo apt -y install docker-ce 
sudo usermod -aG docker <YourUserNameGoesHere> 
sudo curl -L https://github.com/docker/compose/releases/download/1.18.0/docker-comp ose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose 
sudo chmod +x /usr/local/bin/docker-compose 
sudo reboot now.



Let’s change the Directory and move the desktop 

 

Once you are  in the Desktop directory Use the following command to curl down the fabric-samples project folder, and Docker images
curl -sSL http://bit.ly/2ysbOFE | bash -s 1.4.0
once the download is complete  you should see as below 
 
Now let’s verify if everything is installed in a proper order 
•	docker-compose -v
•	docker -v
•	git -v 
 
Check if you have all the docker images required downloaded locally 
 
 
	 
Coming soon!! This is a Part 1 of the document on Hyperledger fabric, we will update the advance concepts!!
For any queries please reach out to me : resourcee.labb@gmail.com






