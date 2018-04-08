# Inserting into collections 

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