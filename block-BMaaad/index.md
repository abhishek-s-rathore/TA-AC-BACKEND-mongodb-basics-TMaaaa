writeCode

Write command to:-

- List collections from a database.

  > show dbs

- Create a new collection in your country database which you created recently.
  > show dbs
  > use countries
  > show collections
  > db.createCollection('states')
  > show collections

Write code to:-

- crate a database named `weather`
  > show dbs
  > use weather
- create a capped collection named `temperature` with maximum of 3 documents and try inserting more than 3 to see the result.

  > db.createCollection("temprature", {capped:true,size:1000, max:3})
  > db.temprature.isCapped()
  > db.temperature.insert({tempA: 30})
  > db.temperature.insert({tempB: 40})
  > db.temperature.insert({tempC: 50})
  > db.temperature.insert({tempD: 60})

- create a simple collection named `humidity`
  > db.createCollection("humidity")
- check whether `temperature` collection is capped or not ?
  > db.temprature.isCapped()
- Delete `humidity` collection and then the entire database(weather).
  > db.humidity.drop()
