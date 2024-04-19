# hrportal-k8s-argo-cd
This project is a Jenkins pipeline that deploys spring boot webapp into k8s cluster with argo CD. 
Steps: 
- install ArgoCD to your k8s cluster.Use ArgoCD operator from operatorhub.io. follow the installation steps in there
- Create a namaspace called argocd.
- Create a secret for dockerhub credentials in namespace argocd.
- Install Sonarqube to any accessible server. 
- Create pipleline in Jenkins.

  [Screenshot from 2024-04-19 14-39-32](https://github.com/xsantq/hrportal-k8s-argo-cd/assets/37873784/99fb71ab-9f3a-4928-b8f6-e9567d49af64)


