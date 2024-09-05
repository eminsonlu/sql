# NOT NULL

Bir sütunun boş veya tanımsız (NULL) değerini almasını engeller. Değer girilmesini zorunlu kılar.

```sql
CREATE TABLE products (
    id INT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    category VARCHAR(255) -- category sütunu boş olabilir
);
```