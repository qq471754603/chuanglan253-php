# chuanglan-php
chuanglan-php-demo

## 快速开始

----------------------------------------------发送短信接入流程：--------------------------------------------------

1.登录 https://zz.253.com

2.获取接口API账号，密码：选择任意产品>激活>企业认证（上传公司营业执照）

3.申请签名（以公司简称或缩写命名）备注：平台申请签名，API接口加上申请签名

4.模板申请（自定义编辑内容）：选择任意应用>短息编辑栏目{模板管理}>添加模板  

备注：申请模板可达到短信免审作用


---------------------------------------------创蓝 php 短信发送事例-------------------------------------------------

1、普通发送(批量发送短信使用英文逗号间隔，事例如下)

require_once 'sendSMSAPI.php';

$clapi  = new ChuanglanSmsApi();

$code = mt_rand(100000,999999);

$result = $clapi->sendSMS('15300002325,18900001862','【253云通讯】您好，您的验证码是'.$code ); 

2、变量发送（批量发送参数组使用英文分好间隔，事例如下）
 
require_once 'sendVariableSMSAPI.php';

$clapi  = new ChuanglanSmsApi();

$msg = '【253云通讯】{$var},您好，您发送的内容是{$var}';

$params = '15300001520,李先生,2017-04-12;15800009999,张先生，145444';

$result = $clapi->sendVariableSMS($msg, $params);


----------------------------------------------创蓝php demo php文件说明---------------------------------------------

sendSMS.zip-----普通短信发送

balanceQuery.zip------余额查询

sendVariableSMS.zip--------变量短信发送 

依据您需求选择对应功能文件，参考示例说明操作

下载完成 将demo放入到项目环境中、填写示例中的参数 请求API账号密码以及接口地址请登录zz.253.com获取

具体详情请阅读-->253云通讯PaaS短信云接口说明（JSON版）.docx

## 联系我们



[创蓝客服 链接](https://kefu253.udesk.cn/im_client/?web_plugin_id=47820={"name":"github"})



## 文档链接
- [api文档](https://www.253.com/#/document/1)
