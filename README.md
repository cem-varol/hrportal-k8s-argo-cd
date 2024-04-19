# hrportal-k8s-argo-cd
This project is a Jenkins pipeline that deploys spring boot webapp into k8s cluster with argo CD. 
Steps: 
- install ArgoCD to your k8s cluster.Use ArgoCD operator from operatorhub.io. follow the installation steps in there
- Create a namaspace called argocd.
- Create a secret for dockerhub credentials in namespace argocd.
- Install Sonarqube to any accessible server. 
- Create pipleline in Jenkins.

  [Screenshot from 2024-04-19 14-39-32](https://github.com/xsantq/hrportal-k8s-argo-cd/assets/37873784/99fb71ab-9f3a-4928-b8f6-e9567d49af64)


Deatiled steps are: 

1. Install the necessary Jenkins plugins:
     1.1 Git plugin1.2 Maven Integration plugin
     1.3 Pipeline plugin
     1.4 Kubernetes Continuous Deploy plugin

3. Create a new Jenkins pipeline:
     2.1 In Jenkins, create a new pipeline job and configure it with the Git repository URL for the Java application.
     2.2 Add a Jenkinsfile to the Git repository to define the pipeline stages.

4. Define the pipeline stages:
      Stage 1: Checkout the source code from Git.
      Stage 2: Build the Java application using Maven.
      Stage 3: Run unit tests
      Stage 4: Run SonarQube analysis to check the code quality.
      Stage 5: Package the application into a JAR file.
      Stage 6: Deploy the application to a production environment using Argo CD.

5. Configure Jenkins pipeline stages:
      Stage 1: Use the Git plugin to check out the source code from the Git repository.
      Stage 2: Use the Maven Integration plugin to build the Java application.
      Stage 3: Run unit tests.
      Stage 4: Use the SonarQube plugin to analyze the code quality of the Java application.
      Stage 5: Use the Maven Integration plugin to package the application into a JAR file.
      Stage 8: Use Argo CD to deploy the application to a production environment.


7. Run the Jenkins pipeline:
      7.1 Trigger the Jenkins pipeline to start the CI/CD process for the Java application.

8. Login Argo CD admin UI:
     6.1 Create new Application.
     6.2 Enter git repo url
     6.3 Proivde k8s cluster url
     6.4 Provide namespace of the application that will be deployed on k8s
     6.5 Click create
     6.6 Click Sync
   
This end-to-end Jenkins pipeline will automate the entire CI/CD process for a Java application

Note: Don't forget to change the image tag with "replaceImageTag" keyword in deplpyment.yaml a
