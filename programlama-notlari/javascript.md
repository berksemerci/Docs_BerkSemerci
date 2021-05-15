---
description: Bir web sitesine kazandırılan işlevselliğin diğer adı.
---

# 💎 JavaScript

## Javascirpt Tanımlama ve Dış Bağlantı

```text
<!DOCTYPE html>
<html>
      <head> 
            <meta charset="UTF-8">
            <title>Javascript Test</title>
            <script> alert("Merhaba !"); </script>
      </head> 
      <body> 
            <script> alert("Merhaba !"); </script>
      </body>
</html>
```

🔵 Javascript genellikle _**&lt;head&gt;**_ veya _**&lt;body&gt;**_ tag'ları içerisinde çalıştırılır. Her ikisine de yazılmasına gerek yoktur. Sayfanın çalıştırılma prensibi ve yükleme hızı göz önüne alınarak tercihte bulunularak yazılır. Yukarıdaki örnekte basit bir Javascript yapısı bulunmaktadır. Javascript tanımlamaları sayfa içerisinde yapılacaksa mutlaka _**&lt;script&gt;**_ ile başlamalı ve _**&lt;/script&gt;**_ ile kapatılmalıdır. Script tag içerisinde bulunun _**alert\(\);**_ ise sayfa yüklendiğinde ekrana uyarı mesajı verilmesini sağlar. 

