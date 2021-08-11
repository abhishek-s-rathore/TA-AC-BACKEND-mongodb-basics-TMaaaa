Write code to:-

- create a database named `sports`.sports

  > use sports

- list all databases present in local mongod server.

  > show dbs

- create 3 collections named `cricket`, `football`, `TT` in sports databse.

  > db.createCollection('Cricket')
  > db.createCollection('Football')
  > db.createCollection('Table Tennis')

- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.
  > db.Cricket.insertMany([{name:"Aa",email: "aa@gmail.com", age:21, bid_price: 1000},{name:"Bb",email: "bb@gmail.com", age:22, bid_price: 2000},{name:"Cc",email: "cc@gmail.com", age:23, bid_price: 3000}])
- list all collections in sports database.

- rename `Cricket` collection to `Tennis`.

  > db.Cricket.renameCollection("Tennis")

- create a capped collection called `khokho` which should have max 3 documents.
  Try inserting more than 3 and see what happens?

  > db.createCollection('Khokho', {capped: true, size: 1024, max:3})
  > db.Khokho.insertMany([{name:"Aa",email: "aa@gmail.com", age:21, bid_price: 1000},{name:"Bb",email: "bb@gmail.com", age:22, bid_price: 2000},{name:"Cc",email: "cc@gmail.com", age:23, bid_price: 3000}])
  > db.Khokho.insert({name:"Dd",email: "dd@gmail.com", age:24, bid_price: 4000})

- list all collections in sports database.

  > db.Khokho.find() --> Gives latest 3 documents

- check whether a collection is capped or not?

  > db.Khokho.isCapped() --> false

- drop all documents from `football` collection.

  > db.Football.drop()

- delete `Khokho` collection completely.

  > db.Khokho.drop()

- delete sports database.

  > db.dropDatabase()

- check which database you are connected to ?
  > db --> test
- connect to test database
  > use test
