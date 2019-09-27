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
A Pod (as in a pod of whales or pea pod) is a group of one or more containers (such as Docker containers), with shared storage/network, and a specification for how to run the containers. You can read more at https://kubernetes.io/docs/concepts/workloads/pods/

### Pod Templates
Pod templates are pod specifications which are included in other objects. Controllers use Pod Templates to make actual pods. The sample below is a simple manifest for a Pod which contains a container that prints a message.

```
apiVersion: v1
kind: Pod
metadata:
  name: pod_name_here
  labels:
    key: value
spec:
  containers:
  - name: container_name_here
    image: image_name_here:version
```

The structure of YAML formatted manifest contains the following 4 lines
- apiVersion
- kind
- metadata
- spec
