# Bookmarklet-to-get-YouTube-channel-ID
Bookmarklet to get YouTube channel ID

```
javascript:(function(){function a(e){var a=document.createElement("textarea");a.style.position="fixed",a.style.opacity=0,a.value=e,document.body.appendChild(a),a.focus(),a.select(),document.execCommand("copy"),document.body.removeChild(a)}var b=document.querySelector("meta[property='og:url']"),c=document.querySelector("meta[property='web:url']"),d;if(b){var e=b.getAttribute("content");a(e),d="%E3%82%B3%E3%83%94%E3%83%BC%E3%81%97%E3%81%BE%E3%81%97%E3%81%9F%EF%BC%81\n"+e}else if(c){var f=c.getAttribute("content");a(f),d="%E3%82%B3%E3%83%94%E3%83%BC%E3%81%97%E3%81%BE%E3%81%97%E3%81%9F%EF%BC%81\n"+f}else d="%E5%8F%96%E5%BE%97%E3%81%A7%E3%81%8D%E3%81%BE%E3%81%9B%E3%82%93%E3%81%A7%E3%81%97%E3%81%9F";alert(d)})();void(0);
```

```javascript
javascript:(function(){
    function copyToClipboard(text) {
        var textArea = document.createElement("textarea");
        textArea.style.position = "fixed";
        textArea.style.opacity = 0;
        textArea.value = text;
        document.body.appendChild(textArea);
        textArea.focus();
        textArea.select();
        document.execCommand("copy");
        document.body.removeChild(textArea);
    }

    var ogUrl = document.querySelector("meta[property='og:url']");
    var webUrl = document.querySelector("meta[property='web:url']");
    var alertMessage;

    if (ogUrl) {
        var ogContent = ogUrl.getAttribute("content");
        copyToClipboard(ogContent);
        alertMessage = "コピーしました！\n" + ogContent;
    } else if (webUrl) {
        var webContent = webUrl.getAttribute("content");
        copyToClipboard(webContent);
        alertMessage = "コピーしました！\n" + webContent;
    } else {
        alertMessage = "取得できませんでした";
    }

    alert(alertMessage);
})();void(0);
```
