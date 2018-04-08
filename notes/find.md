## Fetching documents from collection: 
```db.COLLECTION.find();``` -> prints all 
```db.COLLECTION.find({KEY : VALUE});``` -> prints matching documents 

Given the entries above, we could do the following: 
```db.people.find();``-> prints all of the entries 
```db.people.find({drink : "tea"});``-> prints entries for Grandma and Guro
```db.people.find({drink : "tea", name : "Guro"});```-> prints entry for Guro 