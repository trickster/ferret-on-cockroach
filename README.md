# Ferret on Cockroach DB

```
docker exec -it mongosh mongosh mongodb://ferretdb/ferretdb


ferretdb> db.test.insert({name: "Ada Lovelace", age: 205})
DeprecationWarning: Collection.insert() is deprecated. Use insertOne, insertMany, or bulkWrite.
Uncaught:
MongoBulkWriteError: [msg_insert.go:38 pg.(*Handler).MsgInsert] [pg.go:137 pg.(*Handler).DBPool] pgdb.NewPool: ERROR: database "ferretdb" does not exist (SQLSTATE 3D000)
Result: BulkWriteResult {
  insertedCount: 0,
  matchedCount: 0,
  modifiedCount: 0,
  deletedCount: 0,
  upsertedCount: 0,
  upsertedIds: {},
  insertedIds: { '0': ObjectId("643e0b21a5cd4d0724df4843") }
}```