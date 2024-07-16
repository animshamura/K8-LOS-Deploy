# Loan Originating Service (LOS) Deploy : 

The backend application has to be built without testing using below command.

```
mvn clean package -DskipTests
```
So do for the frontend application too.

```
npm run build-only
```

DB connection for the backend would be like this.
```
jdbc:mysql://${MYSQL_HOST}:${MYSQL_PORT}/${DB_NAME}?useUnicode=yes&characterEncoding=UTF-8&characterSetResults=UTF-8
```
For backend URL to fetch data, mention only the upstream in 'default.conf'.
```
'/api'
```
