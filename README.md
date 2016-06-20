# Jboss BRMS docker
Build a Jboss BRMS docker image on Alpine Linux distro.

## Version
- EAP: 6.4.5
- BRMS: 6.1.5

>Dockerhub: https://hub.docker.com/r/anoopnair/jboss-brms/

## Build docker image
- Download _jboss-eap-6.4.5-brms-6.1.5.tar.gz_ or the latest one from JBOSS site
- Put it in this folder
- Update Docker file with EAP and brms version
- Build the docker image using ``docker build`` command


## Start standalone BRMS container
- ``docker run --name brms -it -p 38080:8080 -p 9990:9990 anoopnair/jboss-brms:6.1.5``
- Hit 'http://localhost:38080/business-central' url
- Login using brmsadmin/Redh@t11
- Create repositories and rules
- Stop container using ``docker stop brms``
- Start back same container using ``docker start brms``