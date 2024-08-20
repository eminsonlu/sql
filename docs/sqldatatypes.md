# SQL Veri Türleri

SQL dili birden fazla türü destekleyebilir. Veritabanı yönetim sisteminizin ([DBMS](https://en.wikipedia.org/wiki/Database#:~:text=A%20database%20management%20system%20(DBMS))) desteklediği türler sizin kullandığınız veritabanına göre değişiklik gösterecektir.

Örneğin MySQL veritabanın desktelediği bazı veri türleri şunlardır:

- `INT` - -2,147,483,648 ile 2,147,483,647 arasında (SIGNED) veya 0 ile 4,294,967,295 arasında (UNSIGNED) tam sayıları depolar.
- `DATE` - Yıl, ay ve gün bilgilerini (YYYY-MM-DD formatında) depolar.
- `VARCHAR` - Değişken uzunlukta karakter dizilerini depolar (örneğin, VARCHAR(255)). Uzunluk belirtmeniz gerekir. Daha esnek veri yapıları için uygundur.
- `TEXT` - Maksimum 65,535 karakter uzunluğunda metinleri depolar. `LONGTEXT` 4,294,967,295 karakter uzunluğunda metinleri depolar.
- `BLOB` - Maksimum 65,535 byte boyutunda ikili verileri depolar. Genellikle dosya depolama için kullanılır.
- `BOOL` - Mantıksal değerleri (TRUE, FALSE) depolar. MySQL'de aslında TINYINT(1) olarak temsil edilir.