# Role-and-RoleBinding-in-Kubernetes
Role and Role binding in Kubernetes will help to assign role within a specific namespace with certain permissions

WHAT IS ROLE?
Role is an access policy “rules of resources” that means you have a resource and you will be defining access policies which is like scope is namespace so role is always limited to the namespace.
For example- “reader role in default namespace” this means that i wanted to create “reader” role in default namespace or I wanted to create a role with “configmap update” in default namespace. 
First, you have to create a namespace
...
kubectl create namesapce testing
...
