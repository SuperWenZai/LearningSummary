## 1.返回顶部

``` bash

$(function() {
    $('.top').hide();
    $(window).scroll(function() {
        if ($(window).scrollTop() >= 100) {
            $('.top').fadeIn(300);
        } else {
            $('.top').fadeOut(300);
        }
    });
    $('.top').click(function() {
        $('html,body').animate({
            scrollTop: '0px'
        },
        800);
    });
})；

```

## 2.判断页面加载是否完成

``` bash

document.onreadystatechange = loadingChange; //当页面加载状态改变的时候执行这个方法.  
function loadingChange() {
    if (document.readyState == "complete") { //当页面加载状态为完全结束时进入   
        $(".loading").hide(); //当页面加载完成后将loading页隐藏  
        window.location.href = "http://www.baidu.com";
    }
}

```

## 3.禁止鼠标右键

``` bash

$(document).ready(function() {
    $(document).on("contextmenu",
    function(e) {
        return false;
    });
});

```

## 4.判断是pc端还是移动端

``` bash

function getClientInfo() {
    var banner = document.getElementById('banner');
    var userAgentInfo = navigator.userAgent;
    var Agents = new Array("Android", "iPhone", "SymbianOS", "Windows Phone", "iPad", "iPod");
    var agentinfo = null;
    for (var i = 0; i < Agents.length; i++) {
        if (userAgentInfo.indexOf(Agents[i]) > 0) {
            agentinfo = userAgentInfo;
            break;
        }
    }
    if (agentinfo) {
        $('.banner').css('height', 'auto');
        banner.style.height = 'auto'
    } else {
        $('.banner').css($(window).height());
        banner.style.height = document.body.clientHeight
    }
}

```

## 5.判断是否是ie浏览器

``` bash

function isIE() { //ie?    
    if ( !! window.ActiveXObject || "ActiveXObject" in window) {
        return true;
    } else {}
    return false;
}

```

## 5.点击锚点跳到对应的位置

``` bash

$(".aa").click(function(event) {
    event.preventDefault(); //取消事件的默认动作。
    $('html,body').animate({
        scrollTop: $(this.hash).offset().top
    },
    800);
});

```
