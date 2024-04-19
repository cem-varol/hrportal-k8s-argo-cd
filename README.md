# hrportal-k8s-argo-cd
This project is a Jenkins pipeline that deploys spring boot webapp into k8s cluster with argo CD. 
Steps: 
- install ArgoCD to your k8s cluster.Use ArgoCD operator from operatorhub.io. follow the installation steps in there
- Create a namaspace called argocd.
- Create a secret for dockerhub credentials in namespace argocd.
- Install Sonarqube to any accessible server. 
- Create pipleline in Jenkins.

