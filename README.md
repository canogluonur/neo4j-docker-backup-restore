# neo4j-docker-backup-restore

first we bind our dump file to the docker-compose volume

and then in the command section we type this command:
``` 
$ command: neo4j-admin database load --from-path=/var/lib/neo4j/import neo4j --overwrite-destination=true --verbose
$ docker compose up -d 
```

then we go inside the container and check the logs
```
$ docker logs  <neo4j's container name> 
```

When you see that you are successfull. again we change the command in the docker compose file
```
$ command: neo4j
$ docker compose up -d 
```

