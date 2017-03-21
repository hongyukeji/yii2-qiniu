yii2-qiniu
=================================
* @author Shadow <admin@hongyuvip.com>
* @version 1.1

file upload for Yii Framework 2

php > 5.5 

How to install?
To use this extension, you may insert the following code:
--------------------------------

Get it via [composer](http://getcomposer.org/) by adding the package to your `composer.json`:

```json
{
  "require": {
    "hongyukeji/yii2-qiniu": "dev-master"
  }
}
```
```php
php composer.phar update
```

Usage
-----

```php
<?php
$ak = 'sss';
$sk = 'sss';
$domain = 'http://demo.domain.com/';
$bucket = 'demo';
use hongyukeji\qiniu\Qiniu;
$qiniu = new Qiniu($ak, $sk,$domain, $bucket);
$key = time();
$qiniu->uploadFile($_FILES['tmp_name'],$key);
$url = $qiniu->getLink($key);
```
