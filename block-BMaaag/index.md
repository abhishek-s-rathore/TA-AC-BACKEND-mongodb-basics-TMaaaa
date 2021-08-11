Write code to:-

- create a database named `mountains`

  > show dbs
  > use mountains
  > db

- a collection inside that database named `himalayas`

  > db.createCollections('himalayas')
  > show collections

- insert 1 document into that collection `{name: 'Dhauldhar range', height: '4000 mtrs'}`

  > db.himalayas.insert({name: 'Dhauldhar range', height: '4000 mtrs'})

- insert multiple document using insertMany command

  > db.himalayas.insertMany([{name: 'Everest range', height: '8856 mtrs'}, {name: 'K2 range', height: '5670 mtrs'}])

- find all documents from mountains

  > db.himalayas.find()
  > OR
  > db.himalayas.find({})

- find a single document using name
  > db.himalayas.find({name:"Dhauldhar range"})
  > OR
  > db.himalayas.findOne({name:"Dhauldhar range"})
