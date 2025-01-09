# DevSecOps-Multi-Tier-With-Database
DevSecOps Practice with Multi-Tier-Application With-Database

![image](https://github.com/user-attachments/assets/afeb7634-dfe3-4b5b-bd70-2965e0523dba)


# Architecture & Flow

1.	Below is the Architecure & Flow.

2.	Every stage of Pipeline we can use security to ensure that there is no bug, vulnerabilities within the application.

2.	Best practices from security point of view , Nothing is expose such as Credentials, Passwords, Any kind of API details.

4. Git checkout creates a Local copy of source code in any CICD Tools (Jenkins,Github Actions)
   
6. COMPILE (1 st Level security) Compile stage build the code, it also rectifies if any syntax error for source code (Like missing of "," ";")

7. UNIT TEST CASES (2nd Level security) test cases stage is used to find application source code is working the same way as supposed to   (Ex: a + b = c)
   For this we have to write test cases, if the code is not working as expected then code must have bugs or issues in source code.

8. SonarQube (3rdLevel security):  It will perform 2 task. It also used to resolve the code smell, bug, vulnerabilities.
   a) Code Quality Check: It will  check the Quality of code, such as code can have Bugs, Vulnerabilities, Code smells. If this problems are less then code is good. 
   b) Code Coverage: Code coverage is nothing but if we have 100 lines of code and we have written 10 Test cases, This test cases should cover or test the 100 lines codes functionality.
                     The percentage of code that is tested and covered by running the test cases that is called Code coverage 80% standard.
   
9. Trivy (4th Level security): Trivy used to scan file system ,artifacts,configuartion files.jar files, Docker Image scan.
   Trivy does File system scan(FS scan) such as configuration files like Kubernetes manifest YAML file, terraform files.
   It shows vulnerabilities and error in this files
11. ss
    
