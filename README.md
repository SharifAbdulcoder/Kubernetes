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
A Pod (as in a pod of whales or pea pod) is a group of one or more containers (such as Docker containers), with shared storage/network, and a specification for how to run the containers. Kubernetes Pods are mortal. They are born and when they die, they are not resurrected. You can read more at https://kubernetes.io/docs/concepts/workloads/pods/

### Pod Templates
Pod templates are pod specifications which are included in other objects. Controllers use Pod Templates to make actual pods. The sample below is a simple manifest for a Pod which contains a container that prints a message.

The structure of YAML formatted manifest contains the following 4 lines
- apiVersion
- kind
- metadata
- spec


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

## Services
In Kubernetes, a Service is an abstraction which defines a logical set of Pods and a policy by which to access them (sometimes this pattern is called a micro-service). The set of Pods targeted by a Service is usually determined by a selector.

### Defining a Service
A Service in Kubernetes is a REST object, similar to a Pod. Like all of the REST objects, you can POST a Service definition to the API server to create a new instance.
Example:

```
apiVersion: v1
kind: Service
metadata:
  name: service_name_here
spec:
  selector:
    key: value   >  (input the key:value specified in POD YAML manifest under labels)
  ports:
    - protocol: TCP
      port: 80
      targetPort: 8080
```
This specification creates a new Service object named service_name_here, which targets TCP port 8080 on any Pod with the key=value label
