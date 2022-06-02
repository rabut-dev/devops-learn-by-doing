## CKS Usefull Commands


|Command|Description|
|------|-----------|
|`kubectl certificate <attribute> <csr-request-name>`| attribute: approve or deny, the CSR request.|
|`openssl x509 in <cert-path> -text -noout`| Describe and check certificate details|
|`kubectl config view --kubeconfig=<file-path>`| View config file details where "kubeconfig" attribute is optional|
|`kubectl config use-context <context-name>`| Change context for kube config|
|`curl http://api-server-path:6443 -k`| View available APIs, you may also need to pass key, cert, cacert as attributes for authentication|
|`curl http://api-server-path:6443/apis -k`| View available APIs within named API "apis"|
|`kubectl proxy`| Create local proxy server at port 8001 to access the api-server and subsequently all the underlying services and applications|
|`curl -sk http://localhost:8001/version`| After creating proxy, access the api-server version on localhost through 8001 port|
|`kubectl port-forward <service\/pod> <port:svc\/pod port>`| Another way to expose\/access service\/pod locally i.e local\/host port to a port on the service or pod|
|`kubectl auth can-i <action> <resource>`| Check if the user has the access to create/update/list/get//delete given resources(pod etc)|
|`kubectl api-resources --namespaced=<flag>`| List API Resources with namespace scope, where flag=true or false|
|`kubectl get <resource> --as <username>`| Get the details of a given Kubernetes Resource as a specific user|
|`ps -aux \| grep kubelet`| Get the details of a running process|
|`sha512sum <package-file-name>`| Generate checksum for platform binaries for verification before deploying, on linux|
|`kubectl drain <node-name>`| Move workloads to other worker nodes for upgrade activities or debugging purpose|
|`kubectl uncordon <node-name>`| Allow workloads again after upgrade activities|

## Cluster Upgrade

|Command|Description|
|------|-----------|
|`/var/lib/kubelet/kubelet-config.yaml`| Default location for Configurable Kubelet Options|

## CKS Usefull Locations


|Location or File|Description|
|------|-----------|
|`/var/lib/kubelet/kubelet-config.yaml`| Default location for Configurable Kubelet Options|
|`/usr/local/bin/kubelet`| Default location for a running kubelet service (kubelet.service)|

## Usefull References 


K8s Release Notes: 
https://github.com/kubernetes/kubernetes/tree/master/CHANGELOG