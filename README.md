# Home Server services

This repositoty houses a collection of services I run for my personal needs on my home server.

The services are defined according to the [Compose specification](https://compose-spec.io/) and run on [Fedora CoreOS](https://getfedora.org/coreos) using rootless [Podman](https://podman.io/).


#### 1. Create Podman container:
```
cd $SERVICE_DIRECTORY
podman-compose up
```

#### 2. Create systemd service:
```
cd ~/.config/systemd/user/
podman generate systemd  --name  --new  --files $PODMAN_CONTAINER
```
