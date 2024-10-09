<h1 align="center">Primitive Data Types</h1>

![image](https://github.com/user-attachments/assets/882cf020-a2d5-4659-ae6d-7233b5a5189c)
- Primitive typle'lar stack'te saklanır.
- primitive typle'lara ulaşmak, Non primitive typle'lara göre daha hızlıdır.
- Null değeri alamazlar
- Değerleri sabittir.

# Non - primitive data types
![image](https://github.com/user-attachments/assets/0eee77fd-649b-4448-802a-aee99950e74a)

- Bellek adresleri stack'te saklanır.İçerikleri heap'de saklanır.
- Null değer alabilirler.
- Bellekte tuttukları alanlar değişiklik gösterebilir.
- Daha yavaştırlar, çünkü bellekteki referanslar aracılığıyla işlenirler.
- non-primitive type'ların kullanılmayanları Garbage collector tarafından toplanır.

# Garbage Collector'ın Çalışma Prensibi
Java'da, nesneler heap adı verilen bellek alanında depolanır. Bir nesneye referans edilmediğinde, yani programda artık o nesneye ulaşılmıyorsa, garbage collector devreye girer ve bu nesneyi bellekten temizler. Böylece bellekte boş alan açılır ve yeni nesneler için yer sağlanmış olur.

### Garbage Collector'ın Temel Görevleri

**Bellek Yönetimi:** Kullanılmayan nesneleri tespit eder ve bellekten temizler.

**Bellek Sızıntılarını Önleme:** Kendi başına bellek yönetimi yaparken oluşabilecek bellek sızıntılarını önler.

**Programın Performansını Arttırma:** Bellekte gereksiz yer işgal eden nesneleri temizleyerek daha verimli bir bellek kullanımı sağlar.

# Java'nın Neden Garbage Collector'a İhtiyacı Var?
Java'da garbage collector, C ve C++ gibi dillerdeki manuel bellek yönetiminden farklıdır. Bu dillerde bellekten silinmesi gereken nesneleri programcının manuel olarak temizlemesi gerekir (örneğin, malloc ve free gibi fonksiyonlar kullanılır). Java'da bu iş, garbage collector tarafından yapılır ve böylece olası bellek sızıntıları ya da program çökmelerinin önüne geçilir.

Özetle, Garbage Collector, Java'da bellek yönetimini otomatik hale getirerek programcıların işini kolaylaştırır ve uygulamaların daha güvenli ve verimli bir şekilde çalışmasını sağlar.



