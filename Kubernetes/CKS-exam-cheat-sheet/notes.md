Kubelet Security:

    10250: Full access, 10255: unauthenticated read-only access
    
    --anonymous-auth=<flag> on kubelet-service or authentication on kubelet-config.ymal config to control the kubelet access

    Kubelet supports certificate(x509) or API Bearer Token authentication.

    Access also can be controlled using certificates(x509) by defining the client ca cert

    Default Kubelet Authorization mode is AlwaysAllow

    readOnlyPort set this to 0 for authenticated read-only access