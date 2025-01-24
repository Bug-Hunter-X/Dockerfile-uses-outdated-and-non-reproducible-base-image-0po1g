# Dockerfile Best Practices

This repository demonstrates a common issue found in Dockerfiles: using an unspecified base image and non-optimized package management commands.  Using `ubuntu:latest` is discouraged because it lacks versioning, potentially causing unexpected behavior in different builds.

The `Dockerfile_fixed` example demonstrates the improvements:
* Uses a specific version of Ubuntu, which ensures consistent behavior and reproducibility.
* Uses `--no-install-recommends` with `apt-get` to install only necessary packages, reducing the image size and improving security.

This is a critical aspect of Docker best practices for building reliable and predictable container images.