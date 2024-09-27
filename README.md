# jenkins-projects

I am going to install jenkins on a local ubuntu vm, it can be it hosted locally or on any cloud platform like AWS/Azure/GCP etc.

**Install Jenkins on Ubuntu**

**Pre-Requisites:**

**Java (JDK)**

Run the below commands to install Java and Jenkins.

**Install Java**

**sudo apt update**

**sudo apt install openjdk-17-jre**

Verify Java is Installed by using:


**java -version**


Now, we can proceed with installing Jenkins.


**curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null**
  
**sudo apt-get update**

**sudo apt-get install jenkins**

Start the Jenkins service and confirm the status.

**sudo systemctl start jenkins.service**

**sudo systemctl status jenkins**

**Login to Jenkins using the below URL:**

**http://localhost:8080**


After you login to Jenkins, Run the command to view the Jenkins Admin Password and Enter the Administrator password.

**sudo cat /var/lib/jenkins/secrets/initialAdminPassword**

<img width="959" alt="image" src="https://github.com/user-attachments/assets/59d33ba3-b200-4fd2-a1c6-eb8a78328d2b">



**Click on Install suggested plugins**

<img width="959" alt="image" src="https://github.com/user-attachments/assets/aada6e7a-d0da-4d3b-9bc5-743e6bf8d354">

Wait for the Jenkins to Install suggested plugins

<img width="959" alt="image" src="https://github.com/user-attachments/assets/f9086899-325e-4c4d-923a-b9a2fbccd497">


Create First Admin User with necesaary details or Skip the step  [If you want to use this Jenkins instance for future use-cases as well, better to create admin user]


<img width="959" alt="image" src="https://github.com/user-attachments/assets/e07c1bdc-3c00-4c72-a45b-b99f321e6a70">

<img width="959" alt="image" src="https://github.com/user-attachments/assets/81e201d6-ff7c-4a5e-accf-c0b25a678623">

Click Start using Jenkins to visit the main Jenkins dashboard:

<img width="959" alt="image" src="https://github.com/user-attachments/assets/117b946b-282d-4a27-85c6-095c7d9a2391">

**Install the required plugins in Jenkins:**

Log in to Jenkins.

Go to Manage Jenkins > Manage Plugins.

In the Available tab, search for a specific plugin like "Docker Pipeline".

Select the plugin and click the Install button.

Restart Jenkins after the plugin is installed.

Wait for the Jenkins to be restarted.


