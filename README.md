# ios-iap-php

iOS支付验证

## install
```bash
composer require sn01615/apple-iap-php
```

## use
```php

use sn01615\iap\ios\Verify;

include "../vendor/autoload.php";

$cc = new Verify();

$receipt = ".."; // 凭据

$cc->endpoint(true);// 可选切，换到沙盒环境

$cc->setPassword('123');// 可选，如果是连续订阅需要密码

$vv = $cc->query($receipt);

// 打印结果
var_dump($vv);

```
