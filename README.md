# Implementing MongoDB Replication Set With AuthKey

This repository contains docker-compose and bash script files to implement mongodb replica-set by using docker compose



- Bash into one container: **docker exec -it mongo1 bash**
- Run **mongosh -u root -p example**
- Initiate the replica set using:
```js
 rs.initiate(
  {
    _id: "rs0",
    version: 1,
    members: [
      { _id: 0, host: "mongo1:27017" },
      { _id: 1, host: "mongo2:27018" },
      { _id: 2, host: "mongo3:27019" }
    ]
  }
)
```

[ref](https://medium.com/@JosephOjo/mongodb-replica-set-with-docker-compose-5ab95c02af0d)
