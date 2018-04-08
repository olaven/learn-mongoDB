# Updating documents in a collection 

To update one or more documents, one specifies a filter (which documents in collection should be updated?), the update itself and options. 

## Updating 
_.updateOne_: updates first occurence of filter = true 
_.updateMany_: updates all occurences 

```db.COLLECTION_NAME.updateOne(FILTER, UPDATE, OPTIONS);```
```db.COLLECTION_NAME.updateMany(FILTER, UPDATE, OPTIONS);```

__Example:__
```javascript 
    db.people.updateMany(
        {drink : "coffee"}, 
        {
            $set : {assumption : "likes to drink coffee"}
        }
    ); 
```


## Replacing 
_.updateOne_: replaces first occurence 
```db.COLLECTION_NAME.replaceOne(FILTER, REPLACEMENT, OPTIONS);```