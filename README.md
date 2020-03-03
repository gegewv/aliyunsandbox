# 支付宝支付（沙箱测试）

* 注册蚂蚁金服开放平台的商户账号
* 下载服务端SDK
    - [电脑网站支付SDK&DEMO](https://docs.open.alipay.com/270/106291/)
    - [手机网站支付SDK&DEMO](https://docs.open.alipay.com/54/106682/)
* 配置密钥
    - 应用密钥 `APP_PUBLIC_KEY`
    - 应用私钥 `APP_PRIVATE_KEY`
* [下载 `支付开放平台开发助手`](https://docs.open.alipay.com/291/105971/)
    - 打开工具 `-->` 选择密钥工具 `-->` 生成密钥
    - 选择密钥长度：RSA2 `-->` 选择密钥格式：PKCS1(非JAVA适用) `-->` 点击生成密钥按钮
* 点击 开发者中心 `-->` 研发服务 `-->` 沙箱环境 `-->` 沙箱应用 `-->` 设置 `RSA2密钥` `-->` 填写上一步生成的 `应用公钥` `-->` 验证公钥的正确性，按照指示下载工具，按照要求验证即可（熟练配置过程后一般不会出现错误，可以忽略这一步）
* 修改SDK中的 `config.php`
    - `app_id` 沙箱的 `APPID`
    - `merchant_private_key` 第4步生成的 `应用私钥`
    - `gatewayUrl` 沙箱的支付宝网关 `https://openapi.alipaydev.com/gateway.do`
    - `alipay_public_key` 第5步设置应用公钥后生成的 `支付宝公钥`
    - `notify_url` 改成相应的路径
    - `return_url` 改成相应的路径
* 查看运行环境，开启PHP扩展 `php_openssl`
* 访问页面
* 下载 [`沙箱钱包`](https://sandbox.alipaydev.com/user/downloadApp.htm)，使用沙箱账号中的买家账号登录，即可扫码付款