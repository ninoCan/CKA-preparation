# Playground cluster

A local cluster to experiment and train with K8s can be set using `kind`

## Installation

On MacOS, `kind` can be installed 

```
    $ brew install kind
```

<details>
<p>
On Archlinux, it might be necessary to activate a couple of kernel modules to get `kind` to work properly.
Namely, edit the `/etc/modules-load.d/k8s.conf` file and add:

```
   overlay
   br_netfilter
```

Also, make sure to activate the necessary kernel parameters by editing `/etc/sysctl.d/k8s.conf`

```
net.bridge.bridge-nf-call-iptables  = 1
net.bridge.bridge-nf-call-ip6tables = 1
net.ipv4.ip_forward                 = 1
```

Then the `kind` package can be found on the AUR.
</p>
</details>
