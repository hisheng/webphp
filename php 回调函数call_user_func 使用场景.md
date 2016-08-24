# php 回调函数call_user_func 使用场景

标签： php call_user_func

---

## 一.何为回调函数
call_user_func 主要用来是一个 调用函数 的函数

``` php
function sayhi(){
    echo 'hellossss';
}
call_user_func('sayhi');
 
```
在这里，其实我们可以发现，和直接调用sayhi() 效果是一样的

## 二.有什么不同，主要场景，主要用来调用 未知名字的函数
1、你要调用的函数名，你不知道
2、要调用函数的参数类型及个数也是未知的

``` php
switch($value)
{
    case 7:
        $func = 'run';
        break;
    default:
        $func = 'stop';
        break;
}

call_user_func($func, 'stuff');
```
## 三.例子  
### 1.call_user_func 带参数，主要是非 数组的参数

``` php
function sayhi($name){
    echo $name.' 您好';
}
$name = '周杰伦';
call_user_func('sayhi',$name); //周杰伦 您好
```
### 2.call_user_func 带多个参数
``` php
function say($name,$hi){
    echo $name.' '.$hi;
}
$name = '周杰伦';
$hi = '你好啊';
call_user_func('say',$name,$hi); //周杰伦 你好啊
```
### 3.call_user_func_array 带1个数组，代替2的情况
``` php
function saynew($p){
    echo $p['name'].' '.$p['hi'];
}
$name = '周杰伦';
$hi = '你好啊';
$p = array('name'=>$name,'hi'=>$hi);
call_user_func('saynew',$p); //周杰伦 你好啊
```

