# BIG DATA - MongoDB Tutorials
Basic MongoDB functions and tutorials on terminal. Please install mongoDB on your server. And then,

## Start to terminal (CMD)
```
D:\set up\mongodb\bin>mongo.exe
```

### Create database or use existing database.
```
>use mytestdb
switched to db mytestdb
```

### To check your currently selected database, use the command db
```
>db
mytestdb
```

### If you want to check your databases list, use the command show dbs.
> Your created database (mytestdb) is not present in list. 
```
>show dbs
local     0.78125GB
config    0.23012GB
```

### I added to users collection(table).
```
>db.users.insert({"name":"UGUR COBAN"})
>show dbs
local      0.78125GB
mytestdb   0.23012GB
```

### Change to collection(table). And Save record. And find last one.
```
>db.newdb.save( { a: 1 } )
>db.newdb.find()
{ "_id" : ObjectId(5879b0f65a56a454), "a" : 1 }
```

### Show Collections(tables)
```
>show collections
users
newdb
```

### Help & Stats & Version
```
>db.help()
>db.stats();
>db.version();
```

### To check counters of database operations
```
D:\set up\mongodb\bin>mongostat
```

### Tracks and reports activity
```
D:\set up\mongodb\bin>mongotop
```

## Documentation

* [MongoDB - Download](https://www.mongodb.com/download-center/community)
* [Nodejs - TutorialsPoint MongoDB](https://www.tutorialspoint.com/mongodb/index.htm)
