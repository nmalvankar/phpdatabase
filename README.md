# phpdatabase example

### Deploy MySQL 8
```sh
oc new-app mysql:8.0 MYSQL_USER=user MYSQL_PASSWORD=pass MYSQL_DATABASE=testdb -l db=mysql
```

### Deploy php application with environment variables for MySQL
```
oc new-app https://github.com/nmalvankar/phpdatabase MYSQL_SERVICE_HOST=mysql MYSQL_USER=user MYSQL_PASSWORD=pass MYSQL_DATABASE=testdb
```

### Expose php application
```
oc expose svc phpdatabase
```
