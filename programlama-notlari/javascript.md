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

🔵 Javascript genellikle &lt;head&gt; veya &lt;body&gt; tag'ları içerisinde çalıştırılır. Her ikisine de yazılmasına gerek yoktur. Sayfanın çalıştırılma prensibi ve yükleme hızı göz önüne alınarak tercihte bulunularak yazılır. Yukarıdaki örnekte basit bir Javascript yapısı bulunmaktadır. Javascript tanımlamaları sayfa içerisinde yapılacaksa mutlaka &lt;script&gt; ile başlamalı ve &lt;/script&gt; ile kapatılmalıdır. Script tag içerisinde bulunun alert\(\); ise sayfa yüklendiğinde ekrana uyarı mesajı verilmesini sağlar. 

![Yukar&#x131;da basit kodlamas&#x131; verilen ve a&#xE7;&#x131;klamas&#x131; yap&#x131;lan &#xF6;rne&#x11F;in ekran g&#xF6;r&#xFC;n&#xFC;m&#xFC;.](../.gitbook/assets/screenshot_2.png)

🔵 Eğer Javascript tagları içerisinde komplike ve birden fazla işlem yapılacaksa hem daha düzenli olması hem de ileride yapılabilecek değişikliklerde yada meydana gelecek hatalarda kod satırlarının anlaşılabilir olması için ayrı bir dosya haline getirilerek dış bağlantı şeklinde projeye eklenmesi daha sağlıklı olacaktır. Bunun için tıpkı bir .html dosyası oluşturur gibi sonu .js ile biten bir Javascript dosyası oluşturmamız ve &lt;script&gt; tagları içerisindeki kod satırlarımızı buraya aktarmamız gereklidir. Daha sonrasında bu kodların index veya oluşturulan başka bir sayfada işlenebilir olması için bağlantısının "src" ile yapılması gerekmektedir. Bu bağlantı aşağıda bulunan örnekteki gibi yapılmaktadır. 

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

* alert\(\) veya window.alert\(\)

  🔹 Aslında ikisi de aynı işlevi görmektedir. Amacı sayfa yüklendiğinde ekrana bildirim göndermektir.

```text
alert("Sayfaya Hoşgeldiniz !!!");
window.alert("Sayfaya Hoşgeldiniz !!!");
```

* innerHTML 🔹 Seçili olan element veya elementlerin istenilen değeri almasını sağlar.

{% hint style="danger" %}
innerHTML yapısının kullanılabilmesi için değer verilmesi istenilen element veya elementler mutlaka seçilmelidir. Seçim işlemlerinde elementin id, name, class veya tag türü kullanılabilir.
{% endhint %}

{% tabs %}
{% tab title="Element by ID" %}
Değer verilmek istenilen elementin ID değerine göre atama yapan kod parçacığıdır. ID unique olması gerektiğinden tek bir ID değerine atama yapılır.

```text
document.GetElementByID("ID_Adi").innerHTML = "Atanacak_Deger";
```
{% endtab %}

{% tab title="Elements by Name" %}
Değer verilmek istenilen elementlerin ad değerine göre atama yapan kod parçacığıdır. Ad değeri birden fazla elementte aynı olarak kullanılabileceğinden çoğul işlemler gerçekleştirir. Aynı ad içerisindeki element kümesinde değer verilmek istenilen elementin indis değeri belirtilmelidir.

```text
document.GetElementsByName("Name_Adi")[0].value = "Atanacak_Deger";
```

{% hint style="warning" %}
innerHTML eğer bir form işleminde veya input için kullanılacaksa value olarak yazılmalıdır. Çünkü bu alanlarda değer yazdırılma yapılmaz, değer atanması gerçekleştirilir.
{% endhint %}
{% endtab %}

{% tab title="Elements by Class" %}
Değer verilmek istenilen elementlerin class değerine göre atama yapan kod parçacığıdır. Class değeri birden fazla elementte aynı olarak kullanılabileceğinden çoğul işlemler gerçekleştirir. Aynı class içerisindeki element kümesinde değer verilmek istenilen elementin indis değeri belirtilmelidir.

```text
document.GetElementsByClassName("Class_Adi")[0].innerHTML = "Atanacak_Deger";
```
{% endtab %}

{% tab title="Elements by Tag" %}
Değer verilmek istenilen elementlerin tag türüne göre atama yapan kod parçacığıdır. Tag değeri birden fazla elementte aynı olarak kullanılabileceğinden çoğul işlemler gerçekleştirir. Aynı tag içerisindeki element kümesinde değer verilmek istenilen elementin indis değeri belirtilmelidir.

```text
document.GetElementsByTagName("Tag_Turu")[0].innerHTML = "Atanacak_Deger";
```
{% endtab %}
{% endtabs %}

* document.write\(\) 🔹Sayfanın boş olan herhangi bir yerinde istenilen yazının veya değerin görüntülenmesini sağlar.

```text
document.write(Sayfada Gözükecek Yazı...);
```

* console.log\(\) 🔹Tarayıcı kaynak görüntülemesinde bulunun konsol sekmesinde istenilen işlemlerin görüntülenmesini sağlar.

```text
console.log(Bu Bir Konsol Denemesidir !);
```

{% hint style="warning" %}
Javascript'te tıpkı diğer birçok dildeki gibi her bir kod satırı noktalı virgül ";" işareti ile ayrılır.

Açıklama satırı eklenecek ise çift eğik çizgi "//" veya yıldız-eğik çizgi "/\*......\*/" kullanılır.
{% endhint %}

