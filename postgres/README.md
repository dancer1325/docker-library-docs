<!--

********************************************************************************

WARNING:

    DO NOT EDIT "postgres/README.md"

    IT IS AUTO-GENERATED

    (from the other files in "postgres/" combined with a set of templates)

********************************************************************************

-->

# Quick reference

-	**Maintained by**:  
	[the PostgreSQL Docker Community](https://github.com/docker-library/postgres)

-	**Where to get help**:  
	[the Docker Community Slack](https://dockr.ly/comm-slack), [Server Fault](https://serverfault.com/help/on-topic), [Unix & Linux](https://unix.stackexchange.com/help/on-topic), or [Stack Overflow](https://stackoverflow.com/help/on-topic)

# Supported tags and respective `Dockerfile` links

-	[`17.2`, `17`, `latest`, `17.2-bookworm`, `17-bookworm`, `bookworm`](https://github.com/docker-library/postgres/blob/0b87a9bbd23f56b1e9e863ecda5cc9e66416c4e0/17/bookworm/Dockerfile)

-	[`17.2-bullseye`, `17-bullseye`, `bullseye`](https://github.com/docker-library/postgres/blob/0b87a9bbd23f56b1e9e863ecda5cc9e66416c4e0/17/bullseye/Dockerfile)

-	[`17.2-alpine3.21`, `17-alpine3.21`, `alpine3.21`, `17.2-alpine`, `17-alpine`, `alpine`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/17/alpine3.21/Dockerfile)

-	[`17.2-alpine3.20`, `17-alpine3.20`, `alpine3.20`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/17/alpine3.20/Dockerfile)

-	[`16.6`, `16`, `16.6-bookworm`, `16-bookworm`](https://github.com/docker-library/postgres/blob/960ebdf14ef92d328588e77af2a879c63e577e96/16/bookworm/Dockerfile)

-	[`16.6-bullseye`, `16-bullseye`](https://github.com/docker-library/postgres/blob/960ebdf14ef92d328588e77af2a879c63e577e96/16/bullseye/Dockerfile)

-	[`16.6-alpine3.21`, `16-alpine3.21`, `16.6-alpine`, `16-alpine`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/16/alpine3.21/Dockerfile)

-	[`16.6-alpine3.20`, `16-alpine3.20`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/16/alpine3.20/Dockerfile)

-	[`15.10`, `15`, `15.10-bookworm`, `15-bookworm`](https://github.com/docker-library/postgres/blob/50b4cdb50e3599013f2fce9cd8860600f53c696c/15/bookworm/Dockerfile)

-	[`15.10-bullseye`, `15-bullseye`](https://github.com/docker-library/postgres/blob/50b4cdb50e3599013f2fce9cd8860600f53c696c/15/bullseye/Dockerfile)

-	[`15.10-alpine3.21`, `15-alpine3.21`, `15.10-alpine`, `15-alpine`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/15/alpine3.21/Dockerfile)

-	[`15.10-alpine3.20`, `15-alpine3.20`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/15/alpine3.20/Dockerfile)

-	[`14.15`, `14`, `14.15-bookworm`, `14-bookworm`](https://github.com/docker-library/postgres/blob/c44484583320c81b35824ec0ce16864690d68bc3/14/bookworm/Dockerfile)

-	[`14.15-bullseye`, `14-bullseye`](https://github.com/docker-library/postgres/blob/c44484583320c81b35824ec0ce16864690d68bc3/14/bullseye/Dockerfile)

-	[`14.15-alpine3.21`, `14-alpine3.21`, `14.15-alpine`, `14-alpine`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/14/alpine3.21/Dockerfile)

-	[`14.15-alpine3.20`, `14-alpine3.20`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/14/alpine3.20/Dockerfile)

-	[`13.18`, `13`, `13.18-bookworm`, `13-bookworm`](https://github.com/docker-library/postgres/blob/9fadd0e250ba0c150dafec9e3c8728de3c8e318f/13/bookworm/Dockerfile)

-	[`13.18-bullseye`, `13-bullseye`](https://github.com/docker-library/postgres/blob/9fadd0e250ba0c150dafec9e3c8728de3c8e318f/13/bullseye/Dockerfile)

-	[`13.18-alpine3.21`, `13-alpine3.21`, `13.18-alpine`, `13-alpine`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/13/alpine3.21/Dockerfile)

-	[`13.18-alpine3.20`, `13-alpine3.20`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/13/alpine3.20/Dockerfile)

-	[`12.22`, `12`, `12.22-bookworm`, `12-bookworm`](https://github.com/docker-library/postgres/blob/5f590b8df7f12270d1d5227758744ca3b0bdef74/12/bookworm/Dockerfile)

-	[`12.22-bullseye`, `12-bullseye`](https://github.com/docker-library/postgres/blob/5f590b8df7f12270d1d5227758744ca3b0bdef74/12/bullseye/Dockerfile)

-	[`12.22-alpine3.21`, `12-alpine3.21`, `12.22-alpine`, `12-alpine`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/12/alpine3.21/Dockerfile)

-	[`12.22-alpine3.20`, `12-alpine3.20`](https://github.com/docker-library/postgres/blob/17818f21dca10ccf02711476e138c219bd31b456/12/alpine3.20/Dockerfile)

# Quick reference (cont.)

-	**Where to file issues**:  
	[https://github.com/docker-library/postgres/issues](https://github.com/docker-library/postgres/issues?q=)

-	**Supported architectures**: ([more info](https://github.com/docker-library/official-images#architectures-other-than-amd64))  
	[`amd64`](https://hub.docker.com/r/amd64/postgres/), [`arm32v5`](https://hub.docker.com/r/arm32v5/postgres/), [`arm32v6`](https://hub.docker.com/r/arm32v6/postgres/), [`arm32v7`](https://hub.docker.com/r/arm32v7/postgres/), [`arm64v8`](https://hub.docker.com/r/arm64v8/postgres/), [`i386`](https://hub.docker.com/r/i386/postgres/), [`mips64le`](https://hub.docker.com/r/mips64le/postgres/), [`ppc64le`](https://hub.docker.com/r/ppc64le/postgres/), [`riscv64`](https://hub.docker.com/r/riscv64/postgres/), [`s390x`](https://hub.docker.com/r/s390x/postgres/)

-	**Published image artifact details**:  
	[repo-info repo's `repos/postgres/` directory](https://github.com/docker-library/repo-info/blob/master/repos/postgres) ([history](https://github.com/docker-library/repo-info/commits/master/repos/postgres))  
	(image metadata, transfer size, etc)

-	**Image updates**:  
	[official-images repo's `library/postgres` label](https://github.com/docker-library/official-images/issues?q=label%3Alibrary%2Fpostgres)  
	[official-images repo's `library/postgres` file](https://github.com/docker-library/official-images/blob/master/library/postgres) ([history](https://github.com/docker-library/official-images/commits/master/library/postgres))

-	**Source of this description**:  
	[docs repo's `postgres/` directory](https://github.com/docker-library/docs/tree/master/postgres) ([history](https://github.com/docker-library/docs/commits/master/postgres))

# Image Variants == flavors

## `postgres:<version>`

* TODO:This is the defacto image. If you are unsure about what your needs are, you probably want to use this one. It is designed to be used both as a throw away container (mount your source code and start the container to start your app), as well as the base to build other images off of.

Some of these tags may have names like bookworm or bullseye in them. These are the suite code names for releases of [Debian](https://wiki.debian.org/DebianReleases) and indicate which release the image is based on. If your image needs to install any additional packages beyond what comes with the image, you'll likely want to specify one of these explicitly to minimize breakage when there are new releases of Debian.

## `postgres:<version>-alpine`

This image is based on the popular [Alpine Linux project](https://alpinelinux.org), available in [the `alpine` official image](https://hub.docker.com/_/alpine). Alpine Linux is much smaller than most distribution base images (~5MB), and thus leads to much slimmer images in general.

This variant is useful when final image size being as small as possible is your primary concern. The main caveat to note is that it does use [musl libc](https://musl.libc.org) instead of [glibc and friends](https://www.etalabs.net/compare_libcs.html), so software will often run into issues depending on the depth of their libc requirements/assumptions. See [this Hacker News comment thread](https://news.ycombinator.com/item?id=10782897) for more discussion of the issues that might arise and some pro/con comparisons of using Alpine-based images.

To minimize image size, it's uncommon for additional related tools (such as `git` or `bash`) to be included in Alpine-based images. Using this image as a base, add the things you need in your own Dockerfile (see the [`alpine` image description](https://hub.docker.com/_/alpine/) for examples of how to install packages if you are unfamiliar).
