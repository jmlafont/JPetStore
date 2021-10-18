# JPETSTORE
This repo is a fork from [https://github.com/IBM-Cloud/jpetstore-kubernetes](https://github.com/IBM-Cloud/jpetstore-kubernetes)

---
It has been adapted to be able to:

- pull & push images from/to quay.io (see [makefile](./makefile) , [jeptstore/Dockerfile](./jpetstore/Dockerfile) and [db/Dockerfile](./jpetstore/db/Dockerfile))
- deploy with various tools: see YAML,TEKTON,ANSIBLE,MCM folders

---
## Usage:
### pre-req:
- install git :
```
cd jpetstore/jpetstore ; ./build.sh all
```
- clone current repository
- install java
```
yum install java-1.8.0-openjdk
```
- set JAVA_HOME (from .bash_profile)
- install docker
```
sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
sudo yum install -y yum-utils
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
sudo yum install docker-ce docker-ce-cli containerd.io
```
### build a new war file:
```
cd jpetstore/jpetstore ; ./build.sh all
```
### build and publish new images:
```
cd jpetstore ; make build-petstore
```
