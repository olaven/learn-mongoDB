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

## Dropping a collection 

A collection is removed with the .drop()-method. It returns true true if dropped, false if not 
```db.COLLECTION.drop();``` 
