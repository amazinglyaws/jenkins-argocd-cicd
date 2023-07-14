
# End to End DevOps CI using Jenkins and CD using ArgoCD

**Tools used :** _VS Code, Git/GitHub, Jenkins, AWS EC2, Shell (Unix), Python, Docker, SonarQube, K8s, ArgoCD_

## Pre-requisites
1. Install and configure Jenkins server on **AWS EC2** instance (use t2.medium and terminate to avoid any recurring charges)
2. Install and configure **Docker** on the EC2 Jenkins Server 
3. Install and configure **SonarQube** on the EC2 Jenkins Server
4. Setup a **minikube** Kubernetes cluster on AWS EC2 instance (use t2.medium)
* TODO: Use userdata for setting up the jenkins, sonarqube and docker in the AWS Ec2 instance for reuse
* TODO: Add scripts


## CI-CD Setup
1. Create a git repository for the project (this git repo will be reference in the next step)
2. Create a **Jenkins CI** pipline (using Groovy script)
3. Configure **Jenkins Runner**
4. Trigger Jenkins job using VS Code
5. Configure **Webhook** in Jenkins
6. Create and build a Python application (can be any application)
  * TODO : Add test framework for python and incorporate in the CI pipeline for automated test
7. Dockerize python applicaiton and push to Dockerhub
8. Create Kubernetes manifest file (service yaml)
9. Create a ArgoCD CD pipleine and configure git to fetch the K8s manifest
10. Connect Kubernetes node to ArgoCD
11. Trigger CD Jenkins job using CURL command and pass the variables from CI pipeline