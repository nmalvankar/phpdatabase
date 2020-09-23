# phpdatabase example

### Deploy MySQL 8
```sh
oc new-app mysql:8.0 MYSQL_USER=user MYSQL_PASSWORD=pass MYSQL_DATABASE=testdb -l db=mysql
```

### Deploy php application and link with MYSQL
```
oc new-app https://github.com/nmalvankar/phpdatabase MYSQL_SERVICE_HOST=mysql MYSQL_USER=user MYSQL_PASSWORD=pass MYSQL_DATABASE=testdb
```


### Expose php app
```
oc expose svc phpdatabase
```
