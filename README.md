# Java 101 - Kodluyoruz / Patika.dev

Bu repo [Kodluyoruz](Kodluyoruz.org) Java 101 eğitimi için hazırlamış olduğum repo. İçerisinde Java pratik ve ödevlerinin soru ve cevaplarını içeren bir adet README dosyası barındırıyor.

| PRATİKLER | ÖDEVLER |
|-----|-----|
| [PRATİK 1](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev/blob/main/README.md#open_book-prati%CC%87k-1--not-ortalamas%C4%B1) - Not Ortalaması | [ÖDEV 1](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-%C3%B6dev-1--v%C3%BCcut-kitle-i%CC%87ndeksi-hesaplama) - Vücut Kitle İndeksi Hesaplama|
| [PRATİK 2](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-2--kdv-hesaplama) - KDV Hesaplama |[ÖDEV 2](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-%C3%B6dev-2--manav-kasa) - Manav Kasa |
| [PRATİK 3](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-3--hipoten%C3%BCs-bulma) - Hipotenüs Bulma| [ÖDEV 3](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-%C3%B6dev-3--u%C3%A7ak-bileti-fiyat%C4%B1-hesaplama) - Uçak Bileti Fiyatı Hesaplama|
| [PRATİK 4](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-4--taksimetre) - Taksimetre | [ÖDEV 4](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-%C3%B6dev-4--%C3%A7in-zodya%C4%9F%C4%B1-hesaplama) - Çin Zodyağı Hesaplama|
| [PRATİK 5](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-5--daire--alan--%C3%A7evre) - Daire & Alan & Çevre |
| [PRATİK 6](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-6--hesap-makinesi) - Hesap Makinesi|
| [PRATİK 7](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev#open_book-prati%CC%87k-7--kullan%C4%B1c%C4%B1-giri%C5%9Fi) - Kullanıcı Girişi|
| [PRATİK 8](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev/blob/main/README.md#open_book-prati%CC%87k-8--s%C4%B1n%C4%B1f%C4%B1-ge%C3%A7me-durumu) - Sınıfı Geçme Durumu|
| [PRATİK 9](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev/blob/main/README.md#open_book-prati%CC%87k-9--hava-s%C4%B1cakl%C4%B1%C4%9F%C4%B1na-g%C3%B6re-etkinlik-%C3%B6nerme) - Hava Sıcaklığına Göre Etkinlik Önerme|
| [PRATİK 10](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev/blob/main/README.md#open_book-prati%CC%87k-10--say%C4%B1lar%C4%B1-b%C3%BCy%C3%BCkten-k%C3%BC%C3%A7%C3%BC%C4%9Fe-s%C4%B1ralayan-program) - Sayıları Büyükten Küçüğe Sıralayan Program|
| [PRATİK 11](https://github.com/Ramedeus/Java_101_Kodluyoruz_Patika.dev/blob/main/README.md#open_book-prati%CC%87k-11--bur%C3%A7-bulan-program) - Burç Bulan Program|

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
Java ile kullanıcıdan alınan para değerinin KDV'li fiyatını ve KDV tutarını hesaplayıp ekrana bastıran programı yazın. (Not : KDV tutarını 18% olarak alın)

:pushpin:KDV'siz Fiyat = 10;   
:pushpin:KDV'li Fiyat = 11.8;   
:pushpin:KDV tutarı = 1.8;   

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

:pushpin: Taksimetre KM başına 2.20 TL tutmaktadır.   
:pushpin: Minimum ödenecek tutar 20 TL'dir. 20 TL altında ki ücretlerde yine 20 TL alınacaktır.   
:pushpin: Taksimetre açılış ücreti 10 TL'dir.   

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

:pushpin: Hesap makinesini switch-case kullanarak yapınız.

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

## :open_book: PRATİK 7	- Kullanıcı Girişi

### SORU :question:
Java koşullu ifadeler ile kullanıcı adı ve şifreyi kontrol eden program yapımı.
  
:interrobang: Eğer şifre yanlış ise kullanıcıya şifresini sıfırlayıp sıfırlamayacağını sorun, eğer kullanıcı sıfırlamak isterse yeni girdiği şifrenin hatalı girdiği ve unuttuğu şifre ile aynı olmaması gerektiğini kontrol edip , şifreler aynı ise ekrana "Şifre oluşturulamadı, lütfen başka şifre giriniz." sorun yoksa "Şifre oluşturuldu" yazan programı yazınız.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik7;

import java.util.Scanner;

public class KullaniciGirisi {
    public static void main(String[] args) {

        //Değişken tanımlamaları
        String userName, passWord;
        char sifreCevap;

        Scanner input = new Scanner(System.in);

        // Kullanıcıdan username ve password girişinin istenmesi
        System.out.print("Lütfen kullanıcı adınızı giriniz: ");
        userName = input.nextLine();

        System.out.print("Lütfen şifrenizi giriniz: ");
        passWord = input.nextLine();

        // Alınan bilgilerin kontrolü ve hatalı işlem cevapları
        if (userName.equals("patika")) {
            if (passWord.equals("dev")) {
                System.out.println("Sisteme başarılı bir şekilde giriş yaptınız.");
            } else {
                System.out.println("Hatalı şifre girişi !!!");
                System.out.print("Şifrenizi sıfırlamak ister misiniz? E/H : ");
                sifreCevap = input.next().charAt(0);

                if (sifreCevap == 'E') {

                    System.out.print("Lütfen yeni şifrenizi giriniz: ");
                    // Eğer String newPassword = input.nextline(); olarak yazılmış olsaydı sistem bu kodu atlayacaktı.
                    // Bu nedenle input.next(); olarak değer aldırıldı.
                    String newPassword = input.next();

                    if (newPassword.equals(passWord) || newPassword.equals("dev")) {
                        System.out.print("Şifre oluşturulamadı");
                    } else {
                        System.out.print("Şifre oluşturuldu.");
                    }
                } else if (sifreCevap == 'H') {
                    System.out.print("Şifre oluşturma işlemi iptal edildi..");

                } else {
                    System.out.print("Lütfen geçerli bir parametre giriniz. E (Evet) veya H (Hayır) !!!");
                }
            }
        } else {
            System.out.println("Hatalı kullanıcı adı girişi !!!");
        }
    }
}

```
</details> 

## :open_book: PRATİK 8	- Sınıfı Geçme Durumu

### SORU :question:
Java koşullu ifadeler ile kullanıcının not durumuna göre sınıfı geçme durumunu hesaplayan program yapımı.

:pushpin: Dersler : Matematik, Fizik, Türkçe, Kimya, Müzik   
:pushpin: Geçme Notu : 55   

:interrobang: Eğer girilen ders notları 0 veya 100 arasında değil ise ortalamaya katılmasın.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik8;

import java.util.Scanner;

public class SinifiGecmeDurumu {

    public static void main(String[] args) {

        /* Her bir ders için değişkenler tanımlandı. Ortalamanın düzgün bir şekilde bölümü için dersSayisi değişkeni
        *  önceden değeri 5 ders olacak şekilde atandı.*/

        int matematik, fizik, turkce, kimya, muzik, dersSayisi = 5;
        double ortalama;
        Scanner input = new Scanner(System.in);

        // Kullanıcıdan ders notları istendi.
        System.out.print("Lütfen matematik notunuzu giriniz : ");
        matematik = input.nextInt();

        System.out.print("Lütfen fizik notunuzu giriniz : ");
        fizik = input.nextInt();

        System.out.print("Lütfen Türkçe notunuzu giriniz : ");
        turkce = input.nextInt();

        System.out.print("Lütfen kimya notunuzu giriniz : ");
        kimya = input.nextInt();

        System.out.print("Lütfen müzik notunuzu giriniz : ");
        muzik = input.nextInt();

        /* Girilen değerlerin 0'dan küçük veya 100'den büyük olma ihtimali kıyaslandı.Eğer koşullar doğru ise
        *  dersSayisi 1 eksiltilerek ilgili ders ortalama hesabından çıkarıldı.*/
        if (matematik < 0 || matematik > 100) {
            matematik = 0;
            dersSayisi--;
        }

        if (fizik < 0 || fizik > 100) {
            fizik = 0;
            dersSayisi--;
        }

        if (turkce < 0 || turkce > 100) {
            turkce = 0;
            dersSayisi--;
        }

        if (kimya < 0 || kimya > 100) {
            kimya = 0;
            dersSayisi--;
        }

        if (muzik < 0 || muzik > 100) {
            muzik = 0;
            dersSayisi--;
        }

        // Ortalama hesabının yapılması ve sonucun ekrana bastırılması.
        ortalama = (matematik + fizik + turkce + kimya + muzik) / dersSayisi;

        if (ortalama >= 55 && ortalama <= 100) {
            System.out.print("Geçtiniz :) Ortalamanız = " + ortalama);
        } else if (ortalama < 55 && ortalama >= 0) {
            System.out.print("Kaldınız :( Ortalamanız = " + ortalama);
        }
    }
}
```
</details>

## :open_book: PRATİK 9	- Hava Sıcaklığına Göre Etkinlik Önerme

### SORU :question:
Java koşullu ifadeler ile hava sıcaklığına göre etkinlik öneren program yapımı.

:pushpin: Koşullar :   
- Sıcaklık 5'dan küçük ise "Kayak" yapmayı öner.   
- Sıcaklık 5 ve 15 arasında ise "Sinema" etkinliğini öner.   
- Sıcaklık 15 ve 25 arasında ise "Piknik" etkinliğini öner.   
- Sıcaklık 25'ten büyük ise "Yüzme" etkinliğini öner.   

:interrobang: Aynı örnek üzerinden if koşulları başka hangi şekilde oluşturulabilirdi farklı çözüm yolları bulunuz.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik9;

import java.util.Scanner;

public class HavaSicakligiEtkinlikOnerme {
    public static void main(String[] args) {

        // IF İLE ÇÖZÜM
        System.out.println("\n!!! IF İLE ÇÖZÜM !!!\n");

        // Değişkenlerin tanımlanması ve kullanıcıdan sıcaklık değerinin aldırılması.
        int sicaklik;
        Scanner input = new Scanner(System.in);
        System.out.print("lütfen sıcaklık değerini giriniz : ");
        sicaklik = input.nextInt();

        // Koşulların sorgulanarak ekrana yazdırılması.
        if (sicaklik < 5) {
            System.out.println("Kayak yapabilirsiniz.");
        } else if (sicaklik < 15) {
            System.out.println("Sinemaya gidebilirsiniz.");
        } else if (sicaklik == 15) {
            System.out.println("Sinemaya gidebilirsiniz.");
            System.out.println("Pikniğe gidebilirsiniz.");
        } else if (sicaklik <= 25) {
            System.out.println("Pikniğe gidebilirsiniz.");
        } else {
            System.out.println("Yüzmeye gidebilirsiniz.");
        }

        // BOOLEAN İLE ÇÖZÜM
        System.out.println("\n!!! BOOLEAN İLE ÇÖZÜM !!!\n");

        System.out.print("lütfen sıcaklık değerini giriniz : ");
        sicaklik = input.nextInt();
        String sonuc;

        // Sıcaklık 25 derece ve üstü ise kosul5 olsaydı eğer her zaman doğru çıkacaktı.
        // Bu nedenle aşağıdaki sorgulamanın son bölümünde kullanıldı.
        boolean kosul1 = sicaklik < 5; // Kayak
        boolean kosul2 = sicaklik >= 5 && sicaklik < 15; // Sinema
        boolean kosul3 = sicaklik == 15; // Sineme ve Piknik
        boolean kosul4 = (sicaklik > 15 && sicaklik <= 25); // Piknik        

        // Koşulların sorgulanması.
        sonuc = kosul1 ? "Kayak yapabilirsiniz." :
                kosul2 ? "Sinemaya gidebilirsiniz." :
                kosul3 ? "Sinemaya gidebilirsiniz. " + "\nPikniğe gidebilirsiniz." :
                kosul4 ? "Pikniğe gidebilirsiniz." :
                         "Yüzmeye gidebilirsiniz.";

        // Sonucun yazdırılması.
        System.out.println(sonuc);

    }
}


```
</details>  

## :open_book: PRATİK 10	- Sayıları Büyükten Küçüğe Sıralayan Program

### SORU :question:
Java koşullu ifadeler ile girilen 3 sayıyı büyükten küçüğe sıralayan program yapımı.

:interrobang: Girilen 3 sayıyı "küçükten büyüğe" sıralayan programı yazınız.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik10;

import java.util.Scanner;

public class SayiBuyuktenKucuge {
    public static void main(String[] args) {

        //Sayılar için değişlenler oluşturuldu.
        int s1, s2, s3;
        Scanner input = new Scanner(System.in);

        // Kullanıcıdan sayı değerleri istendi.
        System.out.print("Lütfen 1. Sayıyı giriniz : ");
        s1 = input.nextInt();

        System.out.print("Lütfen 2. Sayıyı giriniz : ");
        s2 = input.nextInt();

        System.out.print("Lütfen 3. Sayıyı giriniz : ");
        s3 = input.nextInt();

        // BÜYÜKTEN KÜÇÜĞE SIRALAMA
        System.out.println("!!! BÜYÜKTEN KÜÇÜĞE SIRALAMA !!!");

        // Alınan değerler kıyaslanarak yazdırıldı.
        if (s1 > s2 && s1 > s3) {
            if (s2 > s3) {
                System.out.println("s1>s2>s3");
            } else {
                System.out.println("s1>s3>s2");
            }
        } else if (s2 > s1 && s2 > s3) {
            if (s1 > s3) {
                System.out.println("s2>s1>s3");
            } else {
                System.out.println("s2>s3>s1");
            }
        } else {
            if (s1 > s2) {
                System.out.println("s3>s1>s2");
            } else {
                System.out.println("s3>s2>s1");
            }
        }

        // KÜÇÜKTEN BÜYÜĞE SIRALAMA
        System.out.println("\n!!! KÜÇÜKTEN BÜYÜĞE SIRALAMA !!!");

        if (s1 < s2 && s1 < s3) {
            if (s2 < s3) {
                System.out.println("s1<s2<s3");
            } else {
                System.out.println("s1<s3<s2");
            }
        } else if (s2 < s1 && s2 < s3) {
            if (s1 < s3) {
                System.out.println("s2<s1<s3");
            } else {
                System.out.println("s2<s3<s1");
            }
        } else {
            if (s1 < s2) {
                System.out.println("s3<s1<s2");
            } else {
                System.out.println("s3<s2<s1");
            }
        }
    }
}

```
</details>
  
## :open_book: PRATİK 11	- Burç Bulan Program

### SORU :question:
Java koşullu ifadeler ile kullanıcının burcunu bulan program yapımı.

:pushpin: Tarihler:
- Koç Burcu : 21 Mart - 20 Nisan   
- Boğa Burcu : 21 Nisan - 21 Mayıs   
- İkizler Burcu : 22 Mayıs - 22 Haziran   
- Yengeç Burcu : 23 Haziran - 22 Temmuz   
- Aslan Burcu : 23 Temmuz - 22 Ağustos   
- Başak Burcu : 23 Ağustos - 22 Eylül   
- Terazi Burcu : 23 Eylül - 22 Ekim   
- Akrep Burcu : 23 Ekim - 21 Kasım   
- Yay Burcu : 22 Kasım - 21 Aralık   
- Oğlak Burcu : 22 Aralık - 21 Ocak   
- Kova Burcu : 22 Ocak - 19 Şubat   
- Balık Burcu : 20 Şubat - 20 Mart   

:interrobang: Aynı örneği switch-case kullanmadan yapınız.



### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Pratik11;

import java.util.Scanner;

public class BurcBulanProgram {
    public static void main(String[] args) {

        // Değişkenler oluşturuldu kullanıcıdan gün ve ay bilgisi istendi.
        int ay, gun;
        Scanner input = new Scanner(System.in);

        System.out.print("Kaçıncı ayda doğdunuz ? : ");
        ay = input.nextInt();

        System.out.print("Ayın kaçında doğdunuz ? : ");
        gun = input.nextInt();


        // SWTICH-CASE İLE ÇÖZÜM
        System.out.print("!!! SWITCH-CASE İLE ÇÖZÜM !!!\n");

        switch (ay){
            case 1:
                if(gun>=22){
                    System.out.println("Kova Burcu");
                } else {
                    System.out.println("Oğlak Burcu");
                }
                break;

            case 2:
                if(gun>=20){
                    System.out.println("Balık Burcu");
                } else {
                    System.out.println("Kova Burcu");
                }
                break;

            case 3:
                if(gun>=21){
                    System.out.println("Koç Burcu");
                } else {
                    System.out.println("Balık Burcu");
                }
                break;

            case 4:
                if(gun>=21){
                    System.out.println("Boğa Burcu");
                } else {
                    System.out.println("Koç Burcu");
                }
                break;

            case 5:
                if(gun>=22){
                    System.out.println("İkizler Burcu");
                } else {
                    System.out.println("Boğa Burcu");
                }
                break;

            case 6:
                if(gun>=23){
                    System.out.println("Yengeç Burcu");
                } else {
                    System.out.println("İkizler Burcu");
                }
                break;

            case 7:
                if(gun>=23){
                    System.out.println("Aslan Burcu");
                } else {
                    System.out.println("Yengeç Burcu");
                }
                break;

            case 8:
                if(gun>=23){
                    System.out.println("Başak Burcu");
                } else {
                    System.out.println("Aslan Burcu");
                }
                break;

            case 9:
                if(gun>=23){
                    System.out.println("Terazi Burcu");
                } else {
                    System.out.println("Başak Burcu");
                }
                break;

            case 10:
                if(gun>=23){
                    System.out.println("Akrep Burcu");
                } else {
                    System.out.println("Terazi Burcu");
                }
                break;

            case 11:
                if(gun>=22){
                    System.out.println("Yay Burcu");
                } else {
                    System.out.println("Akrep Burcu");
                }
                break;

            case 12:
                if(gun>=22){
                    System.out.println("Oğlak Burcu");
                } else {
                    System.out.println("Yay Burcu");
                }
                break;

            default:
                System.out.println("Lütfen ay için 1-12 arasında bir sayı giriniz. Gün için takvimden yardım alın. :)");
        }


        // IF ile ÇÖZÜM
        System.out.print("\n!!! IF İLE ÇÖZÜM !!!\n");

        System.out.print("Kaçıncı ayda doğdunuz ? : ");
        ay = input.nextInt();

        System.out.print("Ayın kaçında doğdunuz ? : ");
        gun = input.nextInt();

        if (ay == 1 && gun >= 22) {
            System.out.println("Kova Burcu");
        } else if (ay == 1){
            System.out.println("Oğlak Burcu");
        }

        if (ay == 2 && gun >= 20) {
            System.out.println("Balık Burcu");
        } else if (ay == 2){
            System.out.println("Kova Burcu");
        }

        if (ay == 3 && gun >= 21) {
            System.out.println("Koç Burcu");
        } else if (ay == 3){
            System.out.println("Balık Burcu");
        }

        if (ay == 4 && gun >= 21) {
            System.out.println("Boğa Burcu");
        } else if (ay == 4){
            System.out.println("Koç Burcu");
        }

        if (ay == 5 && gun >= 22) {
            System.out.println("ikizler Burcu");
        } else if (ay == 5){
            System.out.println("Boğa Burcu");
        }

        if (ay == 6 && gun >= 23) {
            System.out.println("Yengeç Burcu");
        } else if (ay == 6){
            System.out.println("ikizler Burcu");
        }

        if (ay == 7 && gun >= 23) {
            System.out.println("Aslan Burcu");
        } else if (ay == 7){
            System.out.println("yengeç Burcu");
        }

        if (ay == 8 && gun >= 23) {
            System.out.println("Başak Burcu");
        } else if (ay == 8){
            System.out.println("Aslan Burcu");
        }

        if (ay == 9 && gun >= 23) {
            System.out.println("Terazi Burcu");
        } else if (ay == 9){
            System.out.println("Başak Burcu");
        }

        if (ay == 10 && gun >= 20) {
            System.out.println("Akrep Burcu");
        } else if (ay == 10){
            System.out.println("Terazi Burcu");
        }

        if (ay == 11 && gun >= 20) {
            System.out.println("Yay Burcu");
        } else if (ay == 11){
            System.out.println("Akrep Burcu");
        }

        if (ay == 12 && gun >= 20) {
            System.out.println("Oğlak Burcu");
        } else if (ay == 12){
            System.out.println("Yay Burcu");
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

:pushpin: Meyveler ve KG Fiyatları:

- Armut : 2,14 TL   
- Elma : 3,67 TL  
- Domates : 1,11 TL  
- Muz: 0,95 TL  
- Patlıcan : 5,00 TL  


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
  
  
## :open_book: ÖDEV 3	- Uçak Bileti Fiyatı Hesaplama

### SORU :question:
Java ile mesafeye ve şartlara göre uçak bileti fiyatı hesaplayan programı yapın. Kullanıcıdan Mesafe (KM), yaşı ve yolculuk tipi (Tek Yön, Gidiş-Dönüş) bilgilerini alın. Mesafe başına ücret 0,10 TL / km olarak alın. İlk olarak uçuşun toplam fiyatını hesaplayın ve sonrasında ki koşullara göre müşteriye aşağıdaki indirimleri uygulayın ;

:pushpin: Kullanıcıdan alınan değerler geçerli (mesafe ve yaş değerleri pozitif sayı, yolculuk tipi ise 1 veya 2) olmalıdır. Aksi takdirde kullanıcıya "Hatalı Veri Girdiniz !" şeklinde bir uyarı verilmelidir.

:pushpin: Kişi 12 yaşından küçükse bilet fiyatı üzerinden %50 indirim uygulanır.

:pushpin: Kişi 12-24 yaşları arasında ise bilet fiyatı üzerinden %10 indirim uygulanır.

:pushpin: Kişi 65 yaşından büyük ise bilet fiyatı üzerinden %30 indirim uygulanır.

:pushpin: Kişi "Yolculuk Tipini" gidiş dönüş seçmiş ise bilet fiyatı üzerinden %20 indirim uygulanır.  
  

:mag: İpucu
```
Normal Tutar = Mesafe * 0.10 = 1500 * 0.10 = 150 TL
Yaş İndirimi = Normal Tutar * Yaş İndirim Oranı = 150 * 0.10= 15 TL
İndirimli Tutar = Normal Tutar – Yaş İndirimi = 150 – 15 = 135 TL
Gidiş Dönüş Bilet İndirimi = İndirimli Tutar * 0.20 = 135 * 0.20 = 27 TL
Toplam Tutar = (135-27)* 2 = 216 TL
```
  
:heavy_check_mark: Senaryo 1
```
Mesafeyi km türünden giriniz : 1500
Yaşınızı giriniz : 20
Yolculuk tipini giriniz (1 => Tek Yön , 2 => Gidiş Dönüş ): 2

Toplam Tutar = 216 TL
```  
  
:heavy_check_mark: Senaryo 2
```
Mesafeyi km türünden giriniz : -500
Yaşınızı giriniz : 1
Yolculuk tipini giriniz (1 => Tek Yön , 2 => Gidiş Dönüş ): 77

Hatalı Veri Girdiniz !
```    

:heavy_check_mark: Senaryo 3
```
Mesafeyi km türünden giriniz : 200
Yaşınızı giriniz : 35
Yolculuk tipini giriniz (1 => Tek Yön , 2 => Gidiş Dönüş ): 1

Toplam Tutar = 20.0 TL
```  
 
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Odev3;

import java.util.Scanner;
import java.text.DecimalFormat;

public class UcakBiletiFiyati {
    public static void main(String[] args) {

        // Deişkenler tanımlandı.
        double mesafe, yas, mUcret=0.10, nTutar, yIndirimi=0, iTutar, gdbIndirimi, tTutar;
        int yolTip;

        // Kullanıcıdan değerlerin aldırılması icin scanner kullanıldı.
        // Virgüllerden sonra çıkan 0'ların silinmesi için DecimalFormat eklendi.
        Scanner input = new Scanner(System.in);
        DecimalFormat df = new DecimalFormat("#.##");

        // Kullanıcıdan KM, yaş ve gidiş döneş bilgisi istendi.
        System.out.print("Mesafeyi km türünden giriniz : ");
        mesafe = input.nextInt();

        System.out.print("Yaşınızı giriniz : ");
        yas = input.nextInt();

        System.out.print("Yolculuk tipini giriniz (1 => Tek Yön , 2 => Gidiş Dönüş ): ");
        yolTip = input.nextInt();

        // Ücret hesaplaması...
        nTutar=mesafe*mUcret;

        // İndirimlerin hesaplanması ve toplam tutara uygulanması...
        if (yas < 12) {
            yIndirimi=nTutar*0.50;
        } else if (yas >=12 && yas <= 24){
            yIndirimi=nTutar*0.10;
        } else if (yas >= 65){
            yIndirimi=nTutar*0.30;
        }

        iTutar=nTutar-yIndirimi;

        switch (yolTip) {
            case 1:
                gdbIndirimi=iTutar*0;
                tTutar=iTutar-gdbIndirimi;
                System.out.print("\nToplam Tutar = " + df.format(tTutar) +" TL");
                break;

            case 2:
                gdbIndirimi=iTutar*0.20;
                tTutar=iTutar-gdbIndirimi;
                tTutar=tTutar*2;
                System.out.print("\nToplam Tutar = " + df.format(tTutar) +" TL");
                break;

            default:
                System.out.println("\nHatalı Veri Girdiniz !");
                break;
        }
    }
}

```
</details>   

## :open_book: ÖDEV 4	- Çin Zodyağı Hesaplama

### SORU :question:
Çin Zodyağı Hesaplayan Program

Java ile kullanıcıdan doğum tarihini alıp Çin Zodyağı değerini hesaplayan program yazınız.

:mag: Çin Zodyağı nedir?   
4000 bin yıldır kullanılan bir astroloji çeşididir Çin astrolojisi ve insanları 12 değişik burç ve sembollerle tanımlar. Çin Zodyağı bu 12 burcun eşit aralıklarla(10 derece genişliğinde) sıralandığı bir hayvan halkasıdır ve yıldızlarla pek bir ilgisi yoktur.

:pushpin: Çin Zodyağı nasıl hesaplanır?
Çin zodyağı hesaplanırken kişinin doğum yılının 12 ile bölümünde kalana göre bulunur.
- Doğum Tarihi %12 = 0 ➜ Maymun   
- Doğum Tarihi %12 = 1 ➜ Horoz   
- Doğum Tarihi %12 = 2 ➜ Köpek   
- Doğum Tarihi %12 = 3 ➜ Domuz   
- Doğum Tarihi %12 = 4 ➜ Fare   
- Doğum Tarihi %12 = 5 ➜ Öküz   
- Doğum Tarihi %12 = 6 ➜ Kaplan   
- Doğum Tarihi %12 = 7 ➜ Tavşan   
- Doğum Tarihi %12 = 8 ➜ Ejderha   
- Doğum Tarihi %12 = 9 ➜ Yılan   
- Doğum Tarihi %12 = 10 ➜ At   
- Doğum Tarihi %12 = 11 ➜ Koyun   

 
:heavy_check_mark: Senaryo
```
Doğum Yılınızı Giriniz : 1990
Çin Zodyağı Burcunuz : At
```  
  
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
  
```java
package Odev4;
import java.util.Scanner;

public class CinZodyagi {
    public static void main(String[] args) {
        int dYil, kalan;
        Scanner input = new Scanner(System.in);

        System.out.print("Doğum Yılınızı Giriniz : ");
        dYil = input.nextInt();

        kalan = dYil%12;

        if (kalan==0){
            System.out.print("Çin Zodyağı Burcunuz : Maymun");
        } else if (kalan==1){
            System.out.print("Çin Zodyağı Burcunuz : Horoz");
        }else if (kalan==2){
            System.out.print("Çin Zodyağı Burcunuz : Köpek");
        }else if (kalan==3){
            System.out.print("Çin Zodyağı Burcunuz : Domuz");
        }else if (kalan==4){
            System.out.print("Çin Zodyağı Burcunuz : Fare");
        }else if (kalan==5){
            System.out.print("Çin Zodyağı Burcunuz : Öküz");
        }else if (kalan==6){
            System.out.print("Çin Zodyağı Burcunuz : Kaplan");
        }else if (kalan==7){
            System.out.print("Çin Zodyağı Burcunuz : Tavşan");
        }else if (kalan==8){
            System.out.print("Çin Zodyağı Burcunuz : Ejderha");
        }else if (kalan==9){
            System.out.print("Çin Zodyağı Burcunuz : Yılan");
        }else if (kalan==10){
            System.out.print("Çin Zodyağı Burcunuz : At");
        }else if (kalan==11){
            System.out.print("Çin Zodyağı Burcunuz : Koyun");
        }
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

