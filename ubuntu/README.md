# Ubuntu images
Pre built images for testing with molecule framework. 

## Supported tags
- `16.04`, `xenial`
- `18.04`, `bionic`
- `20.04`, `focal`, `latest`

## Usage
##### Molecule
```
platforms:
  - name: ubuntu
    image: moletti/molecule-ubuntu:20.04
    pre_build_image: true
    privileged: true
    volumes:
      - /sys/fs/cgroup:/sys/fs/cgroup:ro
```

##### Locally
```
docker run -d ubuntu --privileged -v /sys/fs/cgroup:/sys/fs/cgroup:ro moletti/molecule-ubuntu:20.04 
```
