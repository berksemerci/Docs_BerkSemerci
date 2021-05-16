---
description: Bir web sitesine kazandırılan işlevselliğin diğer adı.
---

# 💎 JavaScript

## ↘ Javascirpt Tanımlama ve Dış Bağlantı

```markup
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

### 🔵 Javascript'in Yapısı

➖ Javascript genellikle _**&lt;head&gt;**_ veya _**&lt;body&gt;**_ tag'ları içerisinde çalıştırılır. Her ikisine de yazılmasına gerek yoktur. Sayfanın çalıştırılma prensibi ve yükleme hızı göz önüne alınarak tercihte bulunularak yazılır. Yukarıdaki örnekte basit bir Javascript yapısı bulunmaktadır. Javascript tanımlamaları sayfa içerisinde yapılacaksa mutlaka _**&lt;script&gt;**_ ile başlamalı ve _**&lt;/script&gt;**_ ile kapatılmalıdır. Script tagları içerisinde bulunun _**alert\(\);**_ ise sayfa yüklendiğinde ekrana uyarı mesajı verilmesini sağlar. \(Daha sonraki aşamalarda detaylı bir şekilde bulunmaktadır.\)

![Yukar&#x131;da basit kodlamas&#x131; verilen ve a&#xE7;&#x131;klamas&#x131; yap&#x131;lan &#xF6;rne&#x11F;in ekran g&#xF6;r&#xFC;n&#xFC;m&#xFC;.](../.gitbook/assets/screenshot_2.png)

### 🔵 Javascript Dış Bağlantı

➖ Eğer Javascript tagları içerisinde komplike ve birden fazla işlem yapılacaksa hem daha düzenli olması hem de ileride yapılabilecek değişikliklerde yada meydana gelecek hatalarda kod satırlarının anlaşılabilir olması için ayrı bir dosya haline getirilerek dış bağlantı şeklinde projeye eklenmesi daha sağlıklı olacaktır. Bunun için tıpkı bir _**.html**_ dosyası oluşturur gibi sonu _**.js**_ ile biten bir Javascript dosyası oluşturulması ve _**&lt;script&gt;**_ tagları içerisindeki kod satırlarının buraya yazılması gereklidir. Daha sonrasında bu kodların index veya oluşturulan başka bir sayfada işlenebilir olması için bağlantı yolu kısaltması olan _**"src"**_ ile dosya yolunun eklenmesi gerekmektedir. Bu bağlantı aşağıda bulunan örnekteki gibi yapılmaktadır. 

```markup
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

## ↘ Javascirpt Output \(Çıktı\) İşlemleri

➖ Javascript işlemlerinden geri dönüş sağlamak, sayfa içerisindeki herhangi bir elemente değer atamak, sayfada bildirim gerçekleştirmek ve konsol çıktıları oluşturmak için kullanılan kod yapılarını 4 başlıkta toplanır.

### \*\*\*\*🔵 **alert\(\) veya window.alert\(\)**

➖ Aslında ikisi de aynı işlevi görmektedir. Amacı sayfa yüklendiğinde ekrana bildirim göndermektir.

```javascript
alert("Sayfaya Hoşgeldiniz !!!");
window.alert("Sayfaya Hoşgeldiniz !!!");
```

### \*\*\*\*🔵 **innerHTML ve Value**

➖ Seçili olan element veya elementlerin istenilen değeri almasını sağlar.

{% hint style="danger" %}
innerHTML yapısının kullanılabilmesi için değer verilmesi istenilen element veya elementler mutlaka seçilmelidir. Seçim işlemlerinde elementin _**id, name, class**_ veya _**tag**_ türü kullanılabilir.
{% endhint %}

{% tabs %}
{% tab title="Element by ID" %}
Değer verilmek istenilen elementin ID değerine göre atama yapan kod parçacığıdır. ID unique olması gerektiğinden tek bir ID değerine atama yapılır.

```javascript
document.getElementById("ID_Adi").innerHTML = "Atanacak_Deger";
```
{% endtab %}

{% tab title="Elements by Name" %}
Değer verilmek istenilen elementlerin ad değerine göre atama yapan kod parçacığıdır. Ad değeri birden fazla elementte aynı olarak kullanılabileceğinden çoğul işlemler gerçekleştirir. Aynı ad içerisindeki element kümesinde değer verilmek istenilen elementin indis değeri belirtilmelidir.

```javascript
document.getElementsByName("Name_Adi")[0].value = "Atanacak_Deger";
```

{% hint style="warning" %}
innerHTML eğer bir form işleminde veya input için kullanılacaksa value olarak yazılmalıdır. Çünkü bu alanlarda değer yazdırılma yapılmaz, değer atanması gerçekleştirilir.
{% endhint %}
{% endtab %}

{% tab title="Elements by Class" %}
Değer verilmek istenilen elementlerin class değerine göre atama yapan kod parçacığıdır. Class değeri birden fazla elementte aynı olarak kullanılabileceğinden çoğul işlemler gerçekleştirir. Aynı class içerisindeki element kümesinde değer verilmek istenilen elementin indis değeri belirtilmelidir.

```javascript
document.getElementsByClassName("Class_Adi")[0].innerHTML = "Atanacak_Deger";
```
{% endtab %}

{% tab title="Elements by Tag" %}
Değer verilmek istenilen elementlerin tag türüne göre atama yapan kod parçacığıdır. Tag değeri birden fazla elementte aynı olarak kullanılabileceğinden çoğul işlemler gerçekleştirir. Aynı tag içerisindeki element kümesinde değer verilmek istenilen elementin indis değeri belirtilmelidir.

```javascript
document.getElementsByTagName("Tag_Turu")[0].innerHTML = "Atanacak_Deger";
```
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
Programlama dillerinde indis değerleri sıfırdan başlar.
{% endhint %}

### \*\*\*\*🔵 **document.write\(\)**

