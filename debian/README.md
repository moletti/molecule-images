# Debian images
Pre built images for testing with molecule framework. 

## Supported tags
- `jessie`, `8`
- `stretch`, `9`
- `buster`, `10`, `latest`

## Usage
##### Molecule
```
platforms:
  - name: debian
    image: moletti/molecule-debian:10
    pre_build_image: true
    privileged: true
    volumes:
      - /sys/fs/cgroup:/sys/fs/cgroup:ro
```

##### Locally
```
docker run -d debian --privileged -v /sys/fs/cgroup:/sys/fs/cgroup:ro moletti/molecule-debian:10 
```
