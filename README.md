🚀 Kubernetes Deployment – DevOps Hands-On Project

Overview

This repository showcases my hands-on experience as a DevOps Engineer working with Kubernetes. It demonstrates a complete deployment lifecycle — from creating a YAML file and running a multi-pod deployment, to scaling, simulating a faulty update, and performing a rollback.

The goal is to illustrate real-world DevOps practices using declarative configuration, version control, and cluster management.

🛠️ What This Project Covers

    • ✅ Creating a Kubernetes Deployment using a YAML manifest
    • ✅ Running the deployment with 20 pods
    • ✅ Scaling the deployment up to 20 pods, then down to 7
    • ✅ Simulating a bad update (e.g., broken image or misconfiguration)
    • ✅ Performing a rollout rollback to the previous stable version
    • ✅ Verifying the rollback and restoring service health
    
📁 Repository Structure

├── deployment.yaml          # Initial deployment manifest

├── bad-update.yaml          # Simulated faulty update

├── README.md                # Project documentation

🧪 Step-by-Step Workflow

1. Create and Apply Deployment
   
kubectl apply -f deployment.yaml

    • Deploys 80 replicas of a containerized app (e.g., nginx)
    • Uses labels and selectors for pod management
      

2. Scale the Deployment
   
kubectl scale deployment my-deployment --replicas=100
kubectl scale deployment my-deployment –replicas=70

    • Demonstrates horizontal scaling
    • Useful for traffic spikes or resource optimization

3. Simulate a Bad Update
   
kubectl apply -f bad-update.yaml

    • Introduces a broken image or misconfigured container
    • Causes pods to crash or fail readiness checks
    
4. Roll Back to Previous Version
   
kubectl rollout undo deployment my-deployment

    • Reverts to the last working configuration
    • Ensures service availability and stability

5. Verify Rollback

kubectl rollout status deployment my-deployment
kubectl get pods

    • Confirms that healthy pods are running
    • Validates successful rollback


🎯 Skills Demonstrated

    • Kubernetes Deployment & Scaling
    • YAML Configuration
    • Rollouts and Rollbacks
    • Cluster Health Monitoring
    • CI/CD Readiness
    • Troubleshooting and Recovery
    
📚 Resources
  
Kubernets Docs-Deployment 
https://kubernetes.io/docs/concepts/workloads/controllers/deployment/

Kubernetes Docs-Rollouts
https://kubernetes.io/docs/concepts/workloads/controllers/deployment/#updating-a-deployment



🤝 Connect


If you found this project helpful or want to collaborate. Please consider the below factors while contributing

-Code Style:
Maintain a consistent code style for readability.

-Documentation:
Ensure well-documented code for effective collaboration.

-Testing:
Thoroughly test your changes before submitting a pull request.

-Issue Tracker:
Check the Issue Tracker for tasks.

-Code Review:
All contributions undergo a code review process.

-Licensing:
Contributions are licensed.
