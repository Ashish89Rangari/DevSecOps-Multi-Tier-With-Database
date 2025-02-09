# DevSecOps-Multi-Tier-With-Database
DevSecOps Practice with Multi-Tier-Application With-Database

![image](https://github.com/user-attachments/assets/609e96d2-b681-42df-bd36-6abe987537c4)




# Architecture & Flow

1.	Below is the Architecure & Flow.

2.	Every stage of Pipeline we can use security to ensure that there is no bug, vulnerabilities within the application.

3.	Best practices from security point of view , Nothing is expose such as Credentials, Passwords, Any kind of API details.

4. Git checkout creates a Local copy of source code in any CICD Tools (Jenkins,Github Actions)
   
5. COMPILE (1 st Level security) Compile stage build the code,
   it also rectifies if any syntax error for source code (Like missing of "," ";")

6. UNIT TEST CASES (2nd Level security) test cases stage is used to find application source code is working
   the same way as supposed to   (Ex: a + b = c)
   For this we have to write test cases, if the code is not working as expected then code must have bugs
   or issues in source code.

7. SonarQube (3rdLevel security):  It will perform 2 task. It also used to resolve the code smell, bug, vulnerabilities.
   a) Code Quality Check: It will  check the Quality of code, such as code can have Bugs, Vulnerabilities, Code smells.
     If this problems are less then code is good. 
   b) Code Coverage: Code coverage is nothing but if we have 100 lines of code and we have written 10 Test cases,
      This test cases should cover or test the 100 lines codes functionality.
      he percentage of code that is tested and covered by running the test cases that is called Code coverage 80% standard.
   
8. Trivy (4th Level security): a) Trivy used to scan file system ,artifacts,configuartion files.jar files, Docker Image scan.
   b) Trivy does File system scan(FS scan) such as configuration files like Kubernetes manifest YAML file, terraform files.
   It shows vulnerabilities and error in this files. If you have expose password or token credentials,Trivy will let you know that.
   c) Trivy will also scan (.jar file) depandancy check. JAVA(POM.xml),NODEJS(package.json),Python(requirements.txt).

   

9. Build Application: Build application to get JAVA(.jar), WEB(.war),NODEJS(zip) artifact files.
   
10. Publish Artifacts file: Previously scanned artifact file we can publish on Nexus or Jfrog.

11. Docker Image Build/Push: After Building Docker image , before pushing Docker image to Docker Hub, we will scan Docker image by "Trivy Image Scan".
    So It scans, Base Image(OS), Artifacts like (.jar/.war) and configuration files and dependancy.
    
12. Deploy to Kubernetes Cluster: Before Deploying to K8S cluster, The manifest file can be scan by Trivy, To setup K8S cluster we have to setup Credentials.
    We will not directly deploy with root credentials. We will create a "Service Account" and give minimum permission to deploy application.
    For that we will create a Credential, This Credentials can be used inside Jenkins to perform the deployment. This ensure that we have performed deployment
    Securely.

13. PenTesting(Penetration Testing): When application is Deployed, We manaually attack that website with various tools to find weak bug, vulnerabilities
    so that we can avoid it from hacking.
15. 
    
