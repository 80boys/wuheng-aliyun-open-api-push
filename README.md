# wuheng-aliyun-open-api-push
aliyun-open-api-push 2.0 2016-08-01

# 使用方法
# 此版本 是官方SDK 2.0版本  composer 封装
# 首先 初始化 项目
# composer 安装

new Aliyun\Core\Config();

 ## $accessKeyId    = '你的accessKeyId '; 
 $accessKeySecret = '你的 accessKeySecret';
 
$iClientProfile = Aliyun\Core\Profile\DefaultProfile::getProfile("cn-hangzhou", $accessKeyId, $accessKeySecret);
$client         = new \Aliyun\Core\DefaultAcsClient($iClientProfile);
$request        = new \Push\Request\V20160801\PushRequest();

# 各种初始化 赋值操作 
# 详情看 vendor\wuheng\aliyun-open-api-push\Push\Request\V20160801\PushRequest.php
# 里面的代码

$request->setAppKey('你的用用 appkey');
$request->setTitle('推送标题'); 
$request->setBody('推送内容'); 

//各种参数 赋值
//.......................................

//发送推送
$client->getAcsResponse($this->request);