![Yukar&#x131;da basit kodlamas&#x131; verilen ve a&#xE7;&#x131;klamas&#x131; yap&#x131;lan &#xF6;rne&#x11F;in ekran g&#xF6;r&#xFC;n&#xFC;m&#xFC;.](../.gitbook/assets/screenshot_2.png)

🔵 Eğer Javascript tagları içerisinde komplike ve birden fazla işlem yapılacaksa hem daha düzenli olması hem de ileride yapılabilecek değişikliklerde yada meydana gelecek hatalarda kod satırlarının anlaşılabilir olması için ayrı bir dosya haline getirilerek dış bağlantı şeklinde projeye eklenmesi daha sağlıklı olacaktır. Bunun için tıpkı bir _**.html**_ dosyası oluşturur gibi sonu _**.js**_ ile biten bir Javascript dosyası oluşturmamız ve _**&lt;script&gt;**_ tagları içerisindeki kod satırlarımızı buraya aktarmamız gereklidir. Daha sonrasında bu kodların index veya oluşturulan başka bir sayfada işlenebilir olması için bağlantısının _**"src"**_ ile yapılması gerekmektedir. Bu bağlantı aşağıda bulunan örnekteki gibi yapılmaktadır. 

```text
<!DOCTYPE html>
<html>
      <head> 
            <meta charset="UTF-8">
            <title>Javascript Test</title>
            <script src="BlogScript.js"></script>
      </head> 
      <body>
            ...
      </body>
</html>
```

## Javascirpt Output\(Çıktı\) İşlemleri

🔵 Javascript işlemlerinden geri dönüş sağlamak, sayfa içerisindeki herhangi bir elemente değer atamak, sayfada bildirim gerçekleştirmek ve konsol çıktıları oluşturmak için kullanılan kod yapılarını 4 başlıkta topluyoruz. Bunlar;

* **alert\(\) veya window.alert\(\)**

  🔹 Aslında ikisi de aynı işlevi görmektedir. Amacı sayfa yüklendiğinde ekrana bildirim göndermektir.

```text
alert("Sayfaya Hoşgeldiniz !!!");
window.alert("Sayfaya Hoşgeldiniz !!!");
```

* **innerHTML** 🔹 Seçili olan element veya elementlerin istenilen değeri almasını sağlar.

{% hint style="danger" %}
innerHTML yapısının kullanılabilmesi için değer verilmesi istenilen element veya elementler mutlaka seçilmelidir. Seçim işlemlerinde elementin _**id, name, class**_ veya _**tag**_ türü kullanılabilir.
{% endhint %}

{% tabs %}
{% tab title="Element by ID" %}
Değer verilmek istenilen elementin ID değerine göre atama yapan kod parçacığıdır. ID unique olması gerektiğinden tek bir ID değerine atama yapılır.

```text
document.getElementById("ID_Adi").innerHTML = "Atanacak_Deger";
```
{% endtab %}

{% tab title="Elements by Name" %}
Değer verilmek istenilen elementlerin ad değerine göre atama yapan kod parçacığıdır. Ad değeri birden fazla elementte aynı olarak kullanılabileceğinden çoğul işlemler gerçekleştirir. Aynı ad içerisindeki element kümesinde değer verilmek istenilen elementin indis değeri belirtilmelidir.

```text
document.getElementsByName("Name_Adi")[0].value = "Atanacak_Deger";
```

{% hint style="warning" %}
innerHTML eğer bir form işleminde veya input için kullanılacaksa value olarak yazılmalıdır. Çünkü bu alanlarda değer yazdırılma yapılmaz, değer atanması gerçekleştirilir.
{% endhint %}
{% endtab %}

{% tab title="Elements by Class" %}
Değer verilmek istenilen elementlerin class değerine göre atama yapan kod parçacığıdır. Class değeri birden fazla elementte aynı olarak kullanılabileceğinden çoğul işlemler gerçekleştirir. Aynı class içerisindeki element kümesinde değer verilmek istenilen elementin indis değeri belirtilmelidir.

```text
document.getElementsByClassName("Class_Adi")[0].innerHTML = "Atanacak_Deger";
```
{% endtab %}

{% tab title="Elements by Tag" %}
Değer verilmek istenilen elementlerin tag türüne göre atama yapan kod parçacığıdır. Tag değeri birden fazla elementte aynı olarak kullanılabileceğinden çoğul işlemler gerçekleştirir. Aynı tag içerisindeki element kümesinde değer verilmek istenilen elementin indis değeri belirtilmelidir.

```text
document.getElementsByTagName("Tag_Turu")[0].innerHTML = "Atanacak_Deger";
```
{% endtab %}
{% endtabs %}

* **document.write\(\)** 🔹Sayfanın boş olan herhangi bir yerinde istenilen yazının veya değerin görüntülenmesini sağlar.

```text
document.write("Sayfada Gözükecek Yazı...");
```

* **console.log\(\)** 🔹Tarayıcı kaynak görüntülemesinde bulunun konsol sekmesinde istenilen işlemlerin görüntülenmesini sağlar.

```text
console.log("Bu Bir Konsol Denemesidir !");
```

{% hint style="warning" %}
Javascript'te tıpkı diğer birçok dildeki gibi her bir kod satırı noktalı virgül ";" işareti ile ayrılır.

Açıklama satırı eklenecek ise çift eğik çizgi "//" veya yıldız-eğik çizgi "/\*......\*/" kullanılır.
{% endhint %}

![T&#xFC;m Output\(&#xC7;&#x131;kt&#x131;\) i&#x15F;lemleri tek bir &#xF6;rnekte g&#xF6;sterilmi&#x15F; h&#xE2;li.](../.gitbook/assets/javascript_output_ss.png)

{% file src="../.gitbook/assets/javascript\_output.html" caption="Javascirpt Output\(Çıktı\) İşlemleri Örneğini İndir" %}

## Javascript Variable\(Değişken\) Tanımlama

🔵 Javascript içerisinde değişken tanımlamak son derece kolaydır. Bazı dillerde olduğu gibi tanımlama yapılacak olan değişkenin türünün belirtilmesine ihtiyaç yoktur. Değişken tanımlarken ingilizce anlamı olan variable'ın kısaltılmışı _**"var"**_ kullanılır. Değişkene değer ataması yapmak için _**eşittir "="**_ operatörü kullanılır.  
  
         **`var`** `DegiskenAdi` = `AtanacakDeger;`

{% hint style="info" %}
Her değişken için tanımlama yapılırken değer atamasına gerek yoktur. Yani bazı değişkenler kullanılacaklar zamanlarda değer alabilir.  
  
**`var`** `DegiskenAdi;`
{% endhint %}

🔵 Değişkenler; **Sayı** _**"int"**,_ **Ondalıklı Sayı** _**"double"**,_ **Metinsel** _**"string"** ve_ **Mantıksal "**_**boolean"**_ olarak tanımlanabilir.

```text
var sayi1 = 10;    //int
var sayi2 = 2.5;   //double
var metin = "Blog";    //string
var durum = false;    //boolean
```

{% hint style="warning" %}
Eğer bir değişkene yapılan atamanın hangi türde yapıldığı bilinmiyor veya hatırlanmıyorsa yada değişken türü değişimlerinde kontroller yapılacaksa, _**typeof\(degisken\)**_ kod parçacığı ile tür bilgisi öğrenilebilir.

document.write\(_**typeof\(deger1\)**_\);  
// Sayfa içerisindeki herhangi bir yere "deger1" adlı değişkenimizin türünü yazdırır.
{% endhint %}

![T&#xFC;m Variable\(De&#x11F;i&#x15F;ken\) i&#x15F;lemlerinin tek bir &#xF6;rnekte g&#xF6;sterilmi&#x15F; h&#xE2;li.](../.gitbook/assets/javascript_variable_ss.png)

{% file src="../.gitbook/assets/javascript\_variable.html" caption="Javascript Variable\(Değişken\) Örneğini İndir" %}

## Javascript Operatörleri

🔵 Operatörler Matematiksel, Atama, Metinsel, Karşılaştırma, Mantıksal ve Koşul olmak üzere altı gruba ayrılırlar.

* **Matematiksel Operatörler** 🔹Toplama, Çıkarma, Bölme, Çarpma, Mod, Arttırma ve Azaltma işlemleri bu operatörler aracılığıyla yapılır.

```text
var Sonuc;

Sonuc = 6+4;    //Toplama Operatörü
Sonuc = 6-4;    //Çıkarma Operatörü
Sonuc = 3*2;    //ÇarpmaOperatörü
Sonuc = 8/4;    //Bölme Operatörü
Sonuc = 4%2;    //Mod Alma Operatörü

Sonuc = ++Sayi;    //Bu Operatör Sayi değişkenini önce 1 arttırır sonra Sonuc değişkenine atar 
Sonuc = Sayi++;    //Bu Operatör Sayi değişkenini önce Sonuc değişkenine atar sonra 1 artırır
Sonuc = --Sayi;    //Bu Operatör Sayi değişkenini önce 1 azaltır sonra Sonuc değişkenine atar
Sonuc = Sayi--;    //Bu Operatör Sayi değişkenini önce Sonuc değişkenine atar sonra 1 azaltır
```

* **Atama Operatörleri** 🔹Doğrudan Atayarak, Toplayarak Çıkararak, Bölerek, Çarparak ve Mod alarak değer atama işlemleri bu operatörler aracılığıyla yapılır.

```text
var Sayi;

Sayi = 0;    //Doğrudan Atama
Sayi += 5;    //Toplayarak Atama (Sayi = Sayi + 5) işleminin kısa gösterimidir
Sayi -= 5;    //Çıkararak Atama (Sayi = Sayi - 5) işleminin kısa gösterimidir
Sayi *= 5;    //Çarparak Atama (Sayi = Sayi * 5) işleminin kısa gösterimidir
Sayi /= 5;    //Bölerek Atama (Sayi = Sayi / 5) işleminin kısa gösterimidir
Sayi %= 5;    //Mod Alarak Atama (Sayi = Sayi % 5) işleminin kısa gösterimidir
```

* **Metinsel Operatör** 🔹Birden fazla metinsel değişkenin birleştirilmesinde kullanılır. Toplama işleminde olduğu gibi buradaki operatör _**artı "+"**_ birleştirme işlevi görür.

```text
var Metin1 = "Blog";
var Metin2 = "JavaScript";
var BirlesikMetin;

BirlesikMetin = Metin1 + Metin2;    //Metinleri Boşluksuz Birleştirir
// Çıktısı = BlogJavaScript

BirlesikMetin = Metin1 + " " + Metin2;    //Eğer birleştirme işleminde boşluk isteniyorsa
// Çıktısı = Blog JavaScript
```

* **Karşılaştırma Operatörleri** 🔹Değişkenler arasında Eşitlik, Denklik, Büyüklük ve Küçüklük gibi karşılaştırma işlemleri bu operatörler aracılığıyla yapılır.

```text
var Sayi1 = 3;
var Sayi2 = 7;
var Comp;    //Karşılaştırmalarda true/false değeri alacaktır

Comp = Sayi1 == Sayi2;    //Sayi1, Sayi2'ye Eşit Midir ? -> False
Comp = Sayi1 === Sayi2;    //Sayi1, Sayi2'ye Denk (Tür ve Değeri Aynı) Midir ? -> False
Comp = Sayi1 != Sayi2;    //Sayi1, Sayi2'ye Eşit Değil Midir ? -> True
Comp = Sayi1 > Sayi2;    //Sayi1, Sayi2'den Büyük Müdür ? -> False
Comp = Sayi1 < Sayi2;    //Sayi1, Sayi2'den Küçük Müdür ? -> True
Comp = Sayi1 >= Sayi2;    //Sayi1, Sayi2'ye Büyük Eşit Midir ? -> False
Comp = Sayi1 <= Sayi2;    //Sayi1, Sayi2'ye Küçük Eşit Midir ? -> False
```

* **Mantıksal Operatörler** 🔹Ve, Veya ile Değili karşılaştırmaları bu operatörler aracılığıyla yapılır.

```text
var Deger1 = true;
var Deger2 = false;
var Comp;    //Karşılaştırmalarda true/false değeri alacaktır

Comp = Deger1 && Deger2;    //Ve Operatörü. Her İki değerin aynı olmasında true değerini döndürür -> False
Comp = Deger1 || Deger2;    //Veya Operatörü. Değerlerden herhangi birisinin true olmasında true değerini döndürür -> True
Comp = !Deger1 ;    //Değili Operatörü. Değerin karşıtını döndürür -> False
```

* **Koşul Operatörü** 🔹Atanan değere göre True veya False değerinin tutulmasını sağlar.

```text
var Deger = true;
var Comp;

Comp = Deger ? "Deger true" : "Deger false";
//Deger değişkeni true ise Comp değişkeni Deger true, false ise Comp değişkeni Deger false değerini alır
```

{% file src="../.gitbook/assets/javascript\_operator.html" caption=" Javascript Operatörleri Örneğini İndir" %}

## Javascript Function\(Fonksiyon\) Kullanımı

