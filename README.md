# ConfigServer
Spring cloud config server

## Overview

![Overview](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/aau-claaudia/ConfigServer/main/overview.iuml)

### How to generate new ssh key for github

Run the following command
```
ssh-keygen -m PEM -t rsa -b 4096 -C "config@claaudia.aau.dk"
```


### Deployment

There is no pipeline so the following command is used on the servers to update the container image:

```
sudo docker service update --image ghcr.io/aau-claaudia/configserver:662158 osg_configserver
```

The image tag can be seen on the packages page here: https://github.com/aau-claaudia/ConfigServer/pkgs/container/configserver
