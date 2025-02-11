[[SQL-Drop-Type]]
[discrete]
### SQL - `DROP TYPE` 
image:../images/edit.png[link="https://github.com/ArcadeData/arcadedb-docs/blob/main/src/main/asciidoc/sql/SQL-Drop-Type.md" float=right]

Removes a type from the schema.

**Syntax**

```sql
DROP TYPE <type> [ UNSAFE ]
```

- **`<type>`** Defines the type you want to remove.
- **`UNSAFE`** Defines whether the command drops non-empty edge and vertex typees.  Note, this can disrupt data consistency.  Be sure to create a backup before running it.



NOTE: Bear in mind, that the schema must remain coherent.  For instance, avoid removing calsses that are super-typees to others.  This operation won't delete the associated bucket.

**Examples**

- Remove the type `Account`:

```
ArcadeDB> DROP TYPE Account
```


For more information, see:

- <<SQL-Create-Type,`CREATE TYPE`>>
- <<SQL-Alter-Type,`ALTER TYPE`>>
- <<SQL-Alter-Bucket,`ALTER BUCKET`>>

