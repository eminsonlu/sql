# CONSTRAINTS

Kısıtlamalar tabloda kuralları belirlemek için kullanılır.

Kısıtlamaları kullanarak tablonun ihtiyacımıza göre veri ekleme, veri girişi gibi işlemlerini hızlandırabiliriz.

```sql
CREATE TABLE table_name (
    id datatype constraint,
    name datatype constraint,
    number datatype constraint
);
```

Çoğunlukla SQL de kullanılan kısıtlamalar:

* [PRIMARY KEY](./docs/primarykey.md)
* [FOREIGN KEY](./docs/foreignkey.md)
* [UNIQUE](./docs/unique.md)
* [NOT NULL](./docs/notnull.md)
