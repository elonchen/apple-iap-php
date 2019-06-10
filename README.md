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

## 参考链接

订阅
https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/StoreKitGuide/Chapters/Subscriptions.html

收据
https://developer.apple.com/library/archive/releasenotes/General/ValidateAppStoreReceipt/Chapters/ReceiptFields.html#//apple_ref/doc/uid/TP40010573-CH106
