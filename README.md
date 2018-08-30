# Nginx 1.15.3 with all available 3rd party modules bundle

If you have any nginx module want to list in this bundle, simply submit a pull requests. Add Prerequisite and some description to this file would be appreciate.

Official module list:
https://www.nginx.com/resources/wiki/modules/

All modules which have git repo are added as submodule under modules.

## Exception:
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

## Available Modules:

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
    
### encrypted-session-nginx-module
Encrypt NGINX variables for light-weight session-based authentication

##### Prerequisite:
    --add-dynamic-module=../modules/ngx_devel_kit
    
##### Compile Command:
    --add-dynamic-module=../modules/encrypted-session-nginx-module

### form-input-nginx-module
Parses HTTP POST request bodies and saves results to NGINX variables

##### Prerequisite:
    --add-dynamic-module=../modules/ngx_devel_kit
    
##### Compile Command:
    --add-dynamic-module=../modules/form-input-nginx-module
    
### headers-more-nginx-module
Set and clear input and output headers... more than “add”!

##### Compile Command:
    --add-dynamic-module=../modules/headers-more-nginx-module
    
### iconv-nginx-module
Converts character encodings

##### Prerequisite:
    --add-dynamic-module=../modules/ngx_devel_kit

##### Compile Command:
    --add-dynamic-module=../modules/iconv-nginx-module
    
### lua-nginx-module
Embed the power of Lua into NGINX HTTP servers (OpenResty Official)

##### Compile Command:
    --add-dynamic-module=../modules/lua-nginx-module
   
### memc-nginx-module
Extension of the standard memcached module

##### Compile Command:
    --add-dynamic-module=../modules/memc-nginx-module
   
### ModSecurity-nginx
Web application firewall

##### Prerequisite:
    cd ModSecurity
    git submodule init
    git submodule update
    ./build.sh
    ./configure
    make
    make install

##### Compile Command:
    --add-dynamic-module=../modules/ModSecurity-nginx

### mod_zip
Assemble ZIP archives on the fly

##### Compile Command:
    --add-dynamic-module=../modules/mod_zip
    
### naxsi
Web Application Firewall for NGINX

##### Compile Command:
    --add-dynamic-module=../modules/naxsi/naxsi_src
    
### nchan
Pubsub server for Websockets, Long-Poll, EventSource etc.

##### Compile Command:
    --add-dynamic-module=../modules/nchan
    
### nginx_accept_language_module
Accept-Language header parser

##### Compile Command:
    --add-dynamic-module=../modules/nginx_accept_language_module
    


****

## Complex Requirements (compile not test)

### incubator-pagespeed-ngx
Rewrites webpages and associated assets to reduce latency and bandwidth

##### Prerequisite:
    You need to separately download the pagespeed library:
    $ cd ../modules/incubator-pagespeed-ngx
    $ wget In a release this file would contain the URL to download the pre-compiled PSOL binary, but on development branches (like this one) you have to build PSOL from source yourself.  See:
    https://github.com/apache/incubator-pagespeed-ngx/wiki/Building-PSOL-From-Source
    $ tar -xzvf  # expands to psol/
    
    Or see the installation instructions:
    https://developers.google.com/speed/pagespeed/module/build_ngx_pagespeed_from_source

##### Compile Command:
    --add-dynamic-module=../modules/incubator-pagespeed-ngx
    
### mod_rrd_graph
This module provides an HTTP interface to RRDtool’s graphing facilities

##### Prerequisite:
    ngx_rrd_graph requires RRDtool 1.3 or later.
    
##### Compile Command:
    --add-dynamic-module=../modules/mod_rrd_graph
    
### nginx_circle_gif
Generates simple circle images with colors/size specified in the URL

##### Prerequisite:
    Prerequisite: the Circle GIF addon requires the ImageMagick library.
    
##### Compile Command:
    --add-dynamic-module=../modules/nginx_circle_gif
    
****

## Unable to compile

### healthcheck_nginx_upstreams
Health check HTTP servers inside an upstream

##### Compile Command:
    --add-dynamic-module=../modules/healthcheck_nginx_upstreams
    
