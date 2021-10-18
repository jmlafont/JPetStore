# JPETSTORE
This repo is a fork from [https://github.com/IBM-Cloud/jpetstore-kubernetes](https://github.com/IBM-Cloud/jpetstore-kubernetes)

---
It has been adapted to be able to:

- pull & push images from/to quay.io (see [Link](./makefile) , [Link](./jpetstore/Dockerfile) and [Link](./jpetstore/db/Dockerfile)
- deploy with various tools: see YAML,TEKTON,ANSIBLE,MCM folders

---
## Usage:
### pre-req:
- install git
- clone current repository
- install java
- install docker

### build a new war file:
```
cd jpetstore/jpetstore ; ./build.sh all
```
### build and publish new images:
```
cd jpetstore ; make build-petstore
```
