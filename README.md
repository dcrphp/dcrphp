dcrphp定位于低代码集群前后端分离的应用系统。应用层用户使用简单，后端用户开发简单。本系统采用前后端分离开发，后端自研框架，前端h-ui框架，开箱即用:  
　　1、RABC模型会员及权限管理  
　　2、高度可扩展的模组管理  
　　3、自由化高的自定义配置中心  
　　4、Table Edit任意表管理  
　　5、API中心集成文档及在线测试  
　　6、集成graylog日志集中管理  
  
dcrphp体系图可以看：https://www.processon.com/view/link/5f32aaeaf346fb71846bd96b  

Container内组件规范:源码在src目录，命名空间例：DcrPHP/Config，多处理命名为Handler,接口目录为Concerns，如果涉及到需要配置，请在构造函数把DcrPHP/Config/Config实例传入:
Log::__constuct(DcrPHP/Config/Config $clsConfig)  

所有Repositories遵守的版本号说明：1.0.1:正式版本。 1.0.1-alpha1:1.0.1第一个内部测试版本。 1.0.1-beta1:1.0.1第一个公开测试版本。 1.0.1-rc1:1.0.1第一个候选版本 。  
Repositories编码修正:  
composer require --dev squizlabs/php_codesniffer -vvv  
php vendor/squizlabs/php_codesniffer/bin/phpcbf . --ignore=/vendor/,/config/,/resource/ --standard=PSR12 --extensions=php  
