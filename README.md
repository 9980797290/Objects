 KUBERNETES OBJECT MOBEL


Five types of Object model:-
1. Namespace
2. POD
3. Replicaset
4. Deployment
5. Service

NAMESPACE:-

1. Namespaces are a way to organize clusters into virtual sub-clusters
2. Namespace is like a package name, Logical partionaning of the kubernities cluster is said to be Namespace.
3. Any resource that exists within Kubernetes exists either in the default namespace or a namespace that is created by the cluster operator
4. Namespaces cannot be nested inside one another and each Kubernetes resource can only be in one namespace.
5. Namespaces provide a scope for names. Names of resources need to be unique within a namespace, but not across namespaces.
6. To create namespace ,  my-namespace.yaml
7. To Run namespace - kubectl create -f ./my-namespace.yaml

8. To list the namespace in Cluster we should use below command 
         kubectl get namespaces
9. To delete Namespace - kubectl delete namespaces <insert-some-namespace-name>



PODS:-
Pods are the smallest deployable units of computing that you can create and manage in Kubernetes. 
A Pod is a group of one or more containers, with shared storage and network resources, and a specification for how to run the containers.
A Pod's contents are always co-located and co-scheduled, and run in a shared context.
A Pod models an application-specific "logical host": 
it contains one or more application containers which are relatively tightly coupled.
In non-cloud contexts, applications executed on the same physical or virtual machine are analogous to cloud applications executed on the same logical host.

REPLICA SET:-
Replica Set A ReplicaSet's purpose is to maintain a stable set of replica Pods running at any given time.
As such, it is often used to guarantee the availability of a specified number of identical Pods.
A ReplicaSet is defined with fields, including a selector that specifies how to identify Pods it can acquire, a number of replicas indicating how many Pods it should be maintaining, and a pod template specifying the data of new Pods it should create to meet the number of replicas criteria.
A ReplicaSet then fulfills its purpose by creating and deleting Pods as needed to reach the desired number.
 When a ReplicaSet needs to create new Pods, it uses its Pod template.




Deployment
A Deployment provides declarative updates for Pods and ReplicaSets.
You describe a desired state in a Deployment, and the Deployment Controller changes the actual state to the desired state at a controlled rate.
You can define Deployments to create new ReplicaSets, or to remove existing Deployments and adopt all their resources with new Deployments.