##### First Compile Error:
    ../modules/healthcheck_nginx_upstreams/ngx_http_healthcheck_module.c: In function ‘ngx_http_healthcheck_mark_finished’:
    ../modules/healthcheck_nginx_upstreams/ngx_http_healthcheck_module.c:308:44: error: ‘ngx_http_upstream_srv_conf_t {aka struct ngx_http_upstream_srv_conf_s}’ has no member named ‘health_failcount’
    
### ip2location-nginx
Identifies the country name/code of an IP address

##### Compile Command:
    --add-dynamic-module=../modules/ip2location-nginx
    
##### First Compile Error:
    ../modules/ip2location-nginx/ngx_http_ip2location_module.c:9:63: fatal error: ../ip2location-c-7.0.0/libIP2Location/IP2Location.h: No such file or directory
    
### ipscrub
Anonymizes IP addresses for logging

##### Compile Command:
    --add-dynamic-module=../modules/ipscrub/ipscrub
    
##### First Compile Error:
    ../modules/ipscrub/ipscrub/src/ngx_ipscrub_support.c:9:24: fatal error: bsd/stdlib.h: No such file or directory
    
### limit_upload_rate
Limit the transmission rate of request body from a client

##### Compile Command:
    --add-dynamic-module=../modules/limit_upload_rate
    
##### First Compile Error:
    ../modules/limit_upload_rate/ngx_http_limit_upload_module.c:116:8: error: unknown type name ‘ngx_http_input_body_filter_pt’
   
### lua-upstream-nginx-module
Make Nginx http upstream configurations scriptable by Lua

##### Compile Command:
    --add-dynamic-module=../modules/lua-upstream-nginx-module
    
##### First Compile Error:
    ../modules/lua-upstream-nginx-module/src/ngx_http_lua_upstream_module.c:15:21: fatal error: lauxlib.h: No such file or directory
    
### modjpeg-nginx
Add overlays and logos to JPEGs on-the-fly without degrading the quality

##### Compile Command:
    --add-dynamic-module=../modules/modjpeg-nginx
    
##### First Compile Error:
    ../modules/modjpeg-nginx/ngx_http_jpeg_filter_module.c:77:24: fatal error: libmodjpeg.h: No such file or directory
    
### nginx-audio-track-for-hls-module
Generate audio track for HTTP Live Streaming (HLS) streams on the fly

##### Prerequisite:
    libavcodec-dev libavformat-dev

##### Compile Command:
    --add-dynamic-module=../modules/nginx-audio-track-for-hls-module
    
##### First Compile Error:
    ../modules/nginx-audio-track-for-hls-module/ngx_http_aac_module.c: In function ‘ngx_http_aac_extract_audio’:
    ../modules/nginx-audio-track-for-hls-module/ngx_http_aac_module.c:210:5: error: ‘avcodec_copy_context’ is deprecated [-Werror=deprecated-declarations]
    
### nginx-auth-ldap
LDAP module which supports authentication against multiple LDAP servers

##### Compile Command:
    --add-dynamic-module=../modules/nginx-auth-ldap

##### First Compile Error:
    ../modules/nginx-auth-ldap/ngx_http_auth_ldap_module.c:33:18: fatal error: ldap.h: No such file or directory
    
### nginx-backtrace
A NGINX module to dump backtrace case a worker process exits abnormally

##### Compile Command:
    --add-dynamic-module=../modules/nginx-backtrace
    
##### First Compile Error:
    ../modules/nginx-backtrace/ngx_backtrace_module.c: In function ‘ngx_backtrace_files’:
    ../modules/nginx-backtrace/ngx_backtrace_module.c:187:11: error: implicit declaration of function ‘ngx_log_create’ [-Werror=implicit-function-declaration]
    
### nginx-c-function
It is a NGINX module that allow you to link your .so(c/c++) application

##### Compile Command:
    --add-dynamic-module=../modules/nginx-c-function
    
##### First Compile Error:
    ngx_http_c_func_module.h not found in your system c header path, please copy latest ngx_http_c_func_module.h to your /usr/include or /usr/local/include or relavent header search path with read and write permission given.
    e.g install -m 644 ../nginx-c-function/src/ngx_http_c_func_module.h /usr/local/include/
    
