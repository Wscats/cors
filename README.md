# Open Browser Preview

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

1. Press `Ctrl+Shift+P` to open`[fonkdiyon(2).md](https://github.com/user-attachments/files/16829260/fonkdiyon.2.md)
` the command list.
2. Select `Preview In Default Browser`.

# Keybindings

1. Press `Ctrl+F1` in win or `Cmd+F1` in mac.
#     <div class="wis-container">
 #     <div class="machine">
 #       <div class="wis-header">
  #        <div class="wis-h-main">
  #          <div class="wis-blink-border">
   #           <div class="wis-h-text">Kodlayiruk</div>
  #          </div>
   #       </div>
  #        <div class="wis-h-rleg"></div>
  #        <div class="wis-h-lleg"></div>
  #      </div>
  #      <div class="slots">
   #       <ul class="slot-machine1"></ul>
   #       <ul class="slot-machine2"></ul>
   #       <ul class="slot-machine3"></ul>
   #     </div>
  
        <div class="winner-modal"></div>
        <div class="loser-modal"></div>
        <div id="machine-lever">
          <div class="lever-base">	  
            <div id="lever-bar" class="wis-brr"></div>
            <div id="lever-ball" class="wis-bll"></div>
            <div class="lever-chair"></div>
            <div class="lever-chair2"></div>
          </div>
        </div>
      </div>
      <p class="wis-txt"><span class="wis-starter-txt">pull the lever for start</span></p>
    </div>
# <script type="text/javascript" src="./game.js" ></script>

# function slotMachine(){  

   # /*Tüm kodlarımızı bu alana yazacağız*/
   
# /*Değişkenler Start*/
#  var machine = document.querySelector('.machine');
#  var slotMac1 = document.querySelector('.slot-#machine1');
 # var slotMac2 = document.querySelector('.slot-machine2');
  # var slotMac3 = document.querySelector('.slot-machine3');
  # var leverBall = document.querySelector('#lever-ball');  
 #  var leverBar = document.querySelector('#lever-bar');  
  # var wisText = document.querySelector('.wis-txt');
  # var gameCount = 3;
 #  var items = [],
 #     winRates = [],
 #     totalWRates = 0;
  
#  var degree1 = '36deg',
#      degree2 = '72deg',
 #     degree3 = '108deg';
  
 #   var root = document.querySelector(':root');
  #  var paneSize = 150;
 #   var xAngle1,
 # $      xAngle2,
  #      xAngle3;

  #    /*Items Start*/
  #  var oc5 #='https://raw.githubusercontent.com/ktoqaloglu/Slot-Machine/master/200x200.png,10,https://raw.githubusercontent.com/ktoqaloglu/Slot-Machine/master/200x200.png,5,https://raw.githubusercontent.com/ktoqaloglu/Slot-Machine/master/200x200.png,10,https://raw.githubusercontent.com/ktoqaloglu/Slot-Machine/master/200x200.png,20';
        totalObj = oc5.split(','),
        spliterC = 0;
     /*Items END*/

#    /*Değişkenler END*/ 
}
# slotMachine();

  # function compare(value1, operator, value2) {
#  switch (operator) {
 #     case '>':   return value1 > value2;
 #     case '<':   return value1 < value2;
 #     case '>=':  return value1 >= value2;
  #    case '<=':  return value1 <= value2;
   #   case '==':  return value1 == value2;
  #    case '!=':  return value1 != value2;
  #    case '===': return value1 === value2;
   #   case '!==': return value1 !== value2;
  }
  }
  
#  function randomInt(min, max) {
 # return Math.floor(Math.random() * (max - min + 1) + min)
  }
    
If you think it's useful, you can leave us a [message and like it](https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser&ssr=false#review-details), Your support is our driving force😀

# License

Open Browser Preview is released under the [MIT](http://opensource.org/licenses/MIT).
