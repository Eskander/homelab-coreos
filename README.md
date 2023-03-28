# Homeserver Services

_A collection of services I run on a bare metal single node home server._

The services run in containers on a [Fedora CoreOS](https://getfedora.org/coreos) host using rootless [Podman](https://podman.io/). The containers are defined in [Podman Quadlet](https://docs.podman.io/en/latest/markdown/podman-systemd.unit.5.html) format and are managed as [Systemd](https://systemd.io/) services.

### FAQ

#### How to replicate this setup?
```
git clone https://github.com/Eskander/homeserver-coreos ~/.config/containers/systemd/
systemctl reboot
```

#### Protip: Use [Firewalld](https://firewalld.org/) to forward a privileged port to a rootless container:
```
sudo firewall-cmd --add-forward-port=port=80:proto=tcp:toport=8080
```
