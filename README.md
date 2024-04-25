# kuberneetzzzz

## rhel8 install

``` bash
sestatus
sudo sed -i 's/^SELINUX=enforcing$/SELINUX=permissive/' /etc/selinux/config
reboot
sestatus # should be permissive now
sudo dnf install -y iproute-tc
```
