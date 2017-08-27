# phone_shipei
移动端适配
```
(function (doc, win) {
    var docEl = doc.documentElement,
        resizeEvt = 'orientationchange' in window ? 'orientationchange' : 'resize',
        recalc = function () {
            var clientWidth = docEl.clientWidth;
            if (!clientWidth) return;
            if(clientWidth>=1040){
              docEl.style.fontSize = '100px';
            }else{
              docEl.style.fontSize = 45 * (clientWidth / 750) + 'px';
            }
        };

    if (!doc.addEventListener) return;
    win.addEventListener(resizeEvt, recalc, false);
    doc.addEventListener('DOMContentLoaded', recalc, false);
})(document, window);
```


 docEl.style.fontSize = 45 * (clientWidth / 750) + 'px';
 
 里面的45是根据设计图尺寸来的，一般给50就是750的设计图
