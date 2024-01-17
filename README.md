# WEB APPLICATION CI/CD PROCESS

## Complete Stetp-by-step Jenkins CI/CD With Github Integration.

This sample Node js web application on implementing continuous integreation and Delivery pipeline

1. Create Sample web application and push into the GITHUB
2. Whenver the devloper push the code it will trigger the pipeline automatically using the GITHUB Webhooks

Step-1

Create a Instance and install JENKINS and APACHE/NGINEX.

1. connect to Jenkins server using Gitbash
2. Update the apt repository
   sudo apt-get update
3. install jdk
   sudo apt-get install -y openjdk-11-jdk
4. Dwonload the Jenkins war file
   wget https://get.jenkins.io/war-stable/2.426.2/jenkins.war
5. To start the jenkins
   java -jar jenkins.war
6. To access jenkins from browser using Public IP
7. Install the apache/nginex
   sudo apt-get install apache2
   sudo apt-get install Nginex
Go to default path
 cd /var/www/html/
check the permisions using ls -la command
change the permission for html
chmod 777 /html/

step-2

Access the jenkins using public ip and default port number jenkins is 8080 then the jenkins page would apper paste the password
![image](https://github.com/Santhoshvoja63/New-webapp/assets/147876790/33f3b0c2-293e-455b-aecb-6b26fd758ba7)

After pasting password below page will apper click on install suggested plugins
![image](https://github.com/Santhoshvoja63/New-webapp/assets/147876790/bb48fd30-1219-4ddd-9a36-1e02def59d6a)

after the install plugins you need to create first admin user
![image](https://github.com/Santhoshvoja63/New-webapp/assets/147876790/542f3280-f8f2-4138-ac26-172edeac86a8)

step-3

start using jenkins
1. On jenkins dashboard click on New item to create a first job 
   ![image](https://github.com/Santhoshvoja63/New-webapp/assets/147876790/47a14f37-42cf-4c83-963b-2fa2c96a3fe5)
2. Enter job name then click on free-style project

   ![image](https://github.com/Santhoshvoja63/New-webapp/assets/147876790/1c46f3da-1e61-4343-a93c-c7bef8d648c9)
3. Now we need to configure various parameters of our first job in jenkins
4. In configure section select source code management select git
   paste the Repository URL
   After that select branch to build give the latest branch name
   ![Capture](https://github.com/Santhoshvoja63/New-webapp/assets/147876790/cd399bed-16e4-4f37-9d59-e0b2714d1744)
5. Then select Build triggers tab
   In build trigger select Github hook trigger for GITScm polling option
6. In GITHUB create a web hook and give jenkins URL and select git push and git pull option
   whenver the devloper push the code it will automatically deploy the code.

Step-4

Build Step select Execute shell using below script.
 cp * /var/www/html/
Then select Apply and Save
![image](https://github.com/Santhoshvoja63/New-webapp/assets/147876790/60b7761a-9733-4029-aa82-78d4de9e68f6)

Sample Web application.
![Capture1](https://github.com/Santhoshvoja63/New-webapp/assets/147876790/cc18a745-9285-473f-879d-8b73056084c3)


Challenges:

I have faced one challege during the setup regarding the copy files to web server directory I got permission denaied issue so I have change to excution permission to this file /html/ directory. then I have issue resolved.
   





   

