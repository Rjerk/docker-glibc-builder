# docker-glibc-builder

A glibc binary package builder in Docker. Produces a glibc binary package that can be imported into a rootfs to run applications dynamically linked against glibc.

## Usage

Build images:

    docker build -t sgerrand/glibc-builder:2.30 .

Build a glibc package based on version 2.30 with a prefix of `/usr/glibc-compat`:

    docker run --rm --env STDOUT=1 sgerrand/glibc-builder:2.30 2.30 /usr/glibc-compat > glibc-bin-2.30-0-aarch64.tar.gz
