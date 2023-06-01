# Kubernetes-based deployment project

## 1. Project Overview:

## Project goals and objectives.

- The project should aim to utilize Kubernetes to efficiently scale applications based on demand and easily handle changes in workload.
- It should use DevOps practices, such as continuous integration and continuous delivery.
- Enhance reliability and availability of applications through fault tolerance and high availability features. Which is provided by kubernetes itself.
- Ensure security and compliance by implementing best practices
- Enable monitoring and observability of applications for proactive issue identification and resolution

## Specify the scope of the deployment

1. **CI/CD Pipelines** : Setting up continuous integration and continuous delivery (CI/CD) pipelines using **Jeniks**.
2. **Version control:** Using **github** as the version control, where we keep all the kubernetes manifest files.
3. **Code Quality check :** We will use **SonarQube** for that.
4. **Manage artifact:** We will use **JFrog** to store our application and database image
5. **Containerized Applications:** Deploying them on **Kubernetes** for easier management, scalability, and portability.
6. **Enable Monitoring and Observability:** The project should aim to implement monitoring solutions such as **Prometheus and Grafana** to collect metrics, monitor the health and performance of applications, and enable proactive issue identification and resolution

## Team members

1. **Jai Prakash Bharti** - Create end to end deployment
2. **Divya Chikkala** - infrastructure provisioning

## 2. Setting Up Infrastructure:

1. Provision a virtual machine (VM) to host the Minikube/tanzu cluster.
2. Install and configure Minikube/tanzu on the VM.
3. Set up Jenkins on a separate machine or VM.

## 3. Environment Setup:

1. Create a GitHub repository to store the deployment files.
2. Configure the repository and version control system.
3. Set up SonarQube for code quality analysis and integrate it with the GitHub repository.

## 4. Container Image Management:

1. Set up JFrog Artifactory as a container registry to store the deployment images.
2. Configure the necessary repositories and permissions.
3. Integrate JFrog Artifactory with the CI/CD pipeline.

## 5. Jenkins Pipeline:

1. Develop a Jenkins pipeline using the Jenkinsfile.
2. Define stages for each step of the deployment process, such as build, test, code quality analysis, image creation, and deployment.
3. Incorporate triggers to initiate the pipeline when changes are pushed to the GitHub repository.

## 6. Deployment Configuration:

1. Create Kubernetes deployment files (e.g., YAML) to define the desired state of the deployment.
2. Store the deployment files in the GitHub repository.
3. Ensure proper configuration for scaling, networking, and other required specifications.

## 7. Integration with Minikube/Tanzu:

1. Configure Minikube/tanzu to access the GitHub repository for retrieving the deployment files.
2. Set up a connection between Jenkins and Minikube/tanzu to deploy the application.
3. Ensure Minikube is properly configured to match the required specifications of the deployment.

## 8. Monitoring Setup:

1. Install and configure Prometheus for collecting metrics from the Kubernetes cluster.
2. Set up Grafana for visualizing the collected metrics.
3. Integrate Prometheus and Grafana with the Kubernetes cluster.

## 9. Pipeline Execution and Monitoring:

1. Trigger the Jenkins pipeline when changes are pushed to the GitHub repository.
2. Monitor the pipeline execution for any errors or failures.
3. Verify code quality using SonarQube during the pipeline execution.
4. Monitor the deployed pods, services, and other Kubernetes resources using Grafana and Prometheus.

## Possible Task:

**Task1- Create infrastructure**

SubTask1 - Create VM using VmWare Esxi

SubTask2 - Install docker on it

SubTask3 - Install tanzu on it

**Task2: Create version control**

SubTask1 - Create github repo

SubTask2 - upload kubernetes manifest and jenkinsfile on github

SubTask3 - Install sonarqube server

SubTask4 - Integrate sonarqube server with github

**Task3 - Create docker image & manage it**

SubTask1 - Install JFrog Server

SubTask2 - Configure JFrog server and store our image

SubTask3- Integrate with CI/CD pipeline

**Task4 - Create kubernetes deployment manifest**

SubTask1 - Create Statefulset for hosting DB

SubTask2 - Create Deployment for hosting APP

SubTask3 - Create ConfigMap & Secret for holding credential

SubTask4 - Create Services and Ingress

**Task5: Integration of tanzu**

SubTask1 - Integration of tanzu with github

SubTask2 - Integration of tanzu with jenkins

**Task6: configure monitoring tool**

SubTask1 - Install & configure Prometheus

SubTask2 - Install & configure grafana

SubTask3 - Integrate both with kubernete cluster

**Task7: Create Jenkins pipeline**

SubTask1 - Create Jenkins pipeline with all tools

SubTask2 - test the pipeline