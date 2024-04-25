# kuberneetzzzz

## rhel8 install

``` bash
sestatus
sudo sed -i 's/^SELINUX=enforcing$/SELINUX=permissive/' /etc/selinux/config
reboot
sestatus # should be permissive now
sudo dnf install -y iproute-tc
```

Download some bins:
```
curl -LO https://dl.k8s.io/release/v1.30.0/bin/linux/amd64/kubectl
curl -LO https://dl.k8s.io/release/v1.30.0/bin/linux/amd64/kube-apiserver
curl -LO https://dl.k8s.io/release/v1.30.0/bin/linux/amd64/kube-controller-manager
curl -LO https://dl.k8s.io/release/v1.30.0/bin/linux/amd64/kube-scheduler
curl -LO https://dl.k8s.io/release/v1.30.0/bin/linux/amd64/kubelet
curl -LO https://dl.k8s.io/release/v1.30.0/bin/linux/amd64/kube-proxy
curl -LO https://github.com/kubernetes-sigs/cri-tools/releases/download/v1.30.0/crictl-v1.30.0-linux-amd64.tar.gz.sha512
curl -LO https://github.com/kubernetes-sigs/cri-tools/releases/download/v1.30.0/crictl-v1.30.0-linux-amd64.tar.gz
curl -LO https://github.com/opencontainers/runc/releases/download/v1.1.12/runc.amd64.asc
curl -LO https://github.com/opencontainers/runc/releases/download/v1.1.12/runc.amd64
curl -LO https://github.com/containernetworking/plugins/releases/download/v1.4.1/cni-plugins-linux-amd64-v1.4.1.tgz.sha512
curl -LO https://github.com/containernetworking/plugins/releases/download/v1.4.1/cni-plugins-linux-amd64-v1.4.1.tgz
curl -LO https://github.com/containerd/containerd/releases/download/v1.7.16/containerd-1.7.16-linux-amd64.tar.gz.sha256sum
curl -LO https://github.com/containerd/containerd/releases/download/v1.7.16/containerd-1.7.16-linux-amd64.tar.gz
curl -LO https://github.com/etcd-io/etcd/releases/download/v3.5.13/SHA256SUMS
curl -LO https://github.com/etcd-io/etcd/releases/download/v3.5.13/etcd-v3.5.13-linux-amd64.tar.gz
```
