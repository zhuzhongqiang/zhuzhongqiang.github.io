---
layout:     post
title:      "javascript笔记①"
subtitle:   "关于Java容器的数据结构"
date:       2017-04-23
author:     "hfj"
header-img: "img/post-bg-ios9-web.jpg"
catalog:    true
tags:
    - javascript
    - 笔记
    - 前端
---

* #### 关于&lt;script>标签的属性 ####
> ```javascript
> // async属性:
> //异步加载js文件
> <script scr="path/jsfile.js" async>
>
> //defer属性：
> //异步加载js文件，并且要等该HTML文件都加载完后，才会执行这个js文件
> <script scr="path/jsfile.js" defer="defer">
>
> ```

* #### 巧用 javascript中"||"的短路特性： ####
> ```javascript
> function add(a,b){
>    a = a || 0;
>    b = b || 0;
>    return a+b;
>};
> alert(add(undefined,14));
> //若不经过a=a||0这样的处理，当传入为undefined时，结果为NaN
> ```

* #### javascript创建对象的方式（推荐方式）
```javascript
  function Student(name,gender,age){
    this.name = name;
    this.gender = gender;
    this.age = age;
    this.profile = function(){
      alert("Hi,my name is "+this.name+","+this.age+" years old,"
            +"and I'm a "+this.gender);
    }
  }
  var stu = new Student('Tom','Boy',12);
  stu.profile();
```

* #### 动态给javascript对象增加属性的一种方式
> 给javascript对象增加属性时，可以用 obj.attrName 的方式，也可以用obj["attrattrName"]，例如：
```javascript
  var obj = new Object();
  obj.name = 'Lily';
  obj["age"] = 19;
```
当要给javascript对象增加属性时，那么可以用到 obj["attrattrName"]这种方式：
```javascript
  var obj = new Object();
  for(var i=0;i<5;i++){
    obj["attr"+i] = i;
  }
```
