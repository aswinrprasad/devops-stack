# DevOps Stack
A service stack for DevOps pipelines. 

## Usage
- To start the services :
    ``` 
    $ mkdir db 
    $ docker-compose up -d 
    ```

- Stop services after development
    ```
    $ docker-compose down
    ```
---
## URL's

- Jenkins : *localhost/jenkins*
- Nexus : *localhost/nexus*
- SonarQube : *localhost/sonarqube*

NB - All services are running behind apache reverse proxy

---
### Jenkins service with Docker
#### Docker in Docker - Check if it works
```
$ docker exec -it dev-jenkins bash


#Inside container shell 

jenkins@5ed8c8e06e64:/$ docker version
Client: Docker Engine - Community
 Version:           20.10.13
 API version:       1.41
 Go version:        go1.16.15
 Git commit:        a224086
 Built:             Thu Mar 10 14:08:15 2022
 OS/Arch:           linux/amd64
 Context:           default
 Experimental:      true

Server: Docker Engine - Community
 Engine:
  Version:          20.10.12
  API version:      1.41 (minimum version 1.12)
  Go version:       go1.16.12
  Git commit:       459d0df
  Built:            Mon Dec 13 11:43:56 2021
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.4.12
  GitCommit:        7b11cfaabd73bb80907dd23182b9347b4245eb5d
 runc:
  Version:          1.0.2
  GitCommit:        v1.0.2-0-g52b36a2
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```
---
### Docker Repository for Nexus 3 Service

#### Create docker repos

Follow document : https://blog.sonatype.com/using-nexus-3-as-your-repository-part-3-docker-images

NB - Use Port 8085 for the docker group repo that is created

#### Usage
- Login to nexus 3 with :
    ```
    $ docker login localhost/nexus
    ```
- Pull images with : 
    ```
    $ docker pull localhost/<image:tag>
    ```
- The pulled image will be present in the docker group repository

---
<p align="center"> Made with ❤️ </p>   
