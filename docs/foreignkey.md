# FOREIGN KEY

İlişkisel veri tabanlarının yapı taşlarından biridir. Tablolar arasında belirli sütun veya sütunların birbiri ile olan ilişkisini sağlar. Bu işlemde bağladığımız sütun veya sütunların karşılığı [PRIMARY KEY](./primarykey.md) veya [UNIQUE](./unique.md) olmalıdır. 

Temel kullanım:

```sql
-- Ana tablo
CREATE TABLE categs (
    id INT PRIMARY KEY,
    name VARCHAR(255) NOT NULL
);

-- Bağlı tablo
CREATE TABLE products (
    id INT PRIMARY KEY,
    name VARCHAR(255) NOT NULL
    categ_id INT,
    FOREIGN KEY (categ_id) REFERENCES categs(id)
)
```

Products tablosundaki `categ_id` sütunu categs tablosundaki `id` sütununu referans aldı. Bunun anlamı ürünler tablosuna giren her `categ_id` değerinin categs tablosundaki id değerlerinden birine eşit olmasını zorunlu kılar.

---
Cascade İşlemleri:

```sql
CREATE TABLE products (
    id INT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    categ_id INT,
    FOREIGN KEY (categ_id) REFERENCES categs(id)
    ON DELETE CASCADE
    ON UPDATE CASCADE
);
```

`ON DELETE CASCADE`: `categs` tablosundaki `id` silindiğinde bu id değerini içeren ürünlerde otomatik olarak silinir.

`ON DELETE UPDATE`: `categs` tablosundaki `id` güncellenirse bu id değerinin bulunduğu tüm ürünlerinde `categ_id` değeri güncellenir.