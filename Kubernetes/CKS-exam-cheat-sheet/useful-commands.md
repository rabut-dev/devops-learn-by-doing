## CKS Usefull Commands


|Command|Description|
|------|-----------|
|`kubectl certificate <attribute> <csr-request-name>`| attribute: approve or deny, the CSR request.|
|`openssl x509 in <cert-path> -text -noout`| Describe and check certificate details|
|`kubectl config view --kubeconfig=<file-path>`| View config file details where "kubeconfig" attribute is optional|
|`kubectl config use-context <context-name>`| Change context for kube config|
|`curl http://api-server-path:6443 -k`| View available APIs, you may also need to pass key, cert, cacert as attributes for authentication|
|`curl http://api-server-path:6443/apis -k |grep name`| View available APIs within named API "apis"|
|`kubectl proxy`| Create local proxy server at port 8001|
|`kubectl auth can-i <action> <resource>`| Check if the user has the access to create/update/list/get//delete given resources(pod etc)|