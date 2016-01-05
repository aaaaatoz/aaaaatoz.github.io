# Docker study notes - 1 Overview
## Three essential concepts about docker

	*	Image:
	*	Container:
	*	Repository:

Image is the readonly model for docker container.
It can be an OS or OS with applications. Image is the base of the docker.

Coantiner is the lightweight sandbox. It can run applications in an isolated environment.

Repository is the place to register and hold the images. It can be either public or private.

## Docker Installation
Here are the steps I installed docker on an virtual box - ubuntu 14.04
[Installation Link](https://docs.docker.com/engine/installation/ubuntulinux/)

1. Update apt sources

`$ sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D`

in /etc/apt/sources.list.d/docker.list, put line

`deb https://apt.dockerproject.org/repo ubuntu-trusty main`

update the repo

`apt-get update`

2. For Ubuntu Trusty, Vivid, and Wily, it’s recommended to install the linux-image-extra kernel package. 

`apt-get install linux-image-extra-$(uname -r)

3. Install the Docker service

`apt-get install docker-engine`
check the service is running

`service docker status`

4. run a test docker container

`docker run hello-world`


