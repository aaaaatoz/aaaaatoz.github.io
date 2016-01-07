# Docker image operations

### Get docker image

* docker image can be get via the following command:
` docker pull [image]:[version]`
when you download, you can see the file layers added to the images

### review the docker image
* docker image can listed by the following command:
` docker images [image]`

* docker image can be checked by
` docker image inspect [image id]`

### search the docker images
* docker image can be search by name as
`docker search [name]`

### delete the docker images
* docker image can be deleted by
`docker rmi [image-name]`
note: when there is any container related with docker image, you may need to delete the container before the images
`docker rm [container]`

### save the docker image locally
* docker image can be saved as a local file
`docker save -o [localfile] [image]`

### load local file to a docker image
* docker file can be loaded as a image
`docker load < [image file]`


