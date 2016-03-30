---
title: Running Codeship Locally for Development
date: 2015-05-25 00:00:00 Z
categories:
- docker
tags:
- docker
- jet
- introduction
- installation
- running locally
layout: page
weight: 75
---

<div class="info-block">


These installation instructions are applicable if you want to run the Codeship local development CLI, `jet` binary, locally. If you only want to run your builds via the hosted Codeship environment, you can skip these steps.
</div>

* include a table of contents
{:toc}

## Prerequisites

In order to run the _Jet_ binary on your computer, you need to have Docker installed and configured. We recommend you follow the guides regarding [Docker Toolbox](https://www.docker.com/toolbox) to get both Docker Engine and Docker Machine installed, as well as a Docker host configured.

## Jet

Please follow the steps below for the operating system you are using. See the [Jet Release Notes]({{ site.baseurl }}{% post_url docker/jet/2015-07-16-release-notes %}) for the ChangeLog.

### Mac OS X

```bash
curl -SLo "jet-{{ site.data.jet.version }}.tar.gz" "{{ site.data.jet.base_url }}/{{ site.data.jet.version }}/jet-darwin_amd64_{{ site.data.jet.version }}.tar.gz"
tar -xC /usr/local/bin/ -f jet-{{ site.data.jet.version }}.tar.gz
chmod u+x /usr/local/bin/jet
```

### Linux

```bash
curl -SLo "jet-{{ site.data.jet.version }}.tar.gz" "{{ site.data.jet.base_url }}/{{ site.data.jet.version }}/jet-linux_amd64_{{ site.data.jet.version }}.tar.gz"
sudo tar -xaC /usr/local/bin -f jet-{{ site.data.jet.version }}.tar.gz
sudo chmod +x /usr/local/bin/jet
```

### Windows

Please download the version (`{{ site.data.jet.version }}`) from [our download site]({{ site.data.jet.base_url }}/{{ site.data.jet.version }}/jet-windows_amd64_{{ site.data.jet.version }}.tar.gz). Once you have done this, you need to extract the archive and copy the binary to your path.

### Dynamically linked version

The above version is statically linked and will work the same way on all platforms. But it doesn't support certain features, e.g. resolving `.local` DNS names. If your builds require this, please use the dynamically linked version instead.

* [Mac OS X]({{ site.data.jet.base_url }}/{{ site.data.jet.version }}/jet-darwin_amd64_{{ site.data.jet.version }}-dynamic.tar.gz)
* [Linux]({{ site.data.jet.base_url }}/{{ site.data.jet.version }}/jet-linux_amd64_{{ site.data.jet.version }}-dynamic.tar.gz)
* [Windows]({{ site.data.jet.base_url }}/{{ site.data.jet.version }}/jet-windows_amd64_{{ site.data.jet.version }}-dynamic.tar.gz)

## Validating Installation

Once this is done you can check that _Jet_ is working by running `jet help`. This will print output similar to the following.

```bash
$ jet version
{{ site.data.jet.version }}
$ jet help
Usage:
  jet [command]
...
```

## Docker Configuration

`DOCKER_HOST` must be set. `DOCKER_TLS_VERIFY` and `DOCKER_CERT_PATH` are respected in the same way as with the official Docker client.

If you installed and configured your Docker environment via [Docker Machine](https://docs.docker.com/machine/) (and you are on OS X or Linux) and named the environment _dev_, running the following command will set those variables.

```bash
eval $(docker-machine env dev)
```
