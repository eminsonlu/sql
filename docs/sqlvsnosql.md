# SQL vs NoSQL

Temel olarak en büyük fark NoSQL veritabanları SQL dilini kullanmaz. NoSQL veritabanlarının da genel anlamda tek ortak yanı SQL dilini kullanmaması olur. SQL yapısı kullanan veritabanları genel kullanıma daha çok hitap eder. Fakat NoSQL daha spesifik durumlara özgü kullanılması yaygındır.

* SQL kullanan bazı popüler veritabanları
    * MySQL
    * PostgreSQL
    * Oracle
    * SQLite

* NoSQL olan bazı popüler veritabanları ve kullanım amaçları
    * MongoDB - JSON benzeri esnek yapısı vardır. İçerik yönetim sistemi vs gibi yapılara uygundur.
    * Cassandra - Büyük ölçekli, yüksek hız gerektiren yerler için. Örnek veri analizi, sensör işleme...
    * Redis - In Memory olması sebebi ile düşük gecikmelidir. Önbellekleme (Cache) gibi yerlerde yaygındır.
    * Neo4j - Graph yapısı sayesinde sosyal medya uygulamaları gibi çok ilişkili yerlerde uygundur.
    * ElasticSearch - Arama yapılarında uygundur. İstatistiksel analizlerde kullanılır.