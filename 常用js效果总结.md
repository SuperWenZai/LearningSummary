## 返回顶部

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
