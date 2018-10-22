---
title: MongoDB
---

# MongoDB
## Helpers
```sql
help
db.help()
db.<collection>.help()
```

### Db and Collection
```sql
show dbs
use <db>
show collections
```

### Others
```sql
show users
show roles
show profile
show databases
load()
```

## Basic
```sql
db.auth()
coll = db.<collection>
db.<collection>.find()
db.<collection>.findOne()

coll = db.users;
coll.find({ name: "Joe" });
```

### CRUD
```sql
db.<collection>.insertOne()
db.<collection>.insertMany()

db.<collection>.updateOne()
db.<collection>.updateMany()

db.<collection>.save()

db.<collection>.deleteOne()
db.<collection>.deleteMany()

db.<collection>.drop()
```

### Others
```sql
db.<collection>.createIndex()
db.getSiblingDB()
```

## Queries
### Find
```sql
db.<collection>.find(<query>, <projection>)

coll = db.users;
coll.find( {}, { name: true });
```

### Sort
```sql
db.<collection>.find(<query>).sort(<sort order>)

coll = db.users;
coll.find().sort({ name: 1 });
```

### Limit & Skip
```sql
db.<collection>.find(...).limit( <n>)
db.<collection>.find(...).skip( <n>)
```

### Count
```sql
// count ignores limit() and skip()
db.<collection>.find(<query>).count()
```

## Administrative
```sql
// all host database must be in noauth mode
db.cloneDatabase(<host>)

// copy <from> db from <host> to <to> db on current server
db.copyDatabase(<from>, <to>, <host>)

db.fromColl.renameCollection(<toColl>)
db.getCollectionNames()
db.dropDatabase()
```