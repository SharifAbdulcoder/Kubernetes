# Kubernetes
Kubernetes (K8s) is an open-source system for automating deployment, scaling, and management of containerized applications

## Services & Resources in Kubernetes
We will go through the simplest way of using Kubernetes. We will create services & resources. Examples:
- Pods
- Service
- Deployment
- Daemon-sets
- Persistent Volume
- Persistent Volume Claim
- Secrets
- Config-Maps
- Load-balancer

### Prerequisites
We will use GCP(Google Cloud Platform) K8S for this overview of Kubernetes services

- If you already have 'Gmail' account then head over to https://cloud.googe.com and setup your GCP account. If not you'll need to create Gmail account then setup your GCP account.
Keep in mind, google will provide $300 credit for new users on GCP. So you won't need to work about expenses.

- After setting up your GCP account create kubernetes cluster. By going;
  - Clicking on menu on left top corner
  - Select Kubernetes Cluster or Kubernetes Engine
  - Click on Create Cluster

- Access your Kubernetes Cluster and you are good to start.  


## Pods
A Pod (as in a pod of whales or pea pod) is a group of one or more containers (such as Docker containers), with shared storage/network, and a specification for how to run the containers
