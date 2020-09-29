# Managing Certificates

```sh
/etc/kubernetes/
├── admin.conf
├── controller-manager.conf
├── kubelet.conf
├── pki
│   ├── apiserver-healthcheck-client.crt
│   ├── apiserver-healthcheck-client.key
│   ├── apiserver-kubelet-client.crt
│   ├── apiserver-kubelet-client.key
│   ├── apiserver.crt
│   ├── apiserver.key
│   ├── auth-proxy-ca.crt
│   ├── auth-proxy-ca.key
│   ├── ca.crt
│   ├── ca.key
│   ├── front-proxy-ca.crt
│   ├── front-proxy-ca.key
│   ├── front-proxy-client.crt
│   ├── front-proxy-client.key
│   ├── sa.key
│   └── sa.pub
└── scheduler.conf
```

## Should be stored out-of-band and made available through secrets management of some kind

https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-certs/

https://kubernetes.io/docs/tasks/tls/managing-tls-in-a-cluster/
