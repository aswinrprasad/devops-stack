# DevOps Stack
A service stack for DevOps pipelines. 

### Usage
- To start the services :
    ``` 
    $ mkdir db 
    $ docker-compose up -d 
    ```

- Stop services after development
    ```
    $ docker-compose down
    ```

### URL's

- Jenkins : *localhost/jenkins*
- Nexus : *localhost/nexus*
- SonarQube : *localhost/sonarqube*

NB - All services are running behind apache reverse proxy