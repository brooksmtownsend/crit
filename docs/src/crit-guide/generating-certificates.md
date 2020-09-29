# Generating Certificates

For an overview of the certificates Kubernetes requires and how they are used, see [here](https://kubernetes.io/docs/setup/best-practices/certificates/)

### Generating a Cluster CA

To generate the cluster CA and private key: 

```sh
crit certs init --cert-dir [/path/to/dir]

```
If unsure about which `--cert-dir` to use, `/etc/kubernetes/pki` is recommended. 

### Generating CA and Certs for Etcd

Etcd certificates can be generated using our [e2d](https://github.com/criticalstack/e2d) tool. See [e2d pki](https://github.com/criticalstack/e2d#generating-certificates)

### Generating Certs and Kubeconfigs for Kubernetes Components 

The following certificates and kubeconfigs can be created with crit. See the [`crit up` command](). 

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



## Using Existing CAs

### If you don't wish to bring the CA private keys....


## Certificate Management


## Should be stored out-of-band and made available through secrets management of some kind

https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-certs/

https://kubernetes.io/docs/tasks/tls/managing-tls-in-a-cluster/
