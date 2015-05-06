# docker-jenkins
Docker Image of Jenkins

## This Docker image contain:

1. Java and maven to build your java projects
1. Default configuration to Active Directory authentication
1. Default configuration to use private ssh key
1. Access to git servers

## How to

### Configure Active Directory authentication

Open config.xml and change the values of "<securityRealm" section

### Configure private ssh key to access private git 

1. Generate your private key and put "id_rsa" and "id_rsa.pub" files inside the same folder that Dockerfile
1. Put the content of "id_rsa" on "<privateKey>" section of credentials.xml file
1. Put the content of "id_rsa.pub" in your git server to access the chosen repositories

## Build your docker image

```
docker build -t=yournick/jenkins .
```
