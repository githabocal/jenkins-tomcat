# jenkins-tomcat

- Create an instance 
- Connect to ec2 (ssh -i ~/<Path of key.pem> ec2-user@PublicIPv4)
- sudo su - --> to switch root user
- run the command ```wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo``` to add the jenkins repo
- import a key file from Jenkins CI to enable installation from the package ```rpm import https://pkg.jenkins.io/redhat-stable/jenkins.io.key```
- install java with the command ```amazon-linux-extras install java-openjdk11 -y```
- install jenkins with the following command ```yum install jenkins -y```
- Enable the Jenkins service to start at boot: run the following command ```systemctl enable jenkins```
- To start Jenkins as a service, run the following command ```systemctl start jenkins```
- Add 8080 port to Security group
- go to PublicIP:8080
- cd /opt
- to install maven, run following command ```wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz```
- To untar ```tar -xzvf apache-maven-3.8.6-bin.tar.gz```
### Sources:
- [jenkins install amazon linux](https://www.jenkins.io/doc/tutorials/tutorial-for-installing-jenkins-on-AWS/)wget -O /etc/yum.repos.d/jenkins.repo
- [maven](https://maven.apache.org/)
- [tomcat](https://tomcat.apache.org/)