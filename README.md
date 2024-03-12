# neo4j-docker-backup-restore



Afterward, we access the MongoDB container.
``` 
$ docker exec -ti <neo4j's container name> sh
$ cd backup
```


### This command is used to backup data from a MongoDB database.
```
$ mongodump --username admin_user --password admin_pass --out=/backup/
```


### restore the database
```
$ mongorestore --username admin_user --password admin_pass --authenticationDatabase admin --db my_database  /backup/dms-database/
```

