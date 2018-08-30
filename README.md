# Nginx 1.15.3 with all available 3rd party modules bundle

Official module list:
https://www.nginx.com/resources/wiki/modules/

All modules which have git repo are added as submodule under modules.

### Exception:
#### Unable to find config file:

[AFCGI](https://github.com/rsms/afcgi "Asynchronous/multiplexing FastCGI for NGINX")

[Pubcookie](https://github.com/ivandeex/pubcookie "Adds Pubcookie-based cross-site authentication method to NGINX")

[FastCGI Functional Handler](https://github.com/Taymindis/fcgi-function "c/c++ service function handler which built for NGINX fastcgi")

[mruby](https://github.com/matsumotory/ngx_mruby "Embedded mruby script language for nginx-module")


#### No git repo:

[Request Authentication](http://mdounin.ru/hg/ngx_http_auth_request_module/ "Allows authorization based on subrequest result")

[MP4 Streaming Lite](http://i.6.cn/nginx_mp4_streaming_public_20081229.tar.bz2 "Seeks time within H.264/MP4 files if a “start” parameter is in the URL")

[Owner Match](https://heiher.info/1755.html "Provides a simple file owner-based access control")

[Passenger](https://www.phusionpassenger.com/ "NGINX-based application server for Ruby, Node.js and Python apps")

[Postgres](http://labs.frickle.com/nginx_ngx_postgres "Allows NGINX to communicate directly with PostgreSQL database")

[HTTP Redis](https://people.freebsd.org/~osa/ngx_http_redis-0.3.8.tar.gz "Redis support module")

[sFlow](https://code.google.com/archive/p/nginx-sflow-module/downloads "Operational performance monitoring with standard sFlow protocol")

[SlowFS Cache](http://labs.frickle.com/nginx_ngx_slowfs_cache "Adds ability to cache static files")

[Supervisord](http://labs.frickle.com/nginx_ngx_supervisord "Communicate with supervisord and manage backends on-demand")

#### Duplicated & Outdated:

[Eval](https://github.com/vkholodkov/nginx-eval-module "A module for evaluating memcached or proxy response into variable")

****

|Author|hajuuk|
|---|---|
|Email|hajuuk@gmail.com|

****
### array-var-nginx-module
Add support for array variables to NGINX config files

##### Prerequisite:
    --add-dynamic-module=../modules/ngx_devel_kit

##### Compile Command:
    --add-dynamic-module=../modules/array-var-nginx-module

### drizzle-nginx-module
Make NGINX talk directly to MySQL or Drizzle database servers

##### Prerequisite:
    libdrizzle

##### Compile Command:
    --add-dynamic-module=../modules/drizzle-nginx-module
    
### echo-nginx-module
Provides familiar shell-style commands to NGINX HTTP servers

##### Compile Command:
    --add-dynamic-module=../modules/echo-nginx-module
