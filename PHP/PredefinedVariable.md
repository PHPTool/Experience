/*
*/
- $_REQUEST 与 $_GET 和 $_POST 相互不干扰
（意味着更改 $_GET 和 $_POST 对 $_REQUEST 无影响）
```php
<?php

$_GET['foo'] = 'a';
$_POST['bar'] = 'b';
var_dump($_GET); // Element 'foo' is string(1) "a"
var_dump($_POST); // Element 'bar' is string(1) "b"
var_dump($_REQUEST); // Does not contain elements 'foo' or 'bar'

?>
```

