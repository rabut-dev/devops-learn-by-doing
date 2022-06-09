Kubelet Security:

    10250: Full access, 10255: unauthenticated read-only access
    
    --anonymous-auth=<flag> on kubelet-service or authentication on kubelet-config.ymal config to control the kubelet access

    Kubelet supports certificate(x509) or API Bearer Token authentication.

    Access also can be controlled using certificates(x509) by defining the client ca cert

    Default Kubelet Authorization mode is AlwaysAllow

    readOnlyPort set this to 0 for authenticated read-only access


By default api-server available on 6443 port

Network Policies:
    
    ingress / egress selectors: 
         podSelector - Allow set of pod with the lables ex. app = web-server
         namespaceSelector - Allow pods on a given namespace ex. prod
         ipBlock - Allow access from a given ip range or cidr block which could be external to your cluster cluster.

Docker: 
    
    some of the environment vairables used by Docker
    DOCKER_HOST
    DOCKER_TLS

    Docker host can also be defined within daemon configuration file.


