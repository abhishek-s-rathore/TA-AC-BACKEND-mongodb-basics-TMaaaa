writeCode

Run these shell commands in mongo shell:

- db.version()
  3.6.8

- db.stats()
  {
  "db" : "test",
  "collections" : 0,
  "views" : 0,
  "objects" : 0,
  "avgObjSize" : 0,
  "dataSize" : 0,
  "storageSize" : 0,
  "numExtents" : 0,
  "indexes" : 0,
  "indexSize" : 0,
  "fileSize" : 0,
  "fsUsedSize" : 0,
  "fsTotalSize" : 0,
  "ok" : 1
  }
- db.help()
  Gives list of different options

Write code to:

- create a database of your country name.
- check list of databases to see newly created database.
- check which database you are currently connected to ?

//--------------------------------------------------------//

> show dbs --> It shows all the datbase list
> admin 0.000GB
> local 0.000GB

> use country --> To create database collection

> show dbs --> It shows all the datbase list
> admin 0.000GB  
>  local 0.000GB (Here country will shown only when document is added to it.)

> db.user.insert({name: "India", capital:"Delhi", flag="Tiranga"}) --> To add document in database.

OR

> db.collection.insert({name: "India", capital:"Delhi", flag="Tiranga"}) --> To add document in database.
> WriteResult({ "nInserted" : 1 }) --> It shows that 1 document is added to collection.

> show dbs
> admin 0.000GB
> country 0.000GB (Now country is visible)
> local 0.000GB

> db --> it will give current database.
