# php.ini

>PHP 一般有 两个 INI 文件.  
一个用于生产环境(production)，一个用于开发环境(development)

; PHP comes packaged with two INI files. One that is recommended to be used  
; in production environments and one that is recommended to be used in  
; development environments.  

---

>是否显示所有错误。

; display_errors  
;   Default Value: On  
;   Development Value: On  
;   Production Value: Off  

---

>每个脚本解析输入数据(POST, GET, upload)的最大允许时间(秒) -1 表示不限制

; max_input_time  
;   Default Value: -1 (Unlimited)  
;   Development Value: 60 (60 seconds)  
;   Production Value: 60 (60 seconds)  

---

>用户定义的php.ini文件(.htaccess)的名字 . 默认是  ".user.ini"

; Name for user-defined php.ini (.htaccess) files. Default is ".user.ini"  
;user_ini.filename = ".user.ini"  

---

>用户定义的 php.ini 配置文件的TTL(time-to-live:生存时间),单位为秒. 默认是 300 秒(即 5 分钟)。   
修改配置后5分钟内会自动生效，不需要重启服务

;user_ini.cache_ttl = 300

---

>; 如果设置open_basedir，会将所有文件操作限制到定义的目录及以下。  
 ; 此指令如果在每个目录或每个虚拟主机的Web服务器配置文件中使用最有意义。  
 ; http://php.net/open-basedir  
open_basedir 将php所能打开的文件限制在指定的目录树中，包括文件本身。当程序要使用例如fopen()或file_get_contents()打开一个文件时，这个文件的位置将会被检查。当文件在指定的目录树之外，程序将拒绝打开。
 
; open_basedir, if set, limits all file operations to the defined directory  
; and below.  This directive makes most sense if used in a per-directory  
; or per-virtualhost web server configuration file.  
; http://php.net/open-basedir  
;open_basedir =  
 
---

>; 默认值为 FALSE 。 如果设置为 TRUE ，在客户端断开连接后，脚本不会被中止。  
 ; 如果启用，即使用户中止请求，该请求也将被允许完成。  
 ; 如果执行长请求，这可能最终会由用户或浏览器超时被中断，这样考虑启用它。   
 ; http://php.net/ignore-user-abort  
 ;ignore_user_abort = On  

; If enabled, the request will be allowed to complete even if the user aborts  
; the request. Consider enabling it if executing long requests, which may end up  
; being interrupted by the user or a browser timing out. PHP's default behavior  
; is to disable this feature.  
; http://php.net/ignore-user-abort  
;ignore_user_abort = On  

---

>; 决定是否暴露 PHP 被安装在服务器上（例如在 Web 服务器的信息头中加上其签名：X-Powered-By: PHP/5.6.30)    
 ; 这个不是安全威胁, 但它可以确定是否在您的服务器上使用PHP。  
 ; http://php.net/expose-php  

; Decides whether PHP may expose the fact that it is installed on the server  
; (e.g. by adding its signature to the Web server header).  It is no security  
; threat in any way, but it makes it possible to determine whether you use PHP  
; on your server or not.  
; http://php.net/expose-php  
expose_php = On  

---

>; 每个脚本的最大执行时间，以秒为单位  
 ; http://php.net/max-execution-time  
 ; 注意: 在CLI SAPI模式下，这个指令会被硬编码为O  
 max_execution_time = 30  
 
; Maximum execution time of each script, in seconds  
; http://php.net/max-execution-time  
; Note: This directive is hardcoded to 0 for the CLI SAPI  
max_execution_time = 30  

---

>; 设置POST、GET以及PUT方式接收数据时间限制。  
 ; 可以在生产环境中设置这个值 来消除意外长时间运行的脚本  
 ; 注意: 这个指令在CLI SAPI环境下会被硬编码为-1  
 ; 默认值是: -1 (不限制) 开发环境: 60 (60 秒) 生产环境: 60 (60 秒)  
 ; http://php.net/max-input-time  
 max_input_time = 60  

; Maximum amount of time each script may spend parsing request data. It's a good  
; idea to limit this time on productions servers in order to eliminate unexpectedly  
; long running scripts.  
; Note: This directive is hardcoded to -1 for the CLI SAPI  
; Default Value: -1 (Unlimited)  
; Development Value: 60 (60 seconds)  
; Production Value: 60 (60 seconds)  
; http://php.net/max-input-time    
max_input_time = 60  

---

>; 在PHP文档之前自动添加文件.  
 ; http://php.net/auto-prepend-file  
 auto_prepend_file =  

; Automatically add files before PHP document.  
; http://php.net/auto-prepend-file  
auto_prepend_file =  

---

>; 在PHP文档之后自动添加文件  
 ; http://php.net/auto-append-file  
 auto_append_file =  

; Automatically add files after PHP document.  
; http://php.net/auto-append-file  
auto_append_file =  

---

>; 默认情况下，PHP将使用Content-Type头输出类型。  
 ; 设置为空时即可禁用  
 ; PHP的内置默认类型设置为 text/html  
 ; http://php.net/default-mimetype    
 default_mimetype = "text/html"  

; By default, PHP will output a media type using the Content-Type header. To  
; disable this, simply set it to be empty.  
; PHP's built-in default media type is set to text/html.  
; http://php.net/default-mimetype  
default_mimetype = "text/html"  

---

