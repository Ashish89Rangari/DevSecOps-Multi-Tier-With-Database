# DevSecOps-Multi-Tier-With-Database
DevSecOps Practice with Multi-Tier-Application With-Database

# Architecture & Flow

1.	Below is the Architecure & Flow.

2.	Every stage of Pipeline we can use security to ensure that there is no bug, vulnerabilities within the application.

2.	Best practices from security point of view , Nothing is expose such as Credentials, Passwords, Any kind of API details.

4. Git checkout creates a Local copy of source code in any CICD Tools (Jenkins,Github Actions)
   
6. COMPILE (1 st Level security) Compile stage build the code, it also rectifies if any syntax error for source code (Like missing of "," ";")

7. UNIT TEST CASES (2nd Level security) test cases stage is used to find application source code is working the same way as supposed to
