# Java 101 - Kodluyoruz / Patika.dev

Bu repo [Kodluyoruz](Kodluyoruz.org) Java 101 eğitimi için hazırlamış olduğum repo. İçerisinde Java pratik ve ödevlerinin soru ve cevaplarını içeren bir adet README dosyası barındırıyor.

| PRATİKLER | ÖDEVLER |
|-----|-----|
| [PRATİK 1](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev/blob/main/README.md#open_book-prati%CC%87k-1--not-ortalamas%C4%B1) - Not Ortalaması | [ÖDEV 1](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-%C3%B6dev-1--v%C3%BCcut-kitle-i%CC%87ndeksi-hesaplama) - Vücut Kitle İndeksi Hesaplama|
| [PRATİK 2](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-2--kdv-hesaplama) - KDV Hesaplama |[ÖDEV 2](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-%C3%B6dev-2--manav-kasa) - Manav Kasa |
| [PRATİK 3](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-3--hipoten%C3%BCs-bulma) - Hipotenüs Bulma|
| [PRATİK 4](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-4--taksimetre) - Taksimetre |
| [PRATİK 5](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-5--daire--alan--%C3%A7evre) - Daire & Alan & Çevre |
| [PRATİK 6](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-6--hesap-makinesi) - Hesap Makinesi|

---

## :open_book: PRATİK 1	- Not Ortalaması

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

## :open_book: PRATİK 2	- KDV Hesaplama

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

## :open_book: PRATİK 3	- Hipotenüs Bulma

### SORU :question:
Dik Üçgende Hipotenüs Bulan Program
Java ile kullanıcıdan dik kenarlarının uzunluğunu alan ve hipotenüsü hesaplayan programı yazın.

:interrobang:
Üç kenar uzunluğunu kullanıcıdan aldığınız üçgenin alanını hesaplayan programı yazınız.


:pushpin: Formül : Üçgenin çevresi = 2𝑢

:pushpin: Formül : 𝑢 = (a+b+c) / 2

:pushpin: Formül : Alan * Alan = 𝑢 * (𝑢 − 𝑎)* (𝑢 − 𝑏) * (𝑢 − 𝑐)


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

## :open_book: PRATİK 4	- Taksimetre

### SORU :question:
Java ile gidilen mesafeye (KM) göre taksimetre tutarını ekrana yazdıran programı yazın.

-Taksimetre KM başına 2.20 TL tutmaktadır.

-Minimum ödenecek tutar 20 TL'dir. 20 TL altında ki ücretlerde yine 20 TL alınacaktır.

-Taksimetre açılış ücreti 10 TL'dir.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik4;
import java.util.Scanner;

public class TaksiMetre {
    public static void main(String[] args) {

    // Değişkenler tanımlandı ve veri girişi için scanner kodu kullanıldı.
    double km, katSayı = 2.2, minUcret = 20, acılısUcret=10, toplamUcret, odenecekUcret;
    Scanner input = new Scanner(System.in);
    System.out.print("Taksimetre uygulaması için KM değerini giriniz : ");
    km = input.nextDouble();

    // Toplam ücret hesaplandı ve km başına olan ücret hesaplanarak sorgulatıldı.
    toplamUcret = acılısUcret+(km*katSayı);
    boolean kosul1 = toplamUcret < 20;
    odenecekUcret = kosul1 ? minUcret : toplamUcret;

    // Hesaplanan ücret ekrana basıldı.
    System.out.print("Toplam ödenecek ücret = " + odenecekUcret + " TL");
    }
}

```
</details>

## :open_book: PRATİK 5	- Daire & Alan & Çevre

### SORU :question:
Dairenin Alanını ve Çevresini Hesaplayan Program
Java ile yarı çapını kullanıcıdan aldığınız dairenin alanını ve çevresini hesaplayan programı yazın.

:pushpin: Alan Formülü : π * r * r;

:pushpin: Çevre Formülü : 2 * π * r;

:interrobang:
Yarıçapı r, merkez açısısının ölçüsü 𝛼 olan daire diliminin alanı bulan programı yazınız.

𝜋 sayısını = 3.14 alınız.

:pushpin: Formül : (𝜋 * (r*r) * 𝛼) / 360

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik5;
import java.util.Scanner;

public class DaireAlanCevre {
    public static void main(String[] args) {
        // Değişkenler tanımlandı ve veri girişi için scanner kodu kullanıldı.
        double yarıCap, alan, cevre, pi=3.14;
        Scanner input = new Scanner(System.in);

        System.out.print("Dairenin yarıçapını (cm cisinden) giriniz : ");
        yarıCap = input.nextDouble();

        // Alan ve cevre hesaplanarak ekrana yazdırıldı.
        alan = pi*yarıCap*yarıCap;
        System.out.println("Dairenin alanı : " + alan + "cm\u00B2");

        cevre = 2*pi*yarıCap;
        System.out.println("Dairenin çevresi : " + cevre + "cm");

        // Daire diliminin alanını bulma ÖDEV
        // Değişkenler tanımlandı ve veri girişi için scanner kodu kullanıldı.
        double merkezAcı, daireDilimAlan;
        System.out.print("Dairenin merkez açısını giriniz : ");
        merkezAcı = input.nextDouble();

        // Daire diliminin alanı hesaplanarak ekrana yazdırıldı.
        daireDilimAlan=(pi*(yarıCap*yarıCap)*merkezAcı)/360;
        System.out.println("Daire diliminin alanı : " + daireDilimAlan + "cm\u00B2");
    }
}

```
</details> 
 
## :open_book: PRATİK 6	- Hesap Makinesi

### SORU :question:
Java koşullu ifadeler ile basit hesap makinesi yapımı.

:pushpin: Hesap makinesini switch-case kullanarak yapınız

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik6;

import java.util.Scanner;

public class HesapMakinesi {
    public static void main(String[] args) {

        // Değişkenler tanımlandı. Sayısal işlemler için double yapılacak olan hesaplamalar operatörler için char kullanıldı.
        double sayi1, sayi2, sonuc;
        char islem;
        Scanner input = new Scanner(System.in);

        // 1. ve 2. sayılar kullanıcıdan istendi. Ardından gerçekleştirilecek işlemin operatörü istendi.
        System.out.print("1. Sayıyı giriniz :");
        sayi1 = input.nextInt();

        System.out.print("2. Sayıyı giriniz :");
        sayi2 = input.nextInt();

        System.out.println("+ ( Toplama )");
        System.out.println("- ( Çıkarma )");
        System.out.println("* ( Çarpma )");
        System.out.println("/ ( Bölme )");
        System.out.print("Yapmak istediğiniz işlem için ilgili sayıyı seçiniz:");

        // Operatör işlemi için char değeri değişkene atandı.
        islem = input.next().charAt(0);

        // Hesaplama yapılması için switch-case kullanıldı ve sonuç ekrana bastırıldı.
        switch (islem) {
            case '+':
                sonuc = sayi1 + sayi2;
                System.out.print("Toplama sonucu = " + sonuc);
                break;
            case '-':
                sonuc = sayi1 - sayi2;
                System.out.print("Çıkarma sonucu = " + sonuc);
                break;
            case '*':
                sonuc = sayi1 * sayi2;
                System.out.print("Çarpma sonucu = " + sonuc);
                break;
            case '/':
                if (sayi2 == 0) {
                    System.out.print("Bir sayı sıfıra bölünemez");
                    break;
                } else {
                    sonuc = sayi1 / sayi2;
                    System.out.print("Bölme sonucu = " + sonuc);
                    break;
                }
            default:
                System.out.print("Lütfen +, -, * veya / işlemlerinden birini seçiniz.");
                break;

        }
    }
}

```
</details> 

## :open_book: ÖDEV 1	- Vücut Kitle İndeksi Hesaplama

### SORU :question:
Vücut Kitle İndeksi Hesaplama
Java ile kullanıcıdan boy ve kilo değerlerini alıp bir değişkene atayın. Aşağıda ki formüle göre kullanıcının "Vücut Kitle İndeks" değerini hesaplayıp ekrana yazdırın.

:pushpin: Formül : Kilo (kg) / Boy(m) * Boy(m)


:heavy_check_mark: Çıktısı
```
Lütfen boyunuzu (metre cinsinde) giriniz : 1,72
Lütfen kilonuzu giriniz : 105
Vücut Kitle İndeksiniz : 35.49215792320173
```
 
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Odev1;
import java.util.Scanner;

public class VucutKitleIndeksi {
    public static void main(String[] args) {

        // Değişkenler tanımlandı ve veri girişi için scanner kodu kullanıldı.
        double boy, kilo, kitleIndeks;
        Scanner input = new Scanner(System.in);

        System.out.print("Lütfen boyunuzu (metre cinsinde) giriniz : ");
        boy = input.nextDouble();

        System.out.print("Lütfen kilonuzu giriniz : ");
        kilo = input.nextDouble();

        // Vücut Kitle İndeksi hesaplanarak ekrana yazdırıldı.
        kitleIndeks = kilo / (boy * boy);
        System.out.print("Vücut Kitle İndeksiniz : " + kitleIndeks);
    }
}

```
</details> 

## :open_book: ÖDEV 2	- Manav Kasa

### SORU :question:
Manav Kasa Programı
Java ile kullanıcıların manavdan almış oldukları ürünlerin kilogram değerlerine göre toplam tutarını ekrana yazdıran programı yazın.

:pushpin: Meyveler ve KG Fiyatları

-Armut : 2,14 TL   
-Elma : 3,67 TL  
-Domates : 1,11 TL  
-Muz: 0,95 TL  
-Patlıcan : 5,00 TL  


:heavy_check_mark: Örnek Çıktı
```
Armut Kaç Kilo ? :0
Elma Kaç Kilo ? :1
Domates Kaç Kilo ? :1
Muz Kaç Kilo ? :2
Patlıcan Kaç Kilo ? :3
Toplam Tutar : 21.68 TL
```

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Odev2;
import java.util.Scanner;

public class ManavKasa {
    public static void main(String[] args) {

        // Değişkenler tanımlandı ve veri girişi için scanner kodu kullanıldı.
        double armutKg=2.14, elmaKg=3.67, domatesKg=1.11, muzKg=0.95, patlicanKg=5, armut, elma, domates, muz, patlican, toplamTutar;
        Scanner input = new Scanner(System.in);

        System.out.print("Armut Kaç Kilo ? :");
        armut = input.nextFloat();

        System.out.print("Elma Kaç Kilo ? :");
        elma = input.nextFloat();

        System.out.print("Domates Kaç Kilo ? :");
        domates = input.nextFloat();

        System.out.print("Muz Kaç Kilo ? :");
        muz = input.nextFloat();

        System.out.print("Patlıcan Kaç Kilo ? :");
        patlican = input.nextFloat();

        // Toplam tutar hesaplanarak ekrana yazdırıldı.
        toplamTutar=(armut*armutKg)+(elma*elmaKg)+(domates*domatesKg)+(muz*muzKg)+(patlican*patlicanKg);
        System.out.print("Toplam Tutar :" + toplamTutar + " TL");
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

