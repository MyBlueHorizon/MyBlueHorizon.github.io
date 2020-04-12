// 瞎写的ajax

function XMLHttp() {
    if (!window.XMLHttpRequest) {
        // alert("辣鸡IE6！");
        // 本来上面这行没有注释掉的，下面这行是被注释掉的，然而想想还是算了吧。。。【恻隐之心
        this.xmlhttp = new ActiveXObject("Microsoft.XMLHTTP");
    }
    else this.xmlhttp = new XMLHttpRequest();
    
    this.setReadyFunc = function(func) {
        this.xmlhttp.onreadystatechange = function() {
            if (this.readyState == 4 && this.status == 200) func(this.responseText);
        }
    }
    
    this.get = function(url, func) {
        this.setReadyFunc(func);
        this.xmlhttp.open("GET", url, true);
        this.xmlhttp.send();
    }
    
    this.post = function(url, func) {
        this.setReadyFunc(func);
        this.xmlhttp.open("POST", url, true);
        this.xmlhttp.send();
    }
    
    this.postForm = function(data, url, func) {
        this.setReadyFunc(func);
        this.xmlhttp.open("POST", url, true);
        this.xmlhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
        this.xmlhttp.send(data.join("&"));
    }
}

// 蛤蛤蛤蛤各种注释各种空格浪费你流量233333
