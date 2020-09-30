# Managing Certificates


## Check Certificate Expiration

You can use the `crit certs list` command to check when certificates expire: 

```sh 
$ crit certs list
Certificate Authorities:
========================
Name		CN		Expires	NotAfter
ca		kubernetes	9y	2030-09-27T01:45:12Z
front-proxy-ca	front-proxy-ca	9y	2030-09-27T16:36:08Z

Certificates:
=============
Name				CN				Expires	NotAfter
apiserver			kube-apiserver			364d	2021-09-29T23:54:16Z
apiserver-kubelet-client	kube-apiserver-kubelet-client	364d	2021-09-29T23:54:16Z
apiserver-healthcheck-client	system:basic-info-viewer	364d	2021-09-29T23:54:16Z
front-proxy-client		front-proxy-client		364d	2021-09-29T23:54:17Z
```


## Renewing Certificates


### Renewing with Crit

You can use the `crit certs renew` command to renew certificates. 

```sh
$ crit certs renew
```

### Renewing  with the Kubernetes certificates API
https://kubernetes.io/docs/reference/access-authn-authz/certificate-signing-requests/
https://kubernetes.io/docs/tasks/tls/manual-rotation-of-ca-certificates/
https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-certs/
https://kubernetes.io/docs/tasks/tls/managing-tls-in-a-cluster/

## Recommendations

Should be stored out-of-band and made available through secrets management of some kind

