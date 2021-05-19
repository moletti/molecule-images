# Debian images
Pre built images for testing with molecule framework.
All images include:
- systemd
- dbus
- python/python3
- sudo

## Supported tags
- `jessie`, `8`
- `stretch`, `9`
- `buster`, `10`, `latest`

## Usage
### Molecule:
```
platforms:
  - name: debian
    image: moletti/molecule-debian:10
    pre_build_image: true
    privileged: true
    volumes:
      - /sys/fs/cgroup:/sys/fs/cgroup:ro
```

### Locally:
```
docker run -d --privileged --name debian -v /sys/fs/cgroup:/sys/fs/cgroup:ro moletti/molecule-debian:10 
```

**SEE ALSO**:
- molecule-ubuntu ( [source](https://github.com/moletti/molecule-images/tree/master/ubuntu), [docker hub](https://hub.docker.com/r/moletti/molecule-ubuntu) )
