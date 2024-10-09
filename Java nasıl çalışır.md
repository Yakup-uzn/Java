<h1> JAVA MÜLAKAT SORULARI </h1>

<h2>Java nasıl çalışır ? :</h2>

![image](https://github.com/user-attachments/assets/4790d1bb-583c-4457-9a04-8bd0223c8186)

# Java Kaynağı (Java Source)
İlk olarak, Java'da bir kaynak kodu yazarız. Örneğin:

```java

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
Bu kod, bir .java uzantılı dosyaya kaydedilir, örneğin: HelloWorld.java.

# 2. Java Derleyici (Java Compiler)
Yazılan bu kaynak kodu, derleyici kullanılarak bytecode'a dönüştürülür. Bu işlemi yapmak için terminalde şu komut yazılır:

```bash
javac HelloWorld.java
```
Bu komut, Java derleyicisini (javac) çağırır ve HelloWorld.java dosyasını derler. Sonuç olarak, Java bytecode'u içeren HelloWorld.class dosyası oluşturulur.

Bu bytecode platform bağımsızdır. Yani bu bytecode, hangi işletim sisteminde çalıştırılırsa çalıştırılsın, aynı kalır.

# 3. Bytecode Taşınması
Oluşturulan HelloWorld.class dosyası, yerel bir sistemde veya bir ağ üzerinden başka bir bilgisayara taşınabilir. Java'nın bu özelliği, kodun bir kez yazılıp her platformda çalışabilmesini sağlar.

4. Çalışma Zamanı Ortamı (Run-time Environment)
Bytecode, artık Java'nın Çalışma Zamanı Ortamı (JRE - Java Runtime Environment) ile çalıştırılmaya hazırdır. Burada birkaç önemli bileşen devreye girer:

Sınıf Yükleyici (Class Loader): HelloWorld.class dosyasındaki bytecode belleğe yüklenir. Sınıf yükleyici, çalıştırılacak sınıfı bulur ve belleğe yerleştirir.

Bytecode Doğrulayıcı (Bytecode Verifier): Belleğe yüklenen bytecode, güvenlik açısından kontrol edilir. Java, güvenlik açısından oldukça katıdır, bu yüzden bytecode'un düzgün ve güvenli olup olmadığını kontrol eder. Yanlış, bozuk veya zararlı kodlar varsa çalışma durdurulur.

5. Çalışma Sistemi (Runtime System)
Belleğe yüklenen ve doğrulanan bytecode, JVM (Java Virtual Machine) tarafından çalıştırılmaya başlar. JVM, iki farklı yol ile bytecode'u çalıştırabilir:

Java Yorumlayıcı (Java Interpreter): Bytecode'u satır satır okur ve her satırı anında çalıştırır. Bu yöntem biraz daha yavaş olabilir çünkü her satırda bytecode tekrar yorumlanır.

Anında Derleyici (Just-in-time Compiler - JIT): JVM, bytecode'u optimize ederek makine diline çevirir ve daha hızlı çalışması için yerel makine kodu olarak çalıştırır. Bu yöntem, performans açısından daha hızlıdır. JVM, sık kullanılan kod parçalarını makine diline çevirip tekrar kullanır.

6. İşletim Sistemi ve Donanım (Operating System & Hardware)
Son olarak, JVM tarafından çalıştırılan bytecode, işletim sistemi üzerinden donanıma iletilir. Java programı, işletim sistemi üzerinde çalışırken işlemcide gerekli işlemleri yapar.

Örneğin, HelloWorld.class dosyasını çalıştırmak için şu komut kullanılır:

```bash
java HelloWorld
```
Bu komut, JVM'i başlatır ve bytecode'u çalıştırır. Ekranda şu çıktıyı görürüz:

```bash
Hello, World!
```
Bu şekilde, Java'da yazılan bir kodun nasıl derlenip çalıştığı adım adım gerçekleşir.

Sürecin Özeti:
Yazma: Java kodu .java dosyasına yazılır.
Derleme: javac komutu ile bytecode'a çevrilir (.class dosyası).
Bytecode: Bu bytecode her platformda aynıdır ve taşınabilir.
Çalıştırma: JVM bytecode'u yükler, doğrular, ve çalıştırır. (Yorumlayıcı veya JIT kullanılır.)
Sonuç: Program işletim sistemi ve donanım üzerinde çalışır ve çıktı üretir.
