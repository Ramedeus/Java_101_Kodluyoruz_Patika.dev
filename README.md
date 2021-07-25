# Java 101 - Kodluyoruz / Patika.dev

Bu repo [Kodluyoruz](Kodluyoruz.org) Java 101 eğitimi için hazırlamış olduğum repo. İçerisinde Java pratik ve ödevlerinin soru ve cevaplarını içeren bir adet README dosyası barındırıyor.

| [PRATİK 1](https://github.com/Ramedeus/Java-101---Kodluyoruz---Patika-Dev/blob/main/README.md#open_book-prati%CC%87k-1) |
 [PRATİK 2](https://github.com/Ramedeus/Java-101---Kodluyoruz---Patika-Dev/blob/main/README.md#open_book-prati%CC%87k-2) |
 [PRATİK 3](https://github.com/Ramedeus/Java-101---Kodluyoruz---Patika-Dev/blob/main/README.md#open_book-prati%CC%87k-3) |

---

## :open_book: PRATİK 1	

### SORU :question:
Not Ortalaması Hesaplayan Program
Java ile Matematik, Fizik, Kimya, Türkçe, Tarih, Müzik derslerinin sınav puanlarını kullanıcıdan alan ve ortalamalarını hesaplayıp ekrana bastırılan programı
yazın.

:interrobang: Aynı program içerisinde koşullu ifadeler kullanılarak, eğer kullanıcının ortalaması 60'dan büyük ise ekrana "Sınıfı Geçti" , küçük ise "Sınıfta Kaldı" yazsın.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik1;
import java.util.Scanner;

public class NotOrtalamasi {
    public static void main(String[] args) {

// Değişkenler tanımlandı ve veri girişi için scanner kodu kullanıldı.     
    double mat, fiz, kim, tur, tar, muz;
    Scanner input = new Scanner(System.in);
  
// Kullanıcıdan not değerleri alınarak değişkenlere atandı.       
    System.out.print("Matematik notunuzu giriniz = ");
    mat = input.nextInt();

    System.out.print("Fizik notunuzu giriniz = ");
    fiz = input.nextInt();

    System.out.print("Kimya notunuzu giriniz = ");
    kim = input.nextInt();

    System.out.print("Türkçe notunuzu giriniz = ");
    tur = input.nextInt();

    System.out.print("Tarih notunuzu giriniz = ");
    tar = input.nextInt();

    System.out.print("Müzik notunuzu giriniz = ");
    muz = input.nextInt();

// Değişkenler ile işlemler yapılarak ortalama değer hesaplandı.    
    double toplam = mat+fiz+kim+tur+tar+muz;
    double ortalama = toplam/6;
    
// Bulunan sonuç istenen koşul ile sorgulanarak ekrana yazdırıldı.
    System.out.println("Ortamanız = " + ortalama);
    boolean kosul1 = ortalama >= 50;
    System.out.println("Durum = " + (kosul1==true ? "Geçti" : "Kaldı"));
    
    }
}
```
</details>

## :open_book: PRATİK 2	

### SORU :question:
KDV Tutarı Hesaplayan Program
Java ile kullanıcıdan alınan para değerinin KDV'li fiyatını ve KDV tutarını hesaplayıp ekrana bastıran programı yazın.

(Not : KDV tutarını 18% olarak alın)

KDV'siz Fiyat = 10;

KDV'li Fiyat = 11.8;

KDV tutarı = 1.8;

:interrobang: 
Eğer girilen tutar 0 ve 1000 TL arasında ise KDV oranı %18 , tutar 1000 TL'den büyük ise KDV oranını %8 olarak KDV tutarı hesaplayan programı yazınız.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik2;
import java.util.Scanner;


public class KDVHesaplama {
    public static void main(String[] args) {

// Değişkenler tanımlandı ve veri girişi için scanner kodu kullanıldı.
     double anaPara, kdv, kdvli, kdv18=18, kdv8=8;

// Kullanıcıdan anapara değeri alındı.
        Scanner input = new Scanner(System.in);
        System.out.print("Ana paranızı giriniz :");
        anaPara = input.nextDouble();

// Girilen anaparanın istenen değerler içerisinde olup olmadığı sorgulandı.
        boolean kosul1 = anaPara >= 0;
        boolean kosul2 = anaPara <= 1000;
        boolean sonuc = kosul1 && kosul2;

// KDV değeri sorgulama sonucuna göre işlemlere aktarıldı ve sonuçlar ekrana yazdırıldı.
        System.out.println("KDV'siz Fiyat :" + anaPara);

        kdv= sonuc ? kdv18 : kdv8;
        kdvli = anaPara + ((anaPara * kdv)/100);

        System.out.println("KDV'li Fiyat :" + kdvli);
        System.out.println("KDV tutarı :" + kdv/10);

    }
}

```
</details>

## :open_book: PRATİK 3	

### SORU :question:
Dik Üçgende Hipotenüs Bulan Program
Java ile kullanıcıdan dik kenarlarının uzunluğunu alan ve hipotenüsü hesaplayan programı yazın.

:interrobang:
Üç kenar uzunluğunu kullanıcıdan aldığınız üçgenin alanını hesaplayan programı yazınız.

Formül
Üçgenin çevresi = 2𝑢

𝑢 = (a+b+c) / 2

Alan * Alan = 𝑢 * (𝑢 − 𝑎)* (𝑢 − 𝑏) * (𝑢 − 𝑐)


### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik3;
import java.util.Scanner;

public class Hipotenus {
    public static void main(String[] args) {
    // Değişkenler tanımlandı ve veri girişi için scanner kodu kullanıldı.

    double  a, b, c;
    Scanner input = new Scanner(System.in);

    // Dik üçgenin 1. ve 2. kenarı kullanıcıdan istendi.
    System.out.print("Diküçgenin 1. kenarını giriniz :");
    a = input.nextDouble();

    System.out.print("Diküçgenin 2. kenarını giriniz :");
    b = input.nextDouble();

    // Hipotenüs hesaplandı.
    c = Math.sqrt ((a*a)+(b*b));
    System.out.println("Hipotenüs :" + c);


    // Üçgen alanını bulma ÖDEV
    System.out.println("Bir Üçgenin Alanının Hesaplaması");

    // Üçgenin kenarları kullanıcıdan istendi.
    System.out.print("Üçgenin 1. kenarını giriniz :");
    a = input.nextInt();

    System.out.print("Üçgenin 2. kenarını giriniz :");
    b = input.nextInt();

    System.out.print("Üçgenin 3. kenarını giriniz :");
    c = input.nextInt();

    // Hesaplamalar için değişkenler oluşturuldu.
    double alan, u;

    // Hesaplamalar yapıldı ve üçgenin alanı ekrana bastırıldı.
    u=(a+b+c)/2;
    alan = Math.sqrt (u*(u-a)*(u-b)*(u-c));

    System.out.print("Üçgenin alanı :" + alan);
    }
}
```
</details> 
 
---

## Contributing :hammer_and_wrench:	
Hatalar, öneriler ve değişiklikler için lütfen bir konu açınız.

## License :notebook_with_decorative_cover:

[MIT](https://www.google.com/search?q=mit+license&oq=mit+license&aqs=chrome.0.0l4j0i22i30l6.2910j0j7&sourceid=chrome&ie=UTF-8)


![Lorem Picsum](https://picsum.photos/200/300)