➖ Sayfanın boş olan herhangi bir yerinde istenilen yazının veya değerin görüntülenmesini sağlar.

```javascript
document.write("Sayfada Gözükecek Yazı...");
```

### \*\*\*\*🔵 **console.log\(\)**

➖ Tarayıcı kaynak görüntülemesinde bulunun konsol sekmesinde istenilen işlemlerin görüntülenmesini sağlar.

```javascript
console.log("Bu Bir Konsol Denemesidir !");
```

{% hint style="warning" %}
Javascript'te tıpkı diğer birçok dildeki gibi her bir kod satırı _**noktalı virgül ";"**_ işareti ile ayrılır.

Açıklama satırı eklenecek ise çift _**eğik çizgi "//"**_ veya _**yıldız-eğik çizgi "/\*......\*/"**_ kullanılır.
{% endhint %}

![T&#xFC;m Output\(&#xC7;&#x131;kt&#x131;\) i&#x15F;lemleri tek bir &#xF6;rnekte g&#xF6;sterilmi&#x15F; h&#xE2;li.](../.gitbook/assets/javascript_output_ss.png)

{% file src="../.gitbook/assets/javascript\_output.html" caption="Javascirpt Output\(Çıktı\) İşlemleri Örneğini İndir" %}

## ↘ Javascript Variables \(Değişkenler\) Tanımlama

➖ Javascript içerisinde değişken tanımlamak son derece kolaydır. Bazı dillerde olduğu gibi tanımlama yapılacak olan değişkenin türünün belirtilmesine ihtiyaç yoktur. Değişken tanımlarken genellikle kullanışlı olması sebebiyle ingilizce anlamı olan variable'ın kısaltılmışı _**"var"**_ kullanılır. Bunun haricinde _**"const"**_ ve _**"let"**_ de kullanılabilir. Değişkene değer ataması yapmak için _**eşittir "="**_ operatörü kullanılır. \(Operatörlerle ilgili detaylı bilgi yazının devamında bulunmaktadır.\)

### 🔵 Var, Const ve Let ve Özellikleri

{% hint style="warning" %}
**var** = Tanımlı olduğu her yerden erişilebilir değişken türüdür. Oluşturulan değişken farklı fonksiyonlar içerisinde farklı değerler alabilir. En son atanan değer yapılan son işlemde geçerlidir.

**const =** Sabit değerli değişkenler atanmasını sağlar. Yani atanan değer kullanılacak olan tüm hesaplama ve fonksiyonlarda geçerlidir.

**let =** Sadece tanımlı olduğu süslü parantez "{}" içerisinden erişilebilir. Yeni değer ataması yapılabilir. Var'a göre daha kısıtlayıcı, const'a göre daha kapsamlı kullanıma sahiptir.
{% endhint %}

             **`var`** `DegiskenAdi` = `AtanacakDeger;`

{% hint style="info" %}
Her değişken için tanımlama yapılırken değer atamasına gerek yoktur. Bazı değişkenler kullanılacaklar zamanlarda değer alabilir. Değer ataması yapılmamış değişken _**"undefined"**_ veya _**"null"**_ değer alır.  
  
**`var`** `DegiskenAdi;`
{% endhint %}

➖ Değişkenler temelde; **Sayı** _**"int"**,_ **Ondalıklı Sayı** _**"double"**,_ **Metinsel** _**"string"** ve_ **Mantıksal "**_**boolean"**_ olarak tanımlanır.

```javascript
var sayi1 = 10;    //int
var sayi2 = 2.5;   //double
var metin = "Blog";    //string
var durum = false;    //boolean
```

### 🔵 typeof\(\) Kullanımı

{% hint style="warning" %}
Eğer bir değişkene yapılan atamanın hangi türde yapıldığı bilinmiyor veya hatırlanmıyorsa yada değişken türü değişimlerinde kontroller yapılacaksa, _**typeof\(degisken\)**_ kod parçacığı ile tür bilgisi öğrenilir.

document.write\(_**typeof\(deger1\)**_\);  
// Sayfa içerisindeki herhangi bir yere "deger1" adlı değişkenin türünü yazdırır.
{% endhint %}

![T&#xFC;m Variable\(De&#x11F;i&#x15F;ken\) i&#x15F;lemlerinin tek bir &#xF6;rnekte g&#xF6;sterilmi&#x15F; h&#xE2;li.](../.gitbook/assets/javascript_variable_ss.png)

{% file src="../.gitbook/assets/javascript\_variable.html" caption="Javascript Variable\(Değişken\) Örneğini İndir" %}

## ↘ Javascript Operatörleri

➖ Operatörler Matematiksel, Atama, Metinsel, Karşılaştırma, Mantıksal ve Koşul olmak üzere altı gruba ayrılırlar.

### \*\*\*\*🔵 **Matematiksel Operatörler**

➖ ****Toplama, Çıkarma, Bölme, Çarpma, Mod, Arttırma ve Azaltma işlemleri bu operatörler aracılığıyla yapılır.

```javascript
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

### \*\*\*\*🔵 **Atama Operatörleri**

➖ ****Doğrudan Atayarak, Toplayarak Çıkararak, Bölerek, Çarparak ve Mod alarak değer atama işlemleri bu operatörler aracılığıyla yapılır.

```javascript
var Sayi;

Sayi = 0;    //Doğrudan Atama
Sayi += 5;    //Toplayarak Atama (Sayi = Sayi + 5) işleminin kısa gösterimidir
Sayi -= 5;    //Çıkararak Atama (Sayi = Sayi - 5) işleminin kısa gösterimidir
Sayi *= 5;    //Çarparak Atama (Sayi = Sayi * 5) işleminin kısa gösterimidir
Sayi /= 5;    //Bölerek Atama (Sayi = Sayi / 5) işleminin kısa gösterimidir
Sayi %= 5;    //Mod Alarak Atama (Sayi = Sayi % 5) işleminin kısa gösterimidir
```

### \*\*\*\*🔵 **Metinsel Operatör**

➖ ****Birden fazla metinsel değişkenin birleştirilmesinde kullanılır. Toplama işleminde olduğu gibi buradaki operatör _**artı "+"**_ birleştirme işlevi görür.

```javascript
var Metin1 = "Blog";
var Metin2 = "JavaScript";
var BirlesikMetin;

BirlesikMetin = Metin1 + Metin2;    //Metinleri Boşluksuz Birleştirir
// Çıktısı = BlogJavaScript

BirlesikMetin = Metin1 + " " + Metin2;    //Eğer birleştirme işleminde boşluk isteniyorsa
// Çıktısı = Blog JavaScript
```

### \*\*\*\*🔵 **Karşılaştırma Operatörleri** 

\*\*\*\*➖ Değişkenler arasında Eşitlik, Denklik, Büyüklük ve Küçüklük gibi karşılaştırma işlemleri bu operatörler aracılığıyla yapılır.

```javascript
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

### \*\*\*\*🔵 **Mantıksal Operatörler** 

\*\*\*\*➖ ****Ve, Veya ile Değili karşılaştırmaları bu operatörler aracılığıyla yapılır.

```javascript
var Deger1 = true;
var Deger2 = false;
var Comp;    //Karşılaştırmalarda true/false değeri alacaktır

Comp = Deger1 && Deger2;    //Ve Operatörü. Her İki değerin aynı olmasında true değerini döndürür -> False
Comp = Deger1 || Deger2;    //Veya Operatörü. Değerlerden herhangi birisinin true olmasında true değerini döndürür -> True
Comp = !Deger1 ;    //Değili Operatörü. Değerin karşıtını döndürür -> False
```

### \*\*\*\*🔵 **Koşul Operatörü**

 ****➖ Atanan değere göre True veya False değerinin tutulmasını sağlar.

```javascript
var Deger = true;
var Comp;

Comp = Deger ? "Deger true" : "Deger false";
//Deger değişkeni true ise Comp değişkeni Deger true, false ise Comp değişkeni Deger false değerini alır
```

{% file src="../.gitbook/assets/javascript\_operator.html" caption=" Javascript Operatörleri Örneğini İndir" %}

## ↘ Javascript Function \(Fonksiyon\) Kullanımı

➖ Javascript'te Function\(Fonksiyon\) tekrar eden veya sık kullanılan işlemlerin tek bir yerden kontrol edilmesini sağlar. Oluşturulan fonksiyon için önce işlem yapılacak kod bloğu içerisinde çağrılarak değer gönderilir. Sonra Function\(Fonksiyon\) içerisinden de yapılan işlemlerin sonucu geri döndürülür. Örnek vermek gerekirse, bir mağazada satılan bir ürünün ücret ödemesiyle ilgili hesaplama yapılacak olsun. Bu ürüne ödenen ücretten, ürün ücreti çıkarılarak geri ödenecek ücretin hesaplanması gereksin. O halde aşağıdaki şekilde tanımlamaların yapılması ve işlemleri gerçekleştirilmesi gerekecektir.

```javascript
var UrunUcreti = 250;
var OdenenUcret = 325;
var GeriOdeme;
GeriOdeme = OdenenUcret - UrunUcreti;
```

➖ Fakat bu üründen bir tane değil de yirmi adet sipariş edilmiş olursa ne olur ? Yukarıda yazılmış olan kod satırlarının yirmi defa yazılması gerekir. Yirmi işlem için dört satır kod yazıldığında aslında seksen satırlık kod oluşturulmuş olur. Bu işlem yorumlayıcı için oldukça yüklü ve gereksiz bir süreç haline gelir. Üstelik ürün fiyatında değişiklik olması durumunda bu seksen satırı tekrar gözden geçirmek gerekir. Daha kötüsü değişken adında değişiklik olması durumunda işin içinden çıkılamayacak bir hal alması bile söz konusu olabilir. İşte tam da bu ve bunun gibi sebeplerden dolayı Function\(Fonksiyon\) kullanılır.

### 🔵Function \(Fonksiyon\) Yapısı

```javascript
function Mesaj(){
    document.write("Bu Bir Fonksiyon Mesajıdır");
}

Mesaj();
```

➖ Burada yapılmış oldan işlemle öncelikle _**"Mesaj"**_ adında bir Function\(Fonksiyon\) oluşturulmuştur. İçerisinde _**"document.write\(\)"**_ komutu ile bir yazı eklenmiştir. Ve beşinci satırda _**"Mesaj\(\)"**_ fonksiyonu çağırarak içerisindeki komutun ekrana yazılması sağlanmıştır. Fakat burada sabit bir komutun ekrana yazılmasını görüyoruz. Peki yukarıdaki örnekteki gibi geri ödenecek ücret hesaplaması bu şekilde nasıl yapılabilir ? Bunun için Function\(Fonksiyon\)'a parametre tanımlaması ve bu parametreye fonksiyon çağrılırken değer gönderilmesi gerekir. Bu işlemi ise şöyle yapılır;

```javascript
function Hesaplama(OdenenUcret){
    var UrunUcreti = 250;
    var GeriOdeme;
    GeriOdeme = OdenenUcret - UrunUcreti;
    document.write(GeriOdeme);
}

var GonderilenUcret = 325;
Hesaplama(GonderilenUcret);

//Çıktısı : 75
```

_\*\*\*\*_➖ _**"Hesaplama"**_ adında bir fonksiyon oluşturulmuş ve bu fonksiyon içerisinde tekrar edecek işlemler sabitlenmiştir. _**"UrunUcreti"**_ ve _**"GeriOdeme"**_ değişkenleri tanımlanarak, geri ödenecek ücretin hesaplanması için gerekli matematiksel operatörü kullanımıyla hesaplama işlemi gerçekleştirilmiştir. Hesaplama işleminde çıkan sonuç ekrana yazdırılmıştır. Peki hesaplama yapılırken fonksiyon _**"OdenenUcreti"**_ nasıl alıyor ? Bunun cevabı dokuzuncu satırdaki kodda gizlidir. Bu satırda fonksiyonun _**parantez "\(\)"**_ ****işaretleri içerisinde tanımlı _**"OdenenUcret"**_ parametresine sekizinci satırda tanımlanmış _**"GonderilenUcret"**_ değişkenin değeri gönderilmiştir. Fonksiyon, parametresine gelen değeri işlemin gerçekleştirilmesi istenilen dördüncü satırda kullanarak sonucu ekrana yazdırmıştır.

{% hint style="warning" %}
Function\(Fonksiyon\)'a gönderilecek değer _**parantez "\(\)"**_ içerisinde parametre olarak gönderilir. Parantez içerisinde birden fazla parametre gönderilebilir. Gönderilecek parametreler birden fazla ise _**virgül ","**_  işareti ile ayrılır.
{% endhint %}

```javascript
function Hesaplama(OdenenUcret, Siparisci){
    var UrunUcreti = 250;
    var GeriOdeme;
    GeriOdeme = OdenenUcret - UrunUcreti;
    document.write(Siparisci + " Kişisine " + GeriOdeme + " TL Ödeme Yapılacak !");
}

var GonderilenUcret = 325;
var AdSoyad = "Elif USLU";
Hesaplama(GonderilenUcret, AdSoyad);

//Çıktısı : Elif USLU Kişisine 75 TL Ödeme Yapılacak !
```

➖ Yukarıdaki örnekte hem ücret hem de ücreti ödeyen kişinin ad soyad bilgisini içeren değişkenlerin değerlerini iki ayrı parametre ile fonksiyona gönderimi gösterilmiştir. Fonksiyon parametrelerine gelen değerleri ilgili işlem satırında kullanarak ekrana sonucu yazdırmıştır. Peki fonksiyonun içerisindeki değeri her zaman ekrana yazdırmak tercih edilmez veya sonuç değişkeni başka bir işlemde yada fonksiyonda kullanılmak istenirse ne yapılması gerekir ? Bu seferde fonksiyon çağırma işleminin aslında tersini yapılması yani değer döndürülmesi gerekir. Fonksiyon içerisinde değer döndürmek için ise _**"return"**_ kullanılır.

### 🔵 return Kullanımı

```javascript
function Hesaplama(OdenenUcret, Siparisci){
    var UrunUcreti = 250;
    var GeriOdeme;
    GeriOdeme = OdenenUcret - UrunUcreti;
    return(Siparisci + " Kişisine " + GeriOdeme + " TL Ödeme Yapılacak !");
}

var GonderilenUcret = 325;
var AdSoyad = "Elif USLU";
document.write(Hesaplama(GonderilenUcret, AdSoyad)); 

//Çıktısı : Elif USLU Kişisine 75 TL Ödeme Yapılacak !
```

_\*\*\*\*_➖ _**"return"**_ eklenerek sonuç değeri onuncu satırda fonksiyonu çağırmak için kullanılan satıra geri döndürülür ve ekrana yazdırılır. Eğer sonuç değeri doğrudan ekrana yazdırılmak istenmezse _**"document.write\(\)"**_ yerine bir değişken tanımlaması yapılarak sonuç değerinin oluşturulan bu yeni değişkene ataması yapılır.

```javascript
 var SonucDeger = Hesaplama(GonderilenUcret, AdSoyad); 
```

{% file src="../.gitbook/assets/javascript\_function.html" caption="Javascript Function\(Fonksiyon\) Örneğini İndir" %}

## ↘ Javascript Object \(Objeler\) Kullanımı

➖ Javascript'te bir nesne veya kişilik ile ilgili tanımlamalar yapılacaksa Object\(Objeler\) kullanılır. Çünkü Object\(Objeler\) kullanımı diziye benze _**Array**_ türünde olduğundan içerisinde birden fazla özellik tanımlaması yapılabilir. Yapılan bu tanımlamalar obje içerisinde veya dışında fonksiyonlar oluşturularak çağrılabilir ve kullanılabilir. Object\(Objeler\) içerisinde özellik tanımlamaları yapılırken _**süslü parantez "{}"**_ açılır, her bir tanımlamadan sonra _**virgül ","**_ konulur. 

### 🔵 Object \(Objeler\) Yapısı

```javascript
var Araba = {
    Markasi : "Honda",
    Modeli : "Civic",
    Motoru : "1.6",
    Yili : 2000,
    Rengi : "Gri"    
}

console.log(Araba);
```

![Yukar&#x131;da bulunan kod sat&#x131;rlar&#x131;n&#x131;n console ekran&#x131;nda g&#xF6;r&#xFC;n&#xFC;m&#xFC;.](../.gitbook/assets/javascript_object_consolelog1.png)

➖ Eğer _**"Araba"**_ objesinde tanımlanmış olan özelliklerden seçim yapmazsak yukarıdaki console çıktısında olduğu gibi eklenmiş olan tüm özellikler bir _**Array**_ olarak listelenmiş şekilde görülür. Sadece arabanın _**"Markası"**_ bilgisini console yazdırılması isteniyorsa;

```javascript
console.log(Araba.Markasi);    //Araba objesinin sadece Markasi özelliğini yazıdırır
```

### 🔵 Objelerde Fonksiyon Yapısı

➖ Object\(Objeler\) içerisinde fonksiyon tanımlayarak bazı işlemler gerçekleştirilebilir. Fonksiyon tanımlaması Object\(Objeler\) içerisinde şu şekilde gerçekleştirilir;

```javascript
var Araba = {
    Markasi : "Honda",
    Modeli : "Civic",
    Motoru : "1.6",
    Yili : 2000,
    Rengi : "Gri",
    Calistir : function(){
        alert("Motor Çalıştırıldı !");
    }    
}

console.log(Araba.Markasi);
Araba.Calistir();
```

➖ Yukarıdaki örnekte _**"Calistir"**_ adından bir fonksiyon oluşturulmuş ve bu fonksiyon objenin dışından çağrılmıştır. Aynı şekilde Objenin içerisinde oluşturulan yeni bir fonksiyonla obje içerisinde yeni bir işlem yapılabilir.

```javascript
var Araba = {
    Markasi : "Honda",
    Modeli : "Civic",
    Motoru : "1.6",
    Yili : 2000,
    Rengi : "Gri",
    Calistir : function(){
        alert("Motor Çalıştırıldı !");
    },    
    Bilgiler: function(){
        console.log("Markası : " + Araba.Markasi);
        console.log("Modeli: " + Araba.Modeli);
        console.log("Motoru: " + this.Motoru );
        console.log("Yili: " + this.Yili );
        console.log("Rengi: " + this.Rengi );
    }  
}

console.log(Araba.Markasi);
Araba.Calistir();
Araba.Bilgiler();
```

![Yukar&#x131;da bulunan kod sat&#x131;rlar&#x131;n&#x131;n console ekran&#x131;nda g&#xF6;r&#xFC;n&#xFC;m&#xFC;.](../.gitbook/assets/javascript_object_consolelog2.png)

➖ Örnekte _**"Bilgiler"**_ adında başka bir fonksiyon oluşturularak, fonksiyon içerisindeki _**"Araba"**_ objesine ait özellikler console ekranına yazdırılmıştır. Bazı özellikler yazdırılırken _**"this"**_  kullanılmıştır. _**"Araba.Markasi"**_ ile _**"this.Markasi"**_ kullanımı arasındaki temel fark _**"this"**_ kullanıldığında oluşturulan objeyi doğrudan ifade ettiğinden sadece o obje içerisinde bulunan bir özelliğin değerinin alınabilmesine olanak sağlamasıdır. Yani _**"Araba.Markasi"**_ kullanımında _**"Araba"**_ yerine başka bir obje yazabilir, dışarıdan bir objenin özellikleri de çekilebilir. Ama _**"this"**_ kullanılıyorsa yalnızca _**Araba"**_ objesinin _**süslü parantez "{}"**_ içerisindeki özelliklerinden değer çekilebilir.

```javascript
var Araba = {
    Markasi : "Honda",
    Modeli : "Civic",
    Motoru : "1.6",
    Yili : 2000,
    Rengi : "Gri",
    Bilgiler: function(){
        console.log("Markası : " + this.Markasi);
        console.log("Kullanan: " + Kullanici.Adi); //Kullanici objesinin özelliği
    }  
}
var Kullanici = {
    Adi : "Berk"
}

Araba.Bilgiler();
```

![Obje ad&#x131; ve this kullan&#x131;m&#x131;n&#x131;n fark&#x131;n&#x131; anlatan yukar&#x131;daki kod sat&#x131;rlar&#x131;n&#x131;n console g&#xF6;r&#xFC;m&#xFC;.](../.gitbook/assets/javascript_object_consolelog3.png)

​​ ➖ Obje içerisindeki fonksiyon işlemleri ile daha önceki örneklerde bulunan fonksiyon işlemleri arasında hiçbir fark yoktur. Orada yapılmış olan tüm işlemler burada da gerçekleştirilebilir.

```javascript
var Araba = {
    Markasi : "Honda",
    Modeli : "Civic",
    Yili : 2000,
    Bilgiler: function(){
        console.log("Markası : " + this.Markasi);
        console.log("Modeli: " + this.Modeli);
        console.log("Kullanan: " + Kullanici.Adi);
    },
    YasHesapla : function(){
        return (2021 - this.Yili);
    }
}
var Kullanici = {
    Adi : "Berk"
}

Araba.Bilgiler();
console.log(Araba.YasHesapla());
```

![Yukar&#x131;da bulunan kod sat&#x131;rlar&#x131;n&#x131;n console ekran&#x131;nda g&#xF6;r&#xFC;n&#xFC;m&#xFC;.](../.gitbook/assets/javascript_object_consolelog4.png)

➖ Örnekte yeni bir fonksiyon ve matematiksel operatör kullanılarak _**"Araba"**_ objesi içerisinde oluşturulan _**"Yili"**_ özelliğindeki değer alınarak arabanın yaşı hesaplanmıştır. Çıkan sonuç ise _**"return"**_ edilerek console ekranına yazdırılmıştır.

{% file src="../.gitbook/assets/javascript\_object.html" caption="Javascript Object \(Objeler\) Örneğini İndir" %}

## ↘ Javascript Events \(Olaylar\) Kullanımı

➖ Javascript ile sayfa içerinde gerçekleştirilen olaylara göre bazı reaksiyonlar alınabilir. Yani bir input içerisine yazı yazıldığında yada butonun üzerinde geldiğinde şu olsun veya bu olsun şeklinde bir takım olay bazlı reaksiyonlar gerçekleştirilebilir. Bu olaylar Mouse, Klavye, Form ve Pencere olayları olmak üzere dört gruba ayrılarak incelenir.

### \*\*\*\*🔵 **Mouse Events \(Olayları\)**

* onclick
* onmouseover
* onmouseout
* onmousedown
* onmouseup
* onmousemove

```javascript
<button onclick="Fonksiyon_1()">Click me</button>
//Butona tıklanınca Fonksiyon_1 çalıştır

<input onmouseover="Fonksiyon_2()" onmouseout="Fonksiyon_3()">
//Input üstüne mouse ile gelince Fonksiyon_2, üstünden mouse çekince Fonksiyon_2 çalıştır

<p onmousedown="Fonksiyon_4()" onmouseup="Fonksiyon_5()">
//Paragrafın üstüne basılı tuttuğunda Fonksiyon_4, basmayı bıraktığında Fonksiyon_5 çalıştır

<img onmousemove="Fonksiyon_6()" src="">
//Resim üzerinde mouse hareket ettiği sürece Fonksiyon_5 çalıştır
```

{% file src="../.gitbook/assets/javascript\_events\_mouse.html" caption="Javascript Events \(Olaylar\) Mouse Örneğini İndir" %}

### \*\*\*\*🔵 **Keyboard Events \(Olayları\)**

* onkeydown
* onkeyup

```javascript
<input id="bas" onkeydown="Fonksiyon_1()">
//Input seçiliyken klavyeden tuşa basıldığında Fonksiyon_1 çalıştır

<input id="birak" onkeydown="Fonksiyon_2()">
//Input seçiliyken tuş bırakıldığında Fonksiyon_2 çalıştır
```

{% file src="../.gitbook/assets/javascript\_events\_keyboard.html" caption="Javascript Events \(Olaylar\) Keyboard Örneğini İndir" %}

### \*\*\*\*🔵 **Form Events \(Olayları\)**

* onsubmit
* onfocus
* onblur
* onchange

```javascript
<form action="" onsubmit="Fonksiyon_1()">
//Form gönderildiğinde Fonksiyon_1 çalıştır

      Bir Şeyler Yaz :<input onfocus="Fonksiyon_2()" onblur="Fonksiyon_3()"type="text">
      //Input üzerinde çalışldığında Fonksiyon_2, başka bir işleme geçildiğinde Fonskiyon_3 çalıştır
      
      <select id="Secim" onchange="Fonksiyon_4()">
      //Seçim işlemlerinde değişim olduğunda Fonskiyon_4 çalıştır
      
            <option value="Audi">Audi</option>
            <option value="BMW">BMW</option>
            <option value="Mercedes">Mercedes</option>
            <option value="Volvo">Volvo</option>
      </select>
      <p>Şuan Bir Şey Seçilmedi !!!</p>
      <input type="submit" value="Submit">
</form>
```

{% file src="../.gitbook/assets/javascript\_events\_form.html" caption="Javascript Events \(Olaylar\) Form Örneğini İndir" %}

### \*\*\*\*🔵 **Window/Document Events \(Olayları\)**

* onload
* onunload
* onresize

```javascript
<!DOCTYPE html>
<html>
  <body onload="Fonksiyon_1()" onunload="Fonksiyon_2()" onresize="Fonksiyon_3()">
  //Sayfa yüklendiğinde Fonksiyon_1, kapatılırken Fonksiyon_2, pencere boyutu değiştiğinde Fonksiyon_3 çalıştır
  
    ...
  </body>
</html>
```

{% file src="../.gitbook/assets/javascript\_events\_window.html" caption="Javascript Events \(Olaylar\) Window Örneğini İndir" %}

### 🔵 Events Yapısı ve Örnekleri

➖ Javascript olaylarına yazılan fonksiyonlarda objelerde de olduğu gibi işlemler yaptırılabilir. Örnek vermek gerekirse, iki adet farklı veri giriş alanına girilen metin birleştirilebilir. Yada butona tıklandığında bir obje türetilerek bu obje içerisindeki özellikler ekrana yazdırılabilir.

*  İki adet farklı veri giriş alanına girilen metini birleştiren örnek uygulama aşağıdaki gibidir;

```javascript
<!DOCTYPE html>
<html>
      <head> 
            <meta charset="UTF-8">
            <title>Javascript Test</title>
      </head> 
      <body>
            <input type="text" name="Metin1">
            <input type="text" name="Metin2">
            <button onclick="Metin_Birlestir(document.getElementsByName('Metin1')[0].value, document.getElementsByName('Metin2')[0].value)">Metinleri Birleştir</button>
            <p id="BirlesikMetin"></p>

            <script>
                  function Metin_Birlestir(GelenMetin1, GelenMetin2) {
                        document.getElementById("BirlesikMetin").innerHTML = GelenMetin1 + " " +GelenMetin2;
                  }
            </script>
      </body>
</html>
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n ekran &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_events_example_1.png)

{% file src="../.gitbook/assets/javascript\_events\_example\_1.html" caption="Javascript Events \(Olaylar\) Örnek Uygulama - 1 İndir" %}

* Butona tıklandığında bir obje türetilerek bu obje içerisindeki özelliklerin ekrana yazdırıldığı örnek uygulama aşağıdaki gibidir;

```javascript
<!DOCTYPE html>
<html>
      <head> 
            <meta charset="UTF-8">
            <title>Javascript Test</title>
      </head> 
      <body>
            <button onclick="ObjeTuret()">Bir Canlı Objesi Türet</button>
            <p id="TuretilenObje"></p>

            <script>
                  function ObjeTuret() {
                        var YeniObje = {
                              Turu : "İnsan",
                              Sac : "Kahverengi",
                              Goz : "Mavi",
                              Ten : "Siyahi",
                              Yas : "45",
                              Bilgiler: function(){
                                    document.getElementById("TuretilenObje").innerHTML =
                                            ("Canlı Türü : " + this.Turu) + '<br>' +
                                            ("Saç Rengi: " + this.Sac) + '<br>' +
                                            ("Göz Rengi: " + this.Goz) + '<br>' +
                                            ("Ten Rengi: " + this.Ten) + '<br>' +
                                            ("Yaşı: " + this.Yas);
                              }
                        }
                        YeniObje.Bilgiler();
                  }
            </script>
      </body>
</html>
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n ekran &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_events_example_2.png)

{% file src="../.gitbook/assets/javascript\_events\_example\_2.html" caption="Javascript Events \(Olaylar\) Örnek Uygulama - 2 İndir" %}

{% hint style="warning" %}
Kod yazarken bazı yerlerde çift tırnak " bazı yerlerde ise tek tırnak ' kullanılmasının sebebi özellikle metinsel ifadelerde yada örneklerde olduğu gibi event işlemlerinde iç içe yazımlarda yazılan kodun derlenirken kesilmemesini sağlamaktır.
{% endhint %}

## ↘ Javascript Array \(Diziler\) Kullanımı

➖ Birden fazla verinin saklanması için oluşturulan değişkenlere Array \(Dizi\) adı verilir. Dizilerin en önemli özelliği birden fazla veriye tek bir değişken altından erişebilmektir. Değişkenlerdeki her bir veriye eleman denir. Elemanları çağırmak için indis değerleri kullanılır. Dizi değişkeni oluşturulurken içerisinde yazılacak elemanlar _**köşeli parantez "\[...\]"**_ içerisinde yazılır. Ve yazılan her eleman arasına _**virgül ","**_ konulur.

       **`var`** `YeniDizi` = `["Deger1", "Deger2", "Deger3", ...];`  
           
       **`var`** `YeniDizi` = `new Array` `["Deger1", "Deger2", "Deger3", ...];`

* Şeklinde tanımlama yapılır. İki türdeki tanımlamada aynı işlevi görmektedir.

```javascript
var Sayilar = ["Bir", "İki", "Üç", "Dört", "Beş"];
console.log(Sayilar);
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_1.png)

➖ Yukarıdaki örnekte _**"Sayilar"**_ adında bir dizi oluşturulmuş içerisine beş adet eleman eklenmiş olup console üzerinde görüntülenmesi sağlanmıştır. Console çıktısında dizi içerisindeki elemanların tamamının listelendiği gözükmektedir.

### 🔵 Eleman Seçimi

➖ Dizi içerisinde belirli bir elemanın listelenmesi istenirse, bu sefer çekilecek olan elemanın indis değerinin belirtilmesi gerekmektedir.

```javascript
var Sayilar = ["Bir", "İki", "Üç", "Dört", "Beş"];
console.log(Sayilar[3]);
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_2.png)

{% hint style="danger" %}
Indis değerinin her zaman _**sıfır "0"**_ olarak başladığı unutulmamalıdır. Yani örnekteki dördüncü sıradaki _**"Dört"**_ elemanı için indis değerinin _**"3"**_ verilmesi gerekmektedir.
{% endhint %}

### 🔵 Eleman Sayısını Bulma

➖ Console ekranında indis değeri belirtilmeden dizi listelendiğine eleman sayısı gözükmektedir. Daha önceki örnekte yer alan _**"length"**_ dizi içerisindeki eleman sayısını vermektedir. Aynı zamanda özel olarak dizi içerisindeki eleman sayısının saydırılması ve farklı bir değişkene atanması içinde _**"length"**_ kullanılır.

```javascript
var Sayilar = ["Bir", "İki", "Üç", "Dört", "Beş"];
var ElemanSayisi = Sayilar.length;
console.log("Dizideki Eleman Sayısı : " + ElemanSayisi);
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_3.png)

### 🔵 Eleman Değeri Değiştirme

➖ Dizideki herhangi bir elemanın daha önceden tanımlanmış veya tanımlanmamış değerinin değiştirilmesi mümkündür. Bunun için dizide bulunan elemanın indis bilgisi kullanılarak yeni değer ataması  yapılmalıdır.

```javascript
var Sayilar = ["Bir", "İki", "Üç", "Dört", "Beş"];
Sayilar[2] = "On";
console.log(Sayilar);
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_4.png)

### 🔵 Yeni Eleman Ekleme

➖ Dizide bulunan elemanlara ekleme yapmak mümkündür. Dizi içerisine gelecek yeni eleman yada elemanlar dizinin başına, sonuna veya ortasına eklenebilir. Ekleme işlemi için üç farklı yöntem bulunmaktadır.

*  **push\(\) -** _Bu yöntemle dizinin sonuna eleman eklenir._
*  **Unshift\(\) -** _Bu yöntemle dizinin başına eleman eklenir._
*  **splice\(\) -** _Bu yöntemle dizinin ortasına eleman eklenebilir ve istenilen sayıda eleman çıkarılabilir._

```javascript
Sayilar.push("SonaEkle");    //Dizinin sonuna eleman ekleme
Sayilar.unshift("BaşınaEkle");    //Dizinin başına eleman ekleme
Sayilar.splice(2,0,"OrtayaEkle")    //Dizinin ortasına eleman ekleme, ikinci değer 0 olursa eleman silinmez !
console.log(Sayilar);
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_5.png)

### 🔵 Eleman Silme

➖ Dizide bulunan elemanlara ekleme yapıldığı gibi silme işlemi de yapılabilir. Silme işleminin yapılabilmesi için dört farklı yöntem bulunmaktadır.

* **splice\(\) -** _Belirtilen indis değerinden itibaren istenilen sayı kadar elemanın, dizi sonuna doğru silinmesini sağlar._
* **pop\(\) -** _Bu yöntemle dizinin sonundaki eleman silinir._
* **shift\(\) -** _Bu yöntemle dizinin başındaki eleman silinir._
* **delete\[\] -** _Dizi içerisinde indis bilgisi verilen elemanın değerinin boşaltılmasını sağlar._

```javascript
Sayilar.shift();    //Dizinin başından eleman silme
Sayilar.pop();    //Dizinin sonundan eleman silme
Sayilar.splice(2,1);    //Dizinin indis bilgisi 2 olan elemanından itibaren bir eleman silme
delete Sayilar[1];    //Dizi de bulunan indis bilgisi 1 olan elemanın değerini silme
console.log(Sayilar);
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_6.png)

{% hint style="warning" %}
Dizi içerisinde _**splice\(\)**_ yöntemi ile eş zamanlı eleman ekleme ve silme işlemi gerçekleştirilebilir.

```javascript
Sayilar.splice(0, 3, "Yedi", "Sekiz", "Dokuz");    //Dizi içerisinde eş zamanlı olarak eleman ekleme ve silme işlemi
```
{% endhint %}

### 🔵 Dizileri Birleştirme ve Parçalama

➖ Dizi işlemlerinden birden fazla dizi içerisindeki elemanlar tek bir dizi içerisinde birleştirilebilir. Bu işlemin tersi olan bir dizinin birden fazla dizi haline dönüştürülmesi de yapılabilir. Bunun için birleştirme işlemlerinde _**concat\(\)**_ ve parçalama işlemlerinde _**slice\(\)**_ kullanılır.

```javascript
var Dizi_1 = ["Araba", "Uçak", "Tren", "Gemi"];    //Birinci dizi ve elemanları
var Dizi_2 = ["Kırmız", "Mavi", "Yeşil"];    //İkinci dizi ve elemanları

var Birlesik_Dizi = Dizi_1.concat(Dizi_2);    //Dizi birleştirme işlemi - Birinci dizinin içerisine ikinci dizinin elemanlarını ekler 
console.log(Birlesik_Dizi);    //Birleştirilmiş dizinin console ekranına yazdırılması
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_7.png)

{% hint style="info" %}
Dizileri birleştirme işleminde kullanılan concat\(\) yönteminde birden fazla dizi birleştirilebilir.

_**`var`**_ `Birlesik_Dizi` = `Dizi_1.concat(Dizi_2, Dizi_3, Dizi_4, ...);`
{% endhint %}

```javascript
var Bolunmus_Dizi = Birlesik_Dizi.slice(0,2);    //Dizi parçalama işlemi - Dizinin içerisinden belirtilen indisten itibaren istenilen sayı kadar elemanı başka bir diziye ekle

console.log(Birlesik_Dizi);    //Birleştirilmiş dizinin console ekranına yazdırılması
console.log(Bolunmus_Dizi);    //Parçalanmış dizinin console ekranına yazdırılması
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_8.png)

{% hint style="danger" %}
Dizi parçalama işleminde kullanılan _**slice\(\)**_ yöntemi ile mevcut dizide olan eleman yeni oluşturulan diziye taşınmaz, eklenir.
{% endhint %}

### 🔵 Elemanların Sıralanması

➖ Diziler içerisinde işlem yaparken veya görüntülenmesini sağlarken daha düzenli olması aynı zamanda aramaların kolaylaşması için elemanların sıralanması gerekebilir. Dizilerde alfabetik veya küçükten büyüğe bir eleman sıralaması yapılacaksa _**sort\(\)**_, dizi içerisindeki elemanlar tersten sıralanacaksa _**reverse\(\)**_ kullanılır.

```javascript
var Siralama = ["A", "K", "F", "T", "B"];    //Dizi ve elemanları
console.log(Siralama.sort());    //Elemanların alfabetik veya küçükten büyüğe sıralanması
console.log(Siralama.reverse());    //Elemanların tersten sıralanması
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_9.png)

{% hint style="danger" %}
Her iki sıralama yöntemi kullanılırken de elemanların indis bilgilerinin değişeceği unutulmamalıdır.
{% endhint %}

### 🔵 Dizide Eleman Arama

➖ Dizilerde elemanlar üzerinde işlem yapmak eleman sayısı az olduğu sürece kolaydır. Fakat eleman sayısı fazlaysa ve eleman üzerinde işlem yapılacaksa indis bilgisinin bulunması biraz zor olabilir. Bu zorluğu aşmak için dizide eleman arama işlemi yapılır. Dizide eleman arama işlemi yapabilmek için _**indexOf\(\)**_ kullanılır. Bu yöntem ile istenilen elemanın indis bilgisine sahip olunur.

```javascript
var Sayilar = ["Bir", "İki", "Üç", "Dört", "Beş"];    //Dizi ve elemanları
console.log(Sayilar);    //Dizinin genel görünümünün console ekranına yazıdırılması
console.log("Aranan İndis : " + Sayilar.indexOf("Üç"));    //Aranılan elemanın indis bilgisinin bulunması
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_10.png)

