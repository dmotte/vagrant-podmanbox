# vagrant-podmanbox

![icon](icon-128.png)

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/dmotte/vagrant-podmanbox/release?logo=github&style=flat-square)](https://github.com/dmotte/vagrant-podmanbox/actions)
[![Vagrant Cloud](https://img.shields.io/badge/vagrant-dmotte/podmanbox-blue?logo=vagrant&style=flat-square)](https://app.vagrantup.com/dmotte/boxes/podmanbox)

:package: **Debian Vagrant box** with **Podman** (and **podman-compose**).

This project uses [alvistack/ansible-role-podman](https://github.com/alvistack/ansible-role-podman) to install the latest versions of _Podman_ and _podman-compose_ inside the VM.

> :package: This box is also on **Vagrant Cloud** as [`dmotte/podmanbox`](https://app.vagrantup.com/dmotte/boxes/podmanbox).

## Usage

See [the `test` folder of dmotte/vagrant-dockerbox](https://github.com/dmotte/vagrant-dockerbox/tree/main/test) for an usage example of another Vagrant box which is very similar to this one.

## Troubleshooting

If you run into problems pulling images:

```
vagrant@podmanbox01:~$ podman pull docker.io/nginx
Trying to pull docker.io/library/nginx:latest...
Error: initializing source docker://nginx:latest: reading manifest latest in quay.io/libpod/nginx: unauthorized: access to the requested resource is not authorized
```

you may want to edit the `/etc/containers/registries.conf` file to use another mirror.
