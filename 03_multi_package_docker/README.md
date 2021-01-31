# Multi Package Docker Image
Demonstrates how to build a multi package docker image in Nix

The pkg for pkg.dockerTools.

NOTE: 
* curl does not work because of the bundle.crt
* locate bundle.crt


## Examples of how to build Docker images
[Examples](https://github.com/NixOS/nixpkgs/blob/master/pkgs/build-support/docker/examples.nix)  

[Interface](https://github.com/NixOS/nixpkgs/blob/master/pkgs/build-support/docker/default.nix)

```sh
nix-build
docker load < result
docker images
docker run -t kuttl:bh3mi99nk7f1vfisv9200c0b2dwbdblx
docker run -it --entrypoint /bin/bash kuttl:bh3mi99nk7f1vfisv9200c0b2dwbdblx

# there is no ls cmd so we use echo.
echo *
echo /bin/*
echo $PATH
```