### 🔵 Elaman Dönüştürme ve join\(\) Kullanımı

➖ Dizi içerisindeki elemanların veri türü hakkında bilgi sahibi olmak için _**typeof\(\)**_ kullanılır. Buradan alınan sonuçla elemanların veri türlerinde farklılıklar olması durumunda tek bir tür olması amacıyla _**toString\(\)**_ yöntemiyle veri türünden dönüşüm sağlanır.

```javascript
var Sayilar = ["Bir", "İki", 3, 4, 5];    //Sayilar adında dizi değişkeni
var Sayilar = Sayilar.toString();    //Dizi içerisindeki elemanların veri türünün metinsel olarak değiştirilmesi
console.log(typeof(Sayilar[2]));    //İndis değeri 2 olan elemanın veri türünün console ekranına yazdırılması
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_11.png)

➖ Dizi içerisindeki elemanlar listelenirken varsayılan olarak elemanlar arasında _**virgül ","**_ bulunur. Görüntülenmesi sırasında bunun isteğe bağlı olarak değiştirilmesi mümkündür.

```javascript
var Sayilar = ["Bir", "İki", 3, 4, 5];    //Sayilar adında dizi değişkeni
console.log(Sayilar.join("_"));    //Listeleme sırasında virgül yerine alttire işaretinin kullanılması
```

![Yukar&#x131;da kodlamas&#x131; verilen &#xF6;rnek uygulaman&#x131;n console &#xE7;&#x131;kt&#x131;s&#x131;.](../.gitbook/assets/javascript_array_example_12.png)

{% file src="../.gitbook/assets/javascript\_array.html" caption="Javascript Array \(Diziler\) Örneğini İndir" %}

## ↘ Javascript String, Number Metodları ve Math Sınıfı

➖ 

