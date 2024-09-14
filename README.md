# Project Title

React.js Application with AWS DynamoDB: Automated DevOps Pipeline on EKS with Terraform and ArgoCD
## Description:

This project showcases the deployment of a React.js application using AWS DynamoDB as its backend database, integrating a comprehensive DevOps pipeline to ensure seamless continuous integration, continuous deployment (CI/CD), security scanning, and monitoring. The project employs a variety of DevOps tools and cloud services, including GitHub, Jenkins, Docker, AWS ECR, Terraform, Helm, ArgoCD, and monitoring solutions like Prometheus and Grafana, to deliver a secure, scalable, and automated deployment on an Amazon EKS cluster.

## Tools and Technologies Used
- React.js
- AWS DynamoDB
- GitHub
- Jenkins
- Docker
- AWS Elastic Container Registry (ECR)
- SonarQube
- Trivy FS Scan
- Trivy Image Scan
- Amazon Elastic Kubernetes Service (EKS
- Jump Server (Bastion Host)
- AWS Elastic Load Balancer (ELB)
- Helm
- ArgoCD
- Prometheus
- Grafana

## Pipeline Flow Diagram
![P02](https://github.com/user-attachments/assets/70e6f107-a8b7-4114-b192-263a88a0df1d)



## Components and Tools Used

### React.js Application with AWS DynamoDB:

A frontend application built using React.js, which interacts with AWS DynamoDB to perform CRUD operations. DynamoDB serves as the NoSQL database for managing the application's data needs.

### Source Control with GitHub:

GitHub is used for version control, source code management, and collaboration. It is integrated with Jenkins to trigger automated pipelines based on commits and pull requests.

### CI/CD Pipeline with Jenkins:

Jenkins automates the CI/CD pipeline to handle the build, test, and deployment processes for the React.js application. The Jenkins pipeline is defined using a Jenkinsfile that includes stages for building, testing, security scanning, and deployment.

The pipeline uses Jenkins agents to handle different tasks, ensuring a consistent and isolated environment for building and deploying the application.

### Infrastructure as Code (IaC) with Terraform:

Terraform is used to create and manage the infrastructure for the project, including the Amazon Elastic Kubernetes Service (EKS) cluster. Terraform scripts define the desired state of AWS resources, making the infrastructure reproducible and version-controlled.

### Containerization with Docker and Image Management with AWS Elastic Container Registry (ECR):

The React.js application is containerized using Docker, ensuring consistent environments across development, testing, and production.

Docker images are built as part of the CI pipeline and stored in AWS ECR, providing a secure and scalable image repository.

### Code Quality and Security with SonarQube and Trivy:

**SonarQube:** Integrated with Jenkins for static code analysis to ensure code quality and detect potential bugs, code smells, and vulnerabilities.

**Trivy FS Scan:** Scans the source code and file system for vulnerabilities and misconfigurations in dependencies.

**Trivy Image Scan:** Conducts security scans on Docker images to detect vulnerabilities before they are pushed to AWS ECR or deployed to the EKS cluster.

### Kubernetes Orchestration with Amazon EKS and Helm:

Amazon EKS (Elastic Kubernetes Service) is used for orchestrating the containerized React.js application. It provides a scalable and managed Kubernetes environment.

**Helm:** Helm charts are used to package and manage Kubernetes deployments, simplifying the process of updating and rolling back releases.

### Github with ArgoCD:

ArgoCD is employed to implement Github for continuous delivery. It automates the deployment of applications to the Kubernetes cluster by continuously monitoring changes in the Git repository and synchronizing them with the desired state defined in Helm charts.

### Secure Access via Jump Server (Bastion Host):

A Jump Server (Bastion Host) is set up to securely access the Amazon EKS cluster and other AWS resources, providing a controlled entry point for administrative tasks.

### Traffic Management with AWS Elastic Load Balancer (ELB):

An AWS Elastic Load Balancer distributes incoming traffic across multiple pods running on the EKS cluster, ensuring high availability, fault tolerance, and efficient load balancing.

### Monitoring and Observability with Prometheus and Grafana:

**Prometheus:** Deployed in the EKS cluster to collect and store metrics from the application and Kubernetes components, providing visibility into system performance and resource usage.

**Grafana:** Integrated with Prometheus to visualize metrics through interactive dashboards, enabling real-time monitoring, alerting, and proactive issue management.

## Project Workflow:

### Source Code Management:

Developers commit changes to the GitHub repository, triggering the Jenkins pipeline automatically.

### CI/CD Pipeline Execution:

***Build and Test:** Jenkins builds the Docker image for the React.js application and runs tests to validate code quality.

**Code Quality and Security Scanning:** SonarQube performs static code analysis, and Trivy scans the file system and Docker images for vulnerabilities.

### Docker Image Management:

Docker images are built and pushed to AWS ECR after passing all security and quality checks, enabling easy deployment to the Kubernetes cluster.

### Infrastructure Provisioning with Terraform:

Terraform scripts are used to provision and manage the EKS cluster, load balancer, and other necessary AWS resources, ensuring a reproducible and scalable infrastructure setup.

### Deployment to EKS using Helm and ArgoCD:

Helm charts are used to define the Kubernetes resources for the React.js application.

ArgoCD continuously monitors the Github repository and automatically deploys changes to the EKS cluster.

### Traffic Routing and Load Balancing:

AWS Elastic Load Balancer routes incoming traffic to the appropriate pods in the EKS cluster, ensuring smooth traffic management and high availability.

### Monitoring

Prometheus collects metrics from the application and cluster components, while Grafana visualizes these metrics.


### Jenkins Overview
![Screenshot (182)](https://github.com/user-attachments/assets/3bf6b84b-f25a-4a68-b13f-3985c404d2d8)


### Tools Installation Jenkins Server
![Screenshot (30)](https://github.com/user-attachments/assets/d057249c-b691-492d-9d44-7c2e2e8e3c61)

### Jenkins Credentials
![Screenshot (31)](https://github.com/user-attachments/assets/561213d8-3af2-4476-bf78-76131bcc3b5a)
![Screenshot (32)](https://github.com/user-attachments/assets/d840fc51-4143-4446-8427-abcb8b6b4768)
![Screenshot (33)](https://github.com/user-attachments/assets/3a7c45a8-7348-4be8-97a3-cc627908d650)

### AWS S3 Bucket Creation
![Screenshot (35)](https://github.com/user-attachments/assets/ae03c40b-9b48-445a-a96d-c32ff96823e4)
![Screenshot (34)](https://github.com/user-attachments/assets/30e89777-6c4f-4ab6-b92d-6ead74b898d3)
![Screenshot (36)](https://github.com/user-attachments/assets/4cae59e2-db75-400a-9f2b-babcd617f950)

### Terraform Amazon EKS Creation Via Jenkins Pipeline
![Screenshot (41)](https://github.com/user-attachments/assets/06418281-c7f2-427a-9759-e2c7f2ba3467)
![Screenshot (37)](https://github.com/user-attachments/assets/d08c810f-dc34-4c45-a740-d758b2a04d31)
![Screenshot (40)](https://github.com/user-attachments/assets/f413ddd1-123b-4f7d-ba0b-8dd243467eb9)
![Screenshot (42)](https://github.com/user-attachments/assets/d4bb9cb7-71e5-4031-9f0b-4e44f540a6be)

![Screenshot (47)](https://github.com/user-attachments/assets/5ef62c9f-c649-42f1-88d3-ca41d1e038d1)
![Screenshot (48)](https://github.com/user-attachments/assets/5c40015e-4235-49bd-98a3-0a9149d87785)
![Screenshot (199)](https://github.com/user-attachments/assets/27f2a632-b11a-4b15-9bd8-eb1247d50df2)

### AWS S3 Bucket OUTPUT
![Screenshot (188)](https://github.com/user-attachments/assets/bf8e0721-23d3-4ffb-ac5f-d2907d57b7e9)


### Jump Server Based on EKS VPC and Tools Install
![Screenshot (43)](https://github.com/user-attachments/assets/65d26d53-fa11-4d11-962d-4cdcd718ceb8)
![Screenshot (44)](https://github.com/user-attachments/assets/c8e08067-53a4-4df5-b1ce-eda115fccbf7)
![Screenshot (45)](https://github.com/user-attachments/assets/39759502-8461-4595-8f49-1312cf5d1fac)
![Screenshot (46)](https://github.com/user-attachments/assets/e4386c11-1f2b-4664-8b58-563e728cb871)
![Screenshot (50)](https://github.com/user-attachments/assets/f2d69a08-7a5b-4a3d-b810-2bcc95a55de7)

### AWS Load Balancer Controller Installation
![Screenshot (53)](https://github.com/user-attachments/assets/2cb1aa73-6d9a-4ead-ace6-6478a9285f77)
![Screenshot (58)](https://github.com/user-attachments/assets/c71b5437-ca74-4674-bc8a-4880c08fe69f)
![Screenshot (59)](https://github.com/user-attachments/assets/2cca6067-f7ef-487f-a51e-185f3e5d9892)
![Screenshot (60)](https://github.com/user-attachments/assets/96354741-a9a6-4664-8336-733f2c2966a8)
![Screenshot (61)](https://github.com/user-attachments/assets/431870b2-cee7-4525-b099-1921dd863e27)
![Screenshot (62)](https://github.com/user-attachments/assets/5e7ef0b4-11d3-480f-95ec-d4f0fc89ba66)

### AWS Dynamodb Creation
![Screenshot (39)](https://github.com/user-attachments/assets/92b05af4-6f44-442d-bd3f-e8c5422766ad)

### Argocd Installation
![Screenshot (63)](https://github.com/user-attachments/assets/57a67eb5-c465-4d8f-9f05-57f97d7782f5)
![Screenshot (65)](https://github.com/user-attachments/assets/0aa37ac1-5ff2-4a26-b8b3-e217f3abdaf2)
![Screenshot (67)](https://github.com/user-attachments/assets/4c530b8b-d75d-45e2-978a-676275e36bde)
![Screenshot (69)](https://github.com/user-attachments/assets/c5d559bd-70e4-49c6-98d9-ca52dd595865)
![Screenshot (71)](https://github.com/user-attachments/assets/3d7a3000-f323-4ec1-bbec-b1ad6320718c)
![Screenshot (72)](https://github.com/user-attachments/assets/98641194-6e9d-4cbd-a70b-8b2ce886d9fb)
![Screenshot (73)](https://github.com/user-attachments/assets/b4053bdb-5c07-4df4-8bae-e507a2eaa30a)

### Sonarqube Setup
![Screenshot (74)](https://github.com/user-attachments/assets/b02b85a3-9433-45ac-bcb0-77745f4a2241)
![Screenshot (75)](https://github.com/user-attachments/assets/e0380489-b4e9-4f61-91a6-0d878c887e34)
![Screenshot (76)](https://github.com/user-attachments/assets/9f709bc2-5f2b-4c73-9855-9bc6d87d046c)
![Screenshot (78)](https://github.com/user-attachments/assets/c91ca19b-b158-4661-86b3-3cba9b48acad)
![Screenshot (80)](https://github.com/user-attachments/assets/ee382e55-0fe2-4f41-a1d5-c3494f4402f0)
![Screenshot (81)](https://github.com/user-attachments/assets/b4b5e036-55b5-48fd-a7e7-281b4e25bf9e)

### Jenkins Setup Pipeline Job For Frontend and Backend
![Screenshot (87)](https://github.com/user-attachments/assets/f25d6201-4b2c-404e-a12c-040e376e1c4d)
![Screenshot (88)](https://github.com/user-attachments/assets/ee408fca-e4b7-4a09-983f-41dff279eb51)
![Screenshot (104)](https://github.com/user-attachments/assets/4ff78555-03af-4ba8-8ca4-990944f096b1)
![Screenshot (94)](https://github.com/user-attachments/assets/8320789d-7eab-4116-9688-5cb2d85288e9)

### AWS ECR repository OUTPUT
![Screenshot (112)](https://github.com/user-attachments/assets/100d9d0a-832e-4b96-b8d8-8ae92739eb3d)
![Screenshot (111)](https://github.com/user-attachments/assets/c873c102-4111-46a4-b161-baa2eb9d28db)
![Screenshot (96)](https://github.com/user-attachments/assets/2db8d049-d917-4289-a670-5e59e278c09d)

### Sonarqube Scanning 
![Screenshot (107)](https://github.com/user-attachments/assets/08e76bdf-018f-40fe-94ef-fcdf9f25e156)
![Screenshot (92)](https://github.com/user-attachments/assets/6d2ab355-cd1b-4ace-85db-7f7b09c68bc2)
![Screenshot (101)](https://github.com/user-attachments/assets/a1e24b34-0fb9-4bb3-8c2b-22bb74f97811)

### Argocd OUTPUT
![Screenshot (171)](https://github.com/user-attachments/assets/ed1ec3c7-db07-4e1f-bfc2-12b4d2b813d8)
![Screenshot (168)](https://github.com/user-attachments/assets/c840ecbd-9b55-4ba3-a9b7-f9112ff8329a)
![Screenshot (169)](https://github.com/user-attachments/assets/00dbfaba-505f-4a43-a861-ec05fb6a45ac)
![Screenshot (167)](https://github.com/user-attachments/assets/207b2504-1247-4c6b-b245-410301efdb40)


### Monitoring Tools Install
![Screenshot (139)](https://github.com/user-attachments/assets/dd124583-1033-41f8-8c37-dba70a494477)
![Screenshot (143)](https://github.com/user-attachments/assets/04bddf7f-e3d3-432b-be73-9b4503955c2e)

### Jump Server OUTPUT
![Screenshot (178)](https://github.com/user-attachments/assets/bbec4df4-dc22-41c9-ac28-15e17f2a624c)
![Screenshot (180)](https://github.com/user-attachments/assets/39f4c17c-47a9-4b3f-9079-8863547019e2)
![Screenshot (202)](https://github.com/user-attachments/assets/5bb3239e-f7d1-4b52-bcbd-c1b469895147)


### Application OUTPUT
![Screenshot (137)](https://github.com/user-attachments/assets/9a372132-0565-4f32-9280-f2b742cd83ba)

### Monitoring OUTPUT
![Screenshot (144)](https://github.com/user-attachments/assets/91ce1109-1c5e-467e-9e7b-f277a38804e3)
![Screenshot (147)](https://github.com/user-attachments/assets/f2eb7e58-a5d1-4655-ad51-08a7dba1e6d4)
![Screenshot (150)](https://github.com/user-attachments/assets/05d71013-bba1-46c0-8849-a685ec05f264)
![Screenshot (157)](https://github.com/user-attachments/assets/da48818e-637d-4e4c-8a4a-b202c9e2e5c8)
![Screenshot (191)](https://github.com/user-attachments/assets/42652fdf-73dd-4c1f-8d1e-549b818c6a0e)
![Screenshot (190)](https://github.com/user-attachments/assets/7c3214ec-4376-4608-bd56-333842c86ad2)

**This project provides an end-to-end DevOps solution for deploying a React.js application with AWS DynamoDB on an Amazon EKS cluster, managed through Terraform. The integration of tools like Jenkins, Docker, SonarQube, Trivy, Helm, and ArgoCD, along with monitoring solutions like Prometheus and Grafana, ensures a secure, automated, and scalable deployment process. By leveraging Github with ArgoCD and IaC with Terraform, the project achieves a modern cloud-native architecture for continuous delivery and infrastructure management.**





# **Thank you.......**
