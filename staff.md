title: 客服
---

微信的客服才能发送消息或者群发消息，而且还有时效限制，真恶心的说。。。

## 获取实例

```php
<?php
use EasyWeChat\Foundation\Application;
// ...
$app = new Application($options);

$staff = $app['staff'];
```

## API

### 获取所有客服账号列表

```php
$staff->lists();
```

### 获取所有在线的客服账号列表

```php
$staff->onlines();
```

### 添加客服帐号

```php
$staff->create($email, $nickname, $password);
```

### 修改客服帐号

```php
$staff->update($email, $nickname, $password);
```

### 删除客服帐号

```php
$staff->delete($email);
```

### 设置客服帐号的头像

```php
$staff->avatar($email, $avatarPath);
```

### 主动发送消息给用户

```php
$staff->message($message)->to($openId)->send();
```

### 指定客服发送消息

```php
$staff->message($message)->by('account@test')->to($openId)->send();
```


关于更多客服接口信息请参考微信官方文档：http://mp.weixin.qq.com/wiki/9/6fff6f191ef92c126b043ada035cc935.html
