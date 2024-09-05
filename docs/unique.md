# UNIQUE

UNIQUE kısıtlaması bir tabloya eklenen sütun veya sütunların içerdiği verilerin birbirinden farklı olmasını zorunlu kılar. Verilerin benzersiz olmasını sağlar ve tekrarı engeller.

Bu kısıtlamayı en çok [many-to-many](https://en.wikipedia.org/wiki/Many-to-many_(data_model)) veri modelinde kullanırız.

---

- Eğer bir sütuna `UNIQUE` uyguladıysanız:

    - O sütundaki her değer benzersiz olmalıdır.
    - `NULL` değerler benzersiz olarak kabul edilir.

    -   ```sql
        CREATE TABLE kullanicilar (
            id INT PRIMARY KEY,
            email VARCHAR(255) UNIQUE,
            kullanici_adi VARCHAR(100)
        );
        ```

---

- Birden fazla `UNIQUE` uyguladıysanız:

    - Her kombinasyon kendi içerisinde benzersiz olmalıdır.

    - ```sql
        CREATE TABLE urunler (
            name VARCHAR(255) UNIQUE,
            kategori_id INT,
            urun_adi VARCHAR(255),
            UNIQUE (kategori_id, urun_adi)
        );
        ```

---

- Birden fazla sütunda `UNIQUE` uyguladıysanız:

    - Uygulanan sütunlar birlikte değerlendirilir.

---

`ALTER TABLE` ile kullanım:

```sql
ALTER TABLE kullanicilar
ADD CONSTRAINT unique_email UNIQUE (email);
```

