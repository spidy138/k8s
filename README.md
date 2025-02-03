#k8s resources
Hey, welcome to the world of kubernetes. I hope this page will provide you a great learning experience .
##Introduction
Kubernetes, also known as k8s, is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications. It provides a way to abstract the underlying infrastructure and manage applications at scale, while also offering flexibility, portability, and a rich feature set

##Key Concepts of Kubernetes
Cluster: A group of nodes (machines) that run containerized applications.
Node: A physical or virtual machine in the cluster that runs containers.
Pod: The smallest and simplest Kubernetes object that represents a single container or a set of closely related containers.
Service: An abstraction that defines a set of Pods and a policy to access them.
Deployment: A controller that manages the deployment of Pods, including updates and scaling.
DaemonSet: Ensures that a copy of a Pod is running on all or selected nodes.
StatefulSet: Similar to Deployments, but it provides guarantees about the ordering and uniqueness of Pods.
Persistent Volume (PV): A piece of storage in the Kubernetes cluster
Persistent Volume Claim (PVC):  A request for storage by a user. PVCs allow you to request specific amounts of storage and access modes without needing to know the specifics of the underlying storage system.

###Pod
A Pod is the basic execution unit in Kubernetes. It contains one or more containers that are tightly coupled and share the same network namespace, which allows them to communicate easily with each other.
###Services
A Service is an abstraction layer that defines a policy to access Pods. Services allow Pods to communicate with each other and with external systems.
###Deployments
A Deployment provides declarative updates to Pods and ReplicaSets. It allows you to manage the lifecycle of Pods, including scaling, rolling updates, and rollbacks.
###DaemonSet
A DaemonSet ensures that a specific Pod is running on all or a selected set of nodes in the cluster. It is used for running background processes such as logging agents or monitoring.
###StatefulSet
A StatefulSet is used for applications that require persistent storage, stable network identities, and ordered deployments. It's typically used for databases and other stateful applications.
StatefulSet provides each Pod with a stable network identity, which is useful for applications that need to track the identity of their instances (like databases).
StatefulSets use Persistent Volume Claims (PVC) to bind each Pod to a specific storage volume.
StatefulSets ensure that Pods are deployed in order (e.g., Pod-0, Pod-1, Pod-2).
###PV
PVs exist beyond the Pod lifecycle, meaning data is retained even if the Pod is deleted.
PVs can be provisioned statically by the administrator or dynamically via storage classes.
PVs Define how the volume can be mounted (e.g., ReadWriteOnce, ReadOnlyMany, ReadWriteMany).
###PVC
PVCs are bound to a matching PV that satisfies the requested storage capacity and access modes.
PVCs can request storage from a specific StorageClass, which defines the type of underlying storage.
PVCs can automatically provision storage if configured correctly with StorageClass.


##Setting up kubernetes cluster
To set up a Kubernetes cluster, you need to choose a deployment environment, install Kubernetes components on each node, configure networking using a plugin, initialize the master node with kubeadm init, join worker nodes using kubeadm join, deploy applications with manifests, and manage the cluster using kubectl or a management tool

refer [medium setup kubernetes cluster in debian](https://medium.com/@achyuth.payani2000/microcks-mock-api-server-in-kubernetes-d2382d14510a)









