# TABLOLAR

Tablolar verilerin satırlar ve sütunlar halinde organize edildiği yapılardır.

Örnek bir tablo yapısı:

| ID | first_name | last_name | salary |
|----|------------|-----------|--------|
| 1  | John       | Doe       | 10000  |
| 2  | Jane       | Smith     | 15000  |

---

### Tablo Oluşturma

Bir tabloyu SQL’de `CREATE TABLE` komutuyla oluşturursunuz. Tabloyu oluştururken sütunların adlarını, veri tiplerini ve varsa ek kısıtlamaları (constraints) belirlemeniz gerekir.

```sql
CREATE TABLE employees (
    id INTEGER,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    salary DECIMAL(10, 2),
    department_id INTEGER
);
```

Bu örnekte:
- id: Bir INTEGER sütunudur.

- first_name ve last_name: VARCHAR(50) veri tipiyle maksimum 50 karakter uzunluğunda metin tutar.

- salary: DECIMAL(10, 2) ile ondalıklı bir sayıdır; 10 hanesi olabilir ve virgülden sonra 2 hane yer alır.

- department_id: İlgili çalışanı bir departmanla ilişkilendirmek için kullanılan bir INTEGER sütunudur.

### Tablo Değiştirme

Bir tabloyu oluşturduktan sonra yeni sütun eklemek, mevcut sütunları değiştirmek veya silmek isterseniz `ALTER TABLE` komutunu kullanabilirsiniz.

Sütun ismi değiştirme:

```sql
ALTER TABLE employees RENAME COLUMN last_name TO middle_name;
```
---

Sütun ekleme:

```sql
ALTER TABLE employees ADD email VARCHAR(100);
```
---
Sütun güncelleme:

```sql
ALTER TABLE employees MODIFY salary DECIMAL(12, 2);
```
---
Sütun silme:
```sql
ALTER TABLE employees DROP COLUMN email;
```