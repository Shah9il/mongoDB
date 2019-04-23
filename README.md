# BIG DATA - MongoDB Tutorials
Basic MongoDB functions and tutorials on terminal. Please install mongoDB on your server. And then,

## Start to Mongo DB on terminal(CMD)
```
C:\Users\Your Name>mongo
```



## Create database or use existing database. 
```
>use ugurdb
switched to db ugurdb
```

> Check your db. Your created database (mytestdb), But it is not present in list. (Because no data yet)
```
>db
ugurdb
>show dbs
local     0.000GB
config    0.000GB
admin     0.000GB
```



## Create Collections(table)
> MongoDB creates collection automatically, when you insert some document. Also you can create before.
```
>db.createCollection("logs")
{ "ok" : 1 }
>show dbs
local     0.000GB
config    0.000GB
admin     0.000GB
ugurdb    0.000GB
```

> Add row to 'users' collection. Created automatically "users" collection.
```
>db.users.insert({"name":"UGUR COBAN"})
WriteResult({ "nInserted" : 1 })
>db.users.insert([
   {
      _id: 1, 
      name: 'MongoDB is no sql database',
      tags: ['mongodb', 'database', 'NoSQL'],
      counter: 100
   },
   {
      name: "NoSQL database doesn't have tables",
      counter: 20, 
      comments: [	
         {
            user:'user1',
            message: 'My first comment',
            dateCreated: new Date(2013,11,10,2,35)
         }
      ]
   }
])
BulkWriteResult({
        "writeErrors" : [ ],
        "writeConcernErrors" : [ ],
        "nInserted" : 2,
        "nUpserted" : 0,
        "nMatched" : 0,
        "nModified" : 0,
        "nRemoved" : 0,
        "upserted" : [ ]
})
```

> Add row to 'files' collection. And Save record. Then, find last one.
```
>db.files.save( { file: 'selam.txt' } )
WriteResult({ "nInserted" : 1 })
>db.files.save( { file: 'selam.txt', date:"2019-02-02" } )
WriteResult({ "nInserted" : 1 })
```

> Find(Select) rows
```
>db.files.find()
{ "_id" : ObjectId("5cbeae8fff0796a9ba06538c"), "file" : "selam.txt" }
{ "_id" : ObjectId("5cbeaf68ff0796a9ba06538d"), "file" : "selam.txt", "date" : "2019-02-02" }
>db.users.find();
{ "_id" : ObjectId("5cbeae4fff0796a9ba06538b"), "name" : "UGUR COBAN" }
{ "_id" : 1, "name" : "MongoDB is no sql database", "tags" : [ "mongodb", "database", "NoSQL" ], "counter" : 100 }
{ "_id" : ObjectId("5cbeb287ff0796a9ba06538e"), "name" : "NoSQL database doesn't have tables", "counter" : 20, "comments" : [ { "user" : "user1", "message" : "My first comment", "dateCreated" : ISODate("2013-12-09T23:35:00Z") } ] }
```

> Show Collections(tables)
```
>show collections
files
logs
users
```

## Delete/Drop Database
> If you have not selected any database, then it will delete default 'test' database.
```
>use test
switched to db test
>db.dropDatabase()
{ "dropped" : "test", "ok" : 1 }
```

## Help & Stats & Version
```
>db.help()
>db.stats();
>db.version();
```

## MangoDB Deployment
> To check counters of database operations
```
D:\set up\mongodb\bin>mongostat
```

> Tracks and reports activity
```
D:\set up\mongodb\bin>mongotop
```

## Documentation

* [MongoDB - Download](https://www.mongodb.com/download-center/community)
* [MongoDB - TutorialsPoint Overview](https://www.tutorialspoint.com/mongodb/index.htm)
