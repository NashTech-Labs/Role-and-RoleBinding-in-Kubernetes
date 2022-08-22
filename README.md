# Role-and-RoleBinding-in-Kubernetes
Role and Role binding in Kubernetes will help to assign role within a specific namespace with certain permissions

WHAT IS ROLE?

Role is an access policy “rules of resources” that means you have a resource and you will be defining access policies which is like scope is namespace so role is always limited to the namespace.
For example- “reader role in default namespace” this means that i wanted to create “reader” role in default namespace or I wanted to create a role with “configmap update” in default namespace. 

### First, you have to create a namespace

`kubectl create namespace testing`

### Verify the namespace

`kubectl get namespaces`

### Create a service account within the namespace(in my case the namesapce is testing, you can write any name of your choice)

`kubectl create serviceaccount test-account -n testing`

This is the imperative way of creating service account, you can also use the yaml file present in the repository with name [svc-acc.yaml]

### Check the service account

`kubectl get serviceaccounts`

### Describe the service account for more information

`kubectl describe serviceaccounts test-account -n testing`

### Now create a Role

`kubectl create role my-role -n testing --verb=create --resource=secret --resource=configmap`

You can write yaml file also to create this role [check role.yaml in repository]
