# 移动端仿console.log函数

引入函数后调用，会在手机屏幕创建一个白色底的div，并打印出参数的内容

```
//调用方法
debug('这里可以填入变量等内容');
//函数
function debug(cont){
    if(!document.querySelector('#js-debugbox')) {
        var div = document.createElement('div');
        div.setAttribute('id','js-debugbox');
        div.style.cssText = 'width:5rem; height:8rem;background: #fff; font-size:.2rem; color:#000; position: absolute; top:0;left:0;z-index: 999;over-flow:scroll';
        document.querySelector('body').appendChild(div);
        console.log(div);
    }
    var debugbox = document.querySelector('#js-debugbox'),
        p = document.createElement('p');
    p.innerHTML = cont;
    debugbox.appendChild(p);
}

```
