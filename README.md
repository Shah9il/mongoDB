# BIG DATA - MongoDB Tutorials
Basic MongoDB functions and tutorials on terminal. Please install mongoDB on your server. And then,

# Start to terminal (CMD)
```
D:\set up\mongodb\bin>mongo.exe
```

## Create database or use existing database.
```
>use mytestdb
switched to db mytestdb
```

## To check your currently selected database, use the command db
```
>db
mytestdb
```

## If you want to check your databases list, use the command show dbs.
```
>show dbs
local     0.78125GB
test      0.23012GB
```

## Your created database (mytestdb) is not present in list. I added to users collection(table).
```
>db.users.insert({"name":"UGUR COBAN"})
>show dbs
local      0.78125GB
mytestdb   0.23012GB
test       0.23012GB
```

## Save and Find in "test" db
```
>db.test.save( { a: 1 } )
>db.test.find()
{ "_id" : ObjectId(5879b0f65a56a454), "a" : 1 }
```

## Help & DB Stats
```
>db.help()
>db.stats();
```


## Documentation

* [MongoDB - Download](https://www.mongodb.com/download-center/community)
* [Nodejs - TutorialsPoint MongoDB](https://www.tutorialspoint.com/mongodb/index.htm)
