# 如何更好的写 php 代码

标签（空格分隔）： Modern PHP 读书笔记

---

最近在看 《Modern PHP》，这本书基于 PHP the right way ，php正确之道，而写。

## 一. composer(基于 namespace psr-4)
composer 代码包管理，为你开启了一扇大门，你可以站到，巨人肩膀上，很多别人写过的 库，比如 log，http，路由，autoload，推送，只要在 https://packagist.org/ 上搜索，都可以立即集成到你的 代码里，大大的加速了我们完成 工作的速度与质量

## 二.良好实践(基于的编程思想)
### 1 .过滤，验证，转义 输入的数据
### 2 .密码，ssh
### 3 .日期，实践 DataTime类，代替以前的时间函数
### 4 .数据库，我们用 pdo，以及预处理和参数绑定，来过滤sql注入
### 5 .多字节，unicode
### 6 .错误和异常  

## 三.代码控制和部署
### 1.git 管理代码
### 2.capistrano自动部署代替 ftp

### 四.测试与调试分析
### 1.phpunit测试
### 2.xdebug调试

### 五. hhvm，hack，社区
