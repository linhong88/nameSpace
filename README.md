# nameSpace
nameSpace整理
> 【手动引入autoLoad】  
 if(strpos($class, 'Vendor') !== FALSE)
 {
        require_once  APP_ROOT.'Lib/vendor/Autoloader.php';
        (new Vendor\Autoloader())->autoload($class);
 }
 
 【使用composer】
 
