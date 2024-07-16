# Loan Originating Service (LOS) Deploy : 

Configure ```application.properties``` to connect backend with MySQL DB.
```
spring.datasource.url= jdbc:mysql://${MYSQL_HOST}:${MYSQL_PORT}/${DB_NAME}?useUnicode=yes&characterEncoding=UTF-8&characterSetResults=UTF-8
spring.datasource.username= ${MYSQL_USER}
spring.datasource.password= ${MYSQL_PASSWORD}
```
To fetch data from the backend, mention only the upstream module for backend from ```default.conf```.

```
'/api'
```

## Docker 

Up the docker-compose file.  
```
docker compose up
```

## Kubernetes

Change the directory to k8.
```
cd k8 
```
Apply all the menifest files in ```k8``` folder.
```
kubectl apply -f .
```

**Note**
- Port mapping has to be done perfectly. Double check whether the mapped port is matching with the container port or not.
- Environment variables have to be mentioned in the docker-compose and k8 menifest files. 
