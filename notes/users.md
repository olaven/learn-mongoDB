# Users 

Users have different permissions. Not everyone should be able to do everything. 
A user can be created in the shell like this: 
```json
    db.createUser({
        user : "testuser", 
        pwd  : "test", 
        roles: ["dbAdmin", "readWrite"] 
    }); 
```