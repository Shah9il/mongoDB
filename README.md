# BIG DATA - MongoDB Tutorials
Basic MongoDB functions and tutorials on terminal. Please install mongoDB on your server. And then,

## Start to Mongo DB on terminal(CMD)
```
C:\Users\Your Name>mongo
```



## Create database or use existing database. 
```
>use mytestdb
switched to db mytestdb
```

> Check your db. Your created database (mytestdb), But it is not present in list. (Because no data yet)
```
>db
mytestdb
>show dbs
local     0.78125GB
config    0.23012GB
```



## Create Collections(table)
> MongoDB creates collection automatically, when you insert some document. Also you can create before.
```
>use latestdb
switched to db latestdb
>db.createCollection("mycollection")
{ "ok" : 1 }
```

> Add row to 'users' collection. Created automatically "users" collection.
```
>db.users.insert({"name":"UGUR COBAN"})
>show dbs
local      0.78125GB
mytestdb   0.23012GB
```

> Add row to 'newdb' collection. And Save record. Then, find last one.
```
>db.newdb.save( { a: 1 } )
>db.newdb.find()
{ "_id" : ObjectId(5879b0f65a56a454), "a" : 1 }
```


> Show Collections(tables)
```
>show collections
mycollection
users
newdb
```

## Delete/Drop Database
> If you have not selected any database, then it will delete default 'test' database.
```
>use latestdb
switched to db latestdb
>db.dropDatabase()
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
