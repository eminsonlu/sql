## Primary Key

Tablodaki bir satırı benzersiz şekilde tanımlamanızı sağlar. Bunun en büyük ve en sık kullanılan örneği oluşturduğumuz çoğu tabloda `id` değerini kullanılır ve bu değeri `PRIMARY KEY` yaparız. Böylece o değere `id` değerini kullanarak çok hızlı ulaşabiliriz. Örnek bir tablo:

```sql

CREATE TABLE users (
    id INT PRIMARY KEY,
    name TEXT
);
```

---
| ID | name         |
|----|--------------|
| 1  | John Doe     |
| 2  | Lissa Shell  |
| 3  | Silvia Colin |

---

Tabloda `PRIMARY KEY` sadece bir defa verilebilir. Bir veya birden fazla sütun içerebilir:

```sql
CREATE TABLE users (
    id INT,
    name TEXT,
    email TEXT,
    CONSTRAINT PK_users PRIMARY KEY (id, name)
);
```

Buradaki `PK_users` bizim belirlediğimiz bir isimdir. Vermek zorunda değilsiniz, bu durumda MySQL sizin için bir isim belirleyebilecektir. `PRIMARY KEY` olan sütunlarda `NULL` değeri bulunmaz.

Bu şekilde tablo oluştururken genel anlamda `id` değerini biz belirlemeyiz. Bunu otomatik yapmasını isteriz.

```sql
CREATE TABLE kitaplar (
    kitap_id INT AUTO_INCREMENT PRIMARY KEY,
    kitap_adi VARCHAR(255),
    yazar VARCHAR(255)
);
```

Yukarıda gördüğünüz gibi `AUTO_INCREMENT` bizim için oluşturup değeri artıracaktır.