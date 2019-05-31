# ios-iap-php

iOS支付验证

## install
```bash
composer require sn01615/ios-iap-php
```

```php

use sn01615\iap\ios\Verify;

include "../vendor/autoload.php";

$cc = new Verify();

$receipt = ".."; // 凭据

$cc->endpoint(true);// 可选切换到沙盒环境

$vv = $cc->query($receipt);

// 打印结果
var_dump($vv);

```