# Collections 

MongoDB stores BSON-documents (data records). These BSON-documents are placed in _Collections_. Several documents can share a collection. 

__Collection "people"__: 
```json
    {name: "Guro", drink: "tea"}
    {name: "Elon", drink: "coffee"}
    {name: "Johanne", drink: "hot chocolate"}
```

Collections are accessed with db.COLLECTION_NAME, i.e. db.people 


## Creating collections 

As with databases, MongoDB creates one if it does not exist, if it is refrenced. 
Collections can also be made using ```db.createCollection(name, {OPTIONS});```

## Inserting into collections 

Inserting documents into collections can be done using: ```db.COLLECTION.insertOne(DOCUMENT);```  
Inserting several documents into collection:  ```db.COLLECTION.insert([DOCUMENT1, DOCUMENT2]);```  


For example: 
```json
    db.people.insertOne({name : "Grandma", drink: "tea"});
    db.peope.insert([
        {name: "Guro", drink: "tea"}, 
        {name: "Elon", drink: "coffee", note: "!>1cup"},
        {name: "Johanne", drink: "hot chocolate"}
    ]); 
```

## Dropping a collection 

A collection is removed with the .drop()-method. It returnst true if dropped, false if not 
```db.COLLECTION.drop();``` 

## Fetching documents from collection: 
```db.COLLECTION.find();``` -> prints all 
```db.COLLECTION.find({KEY : VALUE});``` -> prints matching documents 

Given the entries above, we could do the following: 
```db.people.find();``-> prints all of the entries 
```db.people.find({drink : "tea"});``-> prints entries for Grandma and Guro
```db.people.find({drink : "tea", name : "Guro"});```-> prints entry for Guro 