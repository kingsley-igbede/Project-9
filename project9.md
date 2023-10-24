# Kingsley Documentation of Project 9 
## Project 9 - Continous Integration Pipeline For Tooling Website
### INSTALL AND CONFIGURE JENKINS SERVER
### Step 1 -Install Jenkins server

1. Create an AWS EC2 server based on Ubuntu Server 20.04 LTS and name it “Project9-Jenkins”.

	![jenkins instance](./images/jenkins-instance.jpg)

2. Install JDK (since Jenkins is a Java-based application).

`sudo apt update`

`sudo apt install fontconfig openjdk-17-jre`

`java -version`

3. Install Jenkins

`sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key`

  `echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null`

  `sudo apt-get update`

   `sudo apt-get install jenkins`

   `sudo systemctl status jenkins`

   ![jenkins status](./images/jenkins-status.jpg)

4. By default Jenkins server uses TCP port 8080 – open it by creating a new Inbound Rule in your EC2 Security Group

 ![jenkins inbound rule](./images/jenkins-inbound-rule.jpg)

5. Perform initial Jenkins setup.

[jenkins server browser status](http://100.26.20.73:8080)

 ![jenkins server browser](./images/jenkins-server-browser.jpg)

 *Retrieve password it from your server*

 `sudo cat /var/lib/jenkins/secrets/initialAdminPassword`

  ![customize jenkins](./images/customise-jenkins.jpg)

  *Once plugins installation is done – create an admin user and you will get your Jenkins server address*
  ### The installation is completed!

   ![jenkins complete install](./images/jenkins-complete-install.jpg)


   ### Step 2 – Configure Jenkins to retrieve source codes from GitHub using Webhooks.

   





























