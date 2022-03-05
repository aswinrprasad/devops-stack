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

## URL's

- Jenkins : *localhost/jenkins*
- Nexus : *localhost/nexus*
- SonarQube : *localhost/sonarqube*

NB - All services are running behind apache reverse proxy

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

