# BIG DATA - MongoDB Tutorials
Basic MongoDB functions and tutorials on terminal. Please install mongoDB on your server. And then,

## Start to terminal (CMD)
```
C:\Users\Your Name>mongo
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

### Create a collection(Table)
> MongoDB creates collection automatically, when you insert some document. Also you can create before.
```
use latestdb
switched to db latestdb
db.createCollection("mycollection")
{ "ok" : 1 }
```

### Show Collections(tables)
```
>show collections
mycollection
```

### Delete/Drop Database
> If you have not selected any database, then it will delete default 'test' database.
```
db.dropDatabase()
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
* [MongoDB - TutorialsPoint Overview](https://www.tutorialspoint.com/mongodb/index.htm)
