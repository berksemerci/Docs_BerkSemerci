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



