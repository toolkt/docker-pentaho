# docker-pentaho
Docker Pentaho for OpenERP Tomcat Server

Build the image
```sh
docker build -t toolkt/pentaho:10.0 .
```

Run the container as a Daemon (-d)
```sh
docker run -d -p 8080:8080 --name pentaho10 -d toolkt/pentaho:10.0
```

Start & stop the service
```sh
docker stop pentaho10
```

Enter the terminal of the container
```sh
docker exec -it pentaho10 bash
```


Commit the running container to the image and then to Docker
```sh
docker login
#Enter Username and Password
docker commit pentaho10 toolkt/pentaho:10.0
docker push toolkt/pentaho:10.0
```