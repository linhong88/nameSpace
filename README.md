# nameSpace
nameSpace整理
> 【手动引入autoLoad】  
 if(strpos($class, 'Vendor') !== FALSE)
 {
        require_once  APP_ROOT.'Lib/vendor/Autoloader.php';
        (new Vendor\Autoloader())->autoload($class);
 }
 
 【使用composer】以monolog为例
 流程；安装composor->在目录下执行composer require monolog/monolog->会生成vendor文件，结构：
 composer.json
            ├── autoload.php
            ├── psr(目录)
            ├── monolog(目录)
            └── composer(目录)
 -> 调用例子：
$log = new Monolog\Logger('testMonoLog');
$log->pushHandler(new Monolog\Handler\StreamHandler('/home/data/logs/act-dev.huolala.cn:11008/testCom.log', \Monolog\Logger::WARNING));
$log->warn('Foo');
$log->error('Bar');
