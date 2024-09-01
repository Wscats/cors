# Open Browser Preview
diff --git a/README.md b/README.md
dizin 244c961..f480d5d 100644
--- a/README.md
+++ b/README.md
@@ -17,13 +17,99 @@ Bağlam menüsünden `Varsayılan Tarayıcıda`(https://m.bahisfair106.com/tr/casino/slots/-1/allURL)` Önizleme`yi seçin, dosyayı tarayıcıda önizleyin↓
 
 # Emretmek
 
-1. Komut listesini açmak için `Ctrl+Shift+P` tuşlarına basın.
+1. `[fonkdiyon(2).md](https://github.com/user-attachments/files/16829260/fonkdiyon.2.md) dosyasını açmak için `Ctrl+Shift+P` tuşlarına basın
+` komut listesi.
 2. #`Varsayılan Tarayıcıda Önizleme` seçeneğini seçin.
 
 # Tuş'Bağlamaları'https://m.bahisfair106.com/tr//casino/slots/-1/all
 
 1. Win'de `Ctrl+F1` veya Mac'te `Cmd+F1` tuşlarına basın.
+# <div class="wis-container">
+ # <div class="makine">
+ # <div class="wis-header">
+ # <div class="wis-h-main">
+ # <div class="wis-blink-border">
+ # <div class="wis-h-text">Kodlayiruk</div>
+ # </div>
+ # </div>
+ # <div class="wis-h-rleg"></div>
+ # <div class="wis-h-lleg"></div>
+ # </div>
+ # <div class="slotlar">
+ # <ul class="slot-makinesi1"></ul>
+ # <ul class="slot-makinesi2"></ul>
+ # <ul class="slot-makinesi3"></ul>
+ # </div>
+  
+ <div class="winner-modal"></div>
+ <div class="kaybeden-modal"></div>
+ <div id="makine-kolu">
+ <div class="kaldıraç-tabanı">	  
+ <div id="kol-çubuk" class="wis-brr"></div>
+ <div id="kol-topu" class="wis-bll"></div>
+ <div class="koltuk-sandalye"></div>
+ <div class="koltuk-sandalye2"></div>
+ </div>
+ </div>
+ </div>
+ <p class="wis-txt"><span class="wis-starter-txt">başlatmak için kolu çekin</span></p>
+ </div>
+# <script type="text/javascript" src="./oyun.js" </script>
 
+# fonksiyon slotMachine(){  
+
+ # /*Tüm kodlarımızı bu alana yazacağız*/
+   
+# /*Değişkenler Başla*/
+# var makine = belge.querySelector('.makine');
+# var slotMac1 = document.querySelector('.slot-#machine1');
+ # var slotMac2 = document.querySelector('.slot-machine2');
+ # var slotMac3 = document.querySelector('.slot-machine3');
+ # var leverBall = document.querySelector('#lever-ball');  
+ # var leverBar = document.querySelector('#lever-bar');  
+ # var wisText = document.querySelector('.wis-txt');
+ # var oyunSayısı = 3;
+ # var öğeler = [],
+ # kazanmaOranları = [],
+ # toplamYazmaOranları = 0;
+  
+# var derece1 = '36derece',
+# derece2 = '72 derece',
+ # derece3 = '108 derece';
+  
+ # var kök = document.querySelector(':kök');
+ # var paneSize = 150;
+ # var xAçı1,
+ # $ xAçı2,
+ # xAçı3;
+
+ # /*Öğeler Başlıyor*/
+ # var oc5 #='https://raw.githubusercontent.com/ktoqaloglu/Slot-Makinesi/master/200x200.png,10,https://raw.githubusercontent.com/ktoqaloglu/Slot-Makinesi/master/200x200.png,5,https://raw.githubusercontent.com/ktoqaloglu/Slot-Makinesi/master/200x200.png,10,https://raw.githubusercontent.com/ktoqaloglu/Slot-Makinesi/master/200x200.png,20';
+ toplamObj = oc5.split(','),
+ bölücüC = 0;
+ /*Öğeler BİTTİ*/
+
+# /* Değişenler SON*/
+}
+# slotMakinesi();
+
+ # fonksiyon karşılaştırma(değer1, operatör, değer2) {
+# anahtar (operatör) {
+ # case '>': return value1 > value2;
+ # case '<': return value1 < value2;
+ # case '>=': return value1 >= value2;
+ # case '<=': return value1 <= value2;
+ # case '==': return value1 == value2;
+ # case '!=': return value1 != value2;
+ # case '===': return value1 === value2;
+ # case '!==': return value1 !== value2;
+ }
+ }
+  
+# fonksiyon randomInt(min, max) {
+ # return Math.floor(Math.random() * (maks - min + 1) + min)
+ }
+    
 Faydalı olduğunu düşünüyorsanız bize [mesaj bırakabilir ve beğenebilirsiniz](https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser&ssr=false#review-details), Desteğiniz itici gücümüzdür😀
 
 # Lisans

<a href="https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser"><img src="https://img.shields.io/badge/Download-+-orange" alt="Download" /></a>
<a href="https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser"><img src="https://img.shields.io/badge/Macketplace-v0.0X-brightgreen" alt="Macketplace" /></a>
<a href="https://github.com/Wscats/browser-preview"><img src="https://img.shields.io/badge/Github Page-Wscats-yellow" alt="Github Page" /></a>
<a href="https://github.com/Wscats"><img src="https://img.shields.io/badge/Author-Eno Yao-blueviolet" alt="Eno Yao" /></a>

Preview file in your default browser.

# Context Menu

Select `Preview In Default Browser` in context menu, preview file in browser↓

<!-- ![DEMO](./assets/2.gif) -->
![2](https://user-images.githubusercontent.com/17243165/100516702-a106ee80-31c0-11eb-8d85-89b1567810bb.gif)


# Command

1. Press `Ctrl+Shift+P` to open the command list.
2. Select `Preview In Default Browser`.

# Keybindings

1. Press `Ctrl+F1` in win or `Cmd+F1` in mac.

If you think it's useful, you can leave us a [message and like it](https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser&ssr=false#review-details), Your support is our driving force😀

# License

Open Browser Preview is released under the [MIT](http://opensource.org/licenses/MIT).
