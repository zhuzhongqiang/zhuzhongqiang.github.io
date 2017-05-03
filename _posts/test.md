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
