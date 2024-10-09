<h1 align="center">Overloading (Metot Aşırı Yükleme) Nedir?</h1>

**Overloading**, aynı isimde birden fazla metot tanımlamak anlamına gelir, ancak bu metotların parametre listeleri (parametre sayısı, tipi veya sırası) farklı olmalıdır. Yani, aynı isimde fakat farklı işlevselliklere sahip metotlar oluşturabiliriz. Overloading compile-time (derleme zamanında) çözülür, yani derleme aşamasında hangi metot çağrısının yapılacağı belirlenir.

### Önemli Özellikler:
- Aynı sınıf içinde gerçekleşir.
- Aynı metot ismi kullanılır, ancak parametre sayısı ya da türleri farklı olur.
- Geri dönüş tipi aynı ya da farklı olabilir.
- Compile-time polymorphism (zamanında çok biçimlilik) olarak bilinir.
- Derleme aşamasında hangi metotun kullanılacağı belirlenir.

```java
public class Hesaplayici {

    // İki parametreli topla metodu
    public int topla(int a, int b) {
        return a + b;
    }

    // Üç parametreli topla metodu
    public int topla(int a, int b, int c) {
        return a + b + c;
    }

    // Aynı isimde fakat farklı parametre tipi alan metot
    public double topla(double a, double b) {
        return a + b;
    }
}
```
Bu örnekte, topla metodu aynı isimde olmasına rağmen parametre sayısı ve tipi farklıdır, dolayısıyla overloading yapılmıştır.


## Overriding (Metot Ezme) Nedir?
Overriding, bir sınıfın başka bir sınıftan miras aldığı (inheritance) bir metodu, kendi ihtiyacına göre tekrar tanımlaması anlamına gelir. Bu, metotların aynı isim, aynı parametre listesi ve aynı geri dönüş tipi ile yeniden tanımlanması anlamına gelir. Overriding runtime (çalışma zamanında) çözülür, yani program çalışırken hangi metodun çağrılacağı belirlenir.

### Önemli Özellikler:
- Kalıtım (inheritance) ilişkisi gerektirir. Yani bir alt sınıf, üst sınıfın metodunu ezerek yeniden tanımlar.
- Aynı metot ismi, aynı parametre listesi ve aynı geri dönüş tipi kullanılır.
- Runtime polymorphism (çalışma zamanında çok biçimlilik) olarak bilinir.
- Metot, üst sınıfta tanımlanmış olmalı ve alt sınıfta ezilerek yeniden tanımlanmalıdır.
- @Override ifadesi kullanılarak metot ezildiği açıkça belirtilir (isteğe bağlı, ama önerilir).

```java
class Hayvan {
    // Üst sınıfta bir metot
    public void sesCikar() {
        System.out.println("Hayvan bir ses çıkarıyor");
    }
}

class Kopek extends Hayvan {
    // Alt sınıfta metot overriding
    @Override
    public void sesCikar() {
        System.out.println("Köpek havlıyor");
    }
}
```
Bu örnekte, Kopek sınıfı, Hayvan sınıfından miras almıştır ve sesCikar metodunu ezerek kendi versiyonunu tanımlamıştır.

## Sonuç:
- Overloading, aynı isimde birden fazla metot tanımlanmasını sağlar ancak bu metotların parametre listeleri farklı olmalıdır.
- Overriding, kalıtım ilişkisiyle bir üst sınıftan alınan bir metodun alt sınıfta yeniden tanımlanmasıdır. Overriding, metot davranışını değiştirmeye olanak tanır.



