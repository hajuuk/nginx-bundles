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

[SmallLight](https://github.com/cubicdaiya/ngx_small_light "Dynamic Image Transformation Module For NGINX")

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

<!-- TOC -->

- [Nginx 1.15.3 with all available 3rd party modules bundle](#nginx-1153-with-all-available-3rd-party-modules-bundle)
    - [Exception:](#exception)
- [Available Modules:](#available-modules)
    - [array-var-nginx-module](#array-var-nginx-module)
    - [drizzle-nginx-module](#drizzle-nginx-module)
    - [echo-nginx-module](#echo-nginx-module)
    - [encrypted-session-nginx-module](#encrypted-session-nginx-module)
    - [form-input-nginx-module](#form-input-nginx-module)
    - [headers-more-nginx-module](#headers-more-nginx-module)
    - [iconv-nginx-module](#iconv-nginx-module)
    - [lua-nginx-module](#lua-nginx-module)
    - [memc-nginx-module](#memc-nginx-module)
    - [ModSecurity-nginx](#modsecurity-nginx)
    - [mod_zip](#mod_zip)
    - [naxsi](#naxsi)
    - [nchan](#nchan)
    - [nginx_accept_language_module](#nginx_accept_language_module)
    - [nginx-clojure](#nginx-clojure)
    - [nginx_cookie_flag_module](#nginx_cookie_flag_module)
    - [nginx-dynamic-etags](#nginx-dynamic-etags)
    - [nginx-elastic-client](#nginx-elastic-client)
    - [nginx-eval-module](#nginx-eval-module)
    - [NginxExecute](#nginxexecute)
    - [nginx-http-auth-digest](#nginx-http-auth-digest)
    - [nginx-http-concat](#nginx-http-concat)
    - [nginx-http-footer-filter](#nginx-http-footer-filter)
    - [nginx-http-rdns](#nginx-http-rdns)
    - [nginx-http-shibboleth](#nginx-http-shibboleth)
    - [nginx-http-slice](#nginx-http-slice)
    - [nginx-http-user-agent](#nginx-http-user-agent)
    - [nginx-ip-blocker](#nginx-ip-blocker)
    - [nginx_md5_filter](#nginx_md5_filter)
    - [nginx-module-sysguard](#nginx-module-sysguard)
    - [nginx-module-url](#nginx-module-url)
    - [nginx-module-vts](#nginx-module-vts)
    - [nginx-openssl-version](#nginx-openssl-version)
    - [nginx-push-stream-module](#nginx-push-stream-module)
    - [nginx-rtmp-module](#nginx-rtmp-module)
    - [nginx-rtmpt-proxy-module](#nginx-rtmpt-proxy-module)
    - [nginx-sorted-querystring-module](#nginx-sorted-querystring-module)
    - [nginx-upload-module](#nginx-upload-module)
    - [nginx-upload-progress-module](#nginx-upload-progress-module)
    - [nginx-upstream-fair](#nginx-upstream-fair)
    - [nginx-upsync-module](#nginx-upsync-module)
    - [nginx-vod-module](#nginx-vod-module)
    - [ngx_auto_lib](#ngx_auto_lib)
    - [ngx_aws_auth](#ngx_aws_auth)
    - [ngx_brotli](#ngx_brotli)
    - [ngx_cache_purge](#ngx_cache_purge)
    - [ngx_devel_kit](#ngx_devel_kit)
    - [ngx-fancyindex](#ngx-fancyindex)
    - [ngx_http_consistent_hash](#ngx_http_consistent_hash)
    - [ngx_http_dyups_module](#ngx_http_dyups_module)
    - [ngx_http_enhanced_memcached_module](#ngx_http_enhanced_memcached_module)
    - [ngx_http_footer_if_filter](#ngx_http_footer_if_filter)
    - [ngx_http_geoip2_module](#ngx_http_geoip2_module)
    - [ngx_http_internal_redirect](#ngx_http_internal_redirect)
    - [ngx_http_lower_upper_case](#ngx_http_lower_upper_case)
    - [ngx_http_php_memcache_standard_balancer](#ngx_http_php_memcache_standard_balancer)
    - [ngx_http_php_session](#ngx_http_php_session)
    - [ngx_http_subrange_module](#ngx_http_subrange_module)
    - [ngx_http_substitutions_filter_module](#ngx_http_substitutions_filter_module)
    - [ngx_http_types_filter](#ngx_http_types_filter)
    - [ngx_http_upstream_ketama_chash](#ngx_http_upstream_ketama_chash)
    - [ngx_log_if](#ngx_log_if)
    - [ngx_upstream_jdomain](#ngx_upstream_jdomain)
    - [rds-csv-nginx-module](#rds-csv-nginx-module)
    - [rds-json-nginx-module](#rds-json-nginx-module)
    - [redis2-nginx-module](#redis2-nginx-module)
    - [set-misc-nginx-module](#set-misc-nginx-module)
    - [sphinx2-nginx-module](#sphinx2-nginx-module)
    - [srcache-nginx-module](#srcache-nginx-module)
    - [stream-lua-nginx-module](#stream-lua-nginx-module)
    - [testcookie-nginx-module](#testcookie-nginx-module)
    - [xss-nginx-module](#xss-nginx-module)
    - [nginx-auth-ldap](#nginx-auth-ldap)
    - [nginx-c-function](#nginx-c-function)
    - [nginx-clojure-embed](#nginx-clojure-embed)
    - [nginx-haskell-module](#nginx-haskell-module)
    - [nginx-module-sts](#nginx-module-sts)
    - [ipscrub](#ipscrub)
    - [nginx-stream-upsync-module](#nginx-stream-upsync-module)
    - [nginx-unzip-module](#nginx-unzip-module)
    - [nginx_upstream_module](#nginx_upstream_module)
    - [nginx-video-thumbextractor-module](#nginx-video-thumbextractor-module)
    - [ngx_dynamic_limit_req_module](#ngx_dynamic_limit_req_module)
    - [ngx_form_auth](#ngx_form_auth)
    - [ngx_http_auth_pam_module](#ngx_http_auth_pam_module)
    - [ngx_http_secure_download](#ngx_http_secure_download)
    - [sass-nginx-module](#sass-nginx-module)
    - [spnego-http-auth-nginx-module](#spnego-http-auth-nginx-module)
- [Complex Requirements (compile not test)](#complex-requirements-compile-not-test)
    - [incubator-pagespeed-ngx](#incubator-pagespeed-ngx)
    - [mod_rrd_graph](#mod_rrd_graph)
    - [nginx_circle_gif](#nginx_circle_gif)
    - [nginx-log-zmq](#nginx-log-zmq)
    - [ngx_http_js_module](#ngx_http_js_module)
    - [ngx-stomp](#ngx-stomp)
- [Unable to compile](#unable-to-compile)
    - [healthcheck_nginx_upstreams](#healthcheck_nginx_upstreams)
    - [ip2location-nginx](#ip2location-nginx)
    - [limit_upload_rate](#limit_upload_rate)
    - [lua-upstream-nginx-module](#lua-upstream-nginx-module)
    - [modjpeg-nginx](#modjpeg-nginx)
    - [nginx-audio-track-for-hls-module](#nginx-audio-track-for-hls-module)
    - [nginx-backtrace](#nginx-backtrace)
    - [nginx-ey-balancer](#nginx-ey-balancer)
    - [nginx-gridfs](#nginx-gridfs)
    - [nginx-limit-upstream](#nginx-limit-upstream)
    - [nginx_lua_module](#nginx_lua_module)
    - [nginx_mod_akamai_g2o](#nginx_mod_akamai_g2o)
    - [nginx-notice](#nginx-notice)
    - [nginx_ocsp_proxy-module](#nginx_ocsp_proxy-module)
    - [nginx-selective-cache-purge-module](#nginx-selective-cache-purge-module)
    - [nginx-static-etags](#nginx-static-etags)
    - [nginx-statsd](#nginx-statsd)
    - [nginx-sticky-module-ng](#nginx-sticky-module-ng)
    - [nginx_tcp_proxy_module](#nginx_tcp_proxy_module)
    - [ngx_http_set_hash](#ngx_http_set_hash)
    - [ngx_mongo](#ngx_mongo)
    - [ngx_php](#ngx_php)
    - [ngx_sssd_info](#ngx_sssd_info)
    - [ngx_webp](#ngx_webp)
    - [replace-filter-nginx-module](#replace-filter-nginx-module)
    - [set-cconv-nginx-module](#set-cconv-nginx-module)
    - [socks-nginx-module](#socks-nginx-module)
    - [stream-echo-nginx-module (trying)](#stream-echo-nginx-module-trying)
    - [summarizer-nginx-module](#summarizer-nginx-module)
    - [traffic-accounting-nginx-module](#traffic-accounting-nginx-module)

<!-- /TOC -->

****

# Available Modules:

## array-var-nginx-module
Add support for array variables to NGINX config files

### Prerequisite:
    --add-dynamic-module=../modules/ngx_devel_kit

### Compile Command:
    --add-dynamic-module=../modules/array-var-nginx-module

## drizzle-nginx-module
Make NGINX talk directly to MySQL or Drizzle database servers

### Prerequisite:
    libdrizzle

### Compile Command:
    --add-dynamic-module=../modules/drizzle-nginx-module
    
## echo-nginx-module
Provides familiar shell-style commands to NGINX HTTP servers

### Compile Command:
    --add-dynamic-module=../modules/echo-nginx-module
    
## encrypted-session-nginx-module
Encrypt NGINX variables for light-weight session-based authentication

### Prerequisite:
    --add-dynamic-module=../modules/ngx_devel_kit
    
### Compile Command:
    --add-dynamic-module=../modules/encrypted-session-nginx-module

## form-input-nginx-module
Parses HTTP POST request bodies and saves results to NGINX variables

### Prerequisite:
    --add-dynamic-module=../modules/ngx_devel_kit
    
### Compile Command:
    --add-dynamic-module=../modules/form-input-nginx-module
    
## headers-more-nginx-module
Set and clear input and output headers... more than “add”!

### Compile Command:
    --add-dynamic-module=../modules/headers-more-nginx-module
    
## iconv-nginx-module
Converts character encodings

### Prerequisite:
    --add-dynamic-module=../modules/ngx_devel_kit

### Compile Command:
    --add-dynamic-module=../modules/iconv-nginx-module
    
## lua-nginx-module
Embed the power of Lua into NGINX HTTP servers (OpenResty Official)

### Compile Command:
    --add-dynamic-module=../modules/lua-nginx-module
   
## memc-nginx-module
Extension of the standard memcached module

### Compile Command:
    --add-dynamic-module=../modules/memc-nginx-module
   
## ModSecurity-nginx
Web application firewall

### Prerequisite:
    cd ModSecurity
    git submodule init
    git submodule update
    ./build.sh
    ./configure
    make
    make install

### Compile Command:
    --add-dynamic-module=../modules/ModSecurity-nginx

## mod_zip
Assemble ZIP archives on the fly

### Compile Command:
    --add-dynamic-module=../modules/mod_zip
    
## naxsi
Web Application Firewall for NGINX

### Compile Command:
    --add-dynamic-module=../modules/naxsi/naxsi_src
    
## nchan
Pubsub server for Websockets, Long-Poll, EventSource etc.

### Compile Command:
    --add-dynamic-module=../modules/nchan
    
## nginx_accept_language_module
Accept-Language header parser

### Compile Command:
    --add-dynamic-module=../modules/nginx_accept_language_module
    
## nginx-clojure
A module for embedding Clojure, Java, and Groovy programs

### Prerequisite:
    Java

### Compile Command:
    --add-dynamic-module=../modules/nginx-clojure/src/c
   
## nginx_cookie_flag_module
Set the flags “HttpOnly”, “secure” and “SameSite” for cookies

### Compile Command:
    --add-dynamic-module=../modules/nginx_cookie_flag_module
    
## nginx-dynamic-etags
NGINX module for etags on dynamic content

### Compile Command:
    --add-dynamic-module=../modules/nginx-dynamic-etags
    
## nginx-elastic-client
Elasticsearch client in nginx proxy for multiple elasticsearch server

### Compile Command:
    --add-dynamic-module=../modules/nginx-elastic-client
    
## nginx-eval-module
Captures arbitrary subrequests’ responses into custom NGINX variables

### Compile Command:
    --add-dynamic-module=../modules/nginx-eval-module
    
## NginxExecute
Commands remotely and return results

### Compile Command:
    --add-dynamic-module=../modules/NginxExecute

## nginx-http-auth-digest
HTTP Digest Authentication

### Compile Command:
    --add-dynamic-module=../modules/nginx-http-auth-digest
    
## nginx-http-concat
Concatenates files in a given context

### Compile Command:
    --add-dynamic-module=../modules/nginx-http-concat
    
## nginx-http-footer-filter
Implements a body filter that adds a given string to the page footer

### Compile Command:
    --add-dynamic-module=../modules/nginx-http-footer-filter
    
## nginx-http-rdns
Makes a reverse DNS lookup and provides control of incoming hostname

### Compile Command:
    --add-dynamic-module=../modules/nginx-http-rdns
    
## nginx-http-shibboleth
Perform authorization based on subrequest to Shibboleth FastCGI app

### Compile Command:
    --add-dynamic-module=../modules/nginx-http-shibboleth
    
## nginx-http-slice
NGINX module for serving a file in slices (reverse byte-range)

### Compile Command:
    --add-dynamic-module=../modules/nginx-http-slice
    
## nginx-http-user-agent
A more powerful module than the native BrowserModule

### Compile Command:
    --add-dynamic-module=../modules/nginx-http-user-agent
    
## nginx-ip-blocker
An efficient shared memory IP blocking system for nginx.

### Compile Command:
    --add-dynamic-module=../modules/nginx-ip-blocker

## nginx_md5_filter
Returns the MD5 sum of content that would’ve otherwise been served

### Compile Command:
    --add-dynamic-module=../modules/nginx_md5_filter

## nginx-module-sysguard
A module to protect the system against too high load

### Compile Command:
    --add-dynamic-module=../modules/nginx-module-sysguard

## nginx-module-url
A module to convert uri to user-defined encoding

### Compile Command:
    --add-dynamic-module=../modules/nginx-module-url

## nginx-module-vts
A virtual host and upstream traffic status module

### Compile Command:
    --add-dynamic-module=../modules/nginx-module-vts

## nginx-openssl-version
OpenSSL minimum version constraints in configuration

### Compile Command:
    --add-dynamic-module=../modules/nginx-openssl-version

## nginx-push-stream-module
Turns NGINX into an adept stream HTTP Push server

### Compile Command:
    --add-dynamic-module=../modules/nginx-push-stream-module

## nginx-rtmp-module
RTMP protocol support. Live streaming and video on demand

### Compile Command:
    --add-dynamic-module=../modules/nginx-rtmp-module

## nginx-rtmpt-proxy-module
Proxy RTMP packages using stadard HTTP requests

### Compile Command:
    --add-dynamic-module=../modules/nginx-rtmpt-proxy-module

## nginx-sorted-querystring-module
Expose a variable with the parameters ordered to be used as a cache_key

### Compile Command:
    --add-dynamic-module=../modules/nginx-sorted-querystring-module

## nginx-upload-module
Handles file uploads using multipart/form-data encoding (RFC 1867)

### Compile Command:
    --add-dynamic-module=../modules/nginx-upload-module

## nginx-upload-progress-module
Tracks and reports upload progress

### Compile Command:
    --add-dynamic-module=../modules/nginx-upload-progress-module

## nginx-upstream-fair
Distributes incoming requests to least-busy servers

### Compile Command:
    --add-dynamic-module=../modules/nginx-upstream-fair

## nginx-upsync-module
Syncing upstreams from etcd or consul, needn’t reload nginx(HTTP Module)

### Compile Command:
    --add-dynamic-module=../modules/nginx-upsync-module

## nginx-vod-module
Repackage MP4 files for streaming in HLS, HDS, MSS and DASH

### Compile Command:
    --add-dynamic-module=../modules/nginx-vod-module

## ngx_auto_lib
Reuse pre-compiled/installed versions of OpenSSL, PCRE and Zlib

### Compile Command:
    --add-dynamic-module=../modules/ngx_auto_lib

## ngx_aws_auth
Generate security headers for GET requests to Amazon S3

### Compile Command:
    --add-dynamic-module=../modules/ngx_aws_auth

## ngx_brotli
Serves dynamically or statically compressed responses with brotli

### Prerequisite:
    Please make sure that the git submodule has been checked out:
    cd ../modules/ngx_brotli && git submodule update --init && cd /home/hajuuk/nginx-bundles/nginx

### Compile Command:
    --add-dynamic-module=../modules/ngx_brotli

## ngx_cache_purge
Adds ability to purge content from FastCGI, proxy, and uWSGI caches

### Compile Command:
    --add-dynamic-module=../modules/ngx_cache_purge

## ngx_devel_kit
An extension to the core functionality of NGINX

### Compile Command:
    --add-dynamic-module=../modules/ngx_devel_kit

## ngx-fancyindex
Like the built-in autoindex module, but fancier

### Compile Command:
    --add-dynamic-module=../modules/ngx-fancyindex

## ngx_http_consistent_hash
Select backend based on Consistent hash ring

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_consistent_hash

## ngx_http_dyups_module
Update upstreams’ config by restful interface

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_dyups_module

## ngx_http_enhanced_memcached_module
Repackaging of the standard memcached module to add features

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_enhanced_memcached_module

## ngx_http_footer_if_filter
Applies a footer if a response meets a specified condition

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_footer_if_filter

## ngx_http_geoip2_module
City and country code lookups via the MaxMind GeoIP2 API

### Prerequisite:
    libmaxminddb-dev

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_geoip2_module

## ngx_http_internal_redirect
A NGINX module for internal redirection

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_internal_redirect

## ngx_http_lower_upper_case
Provides upper/lowercase string functions in NGINX config files

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_lower_upper_case

## ngx_http_php_memcache_standard_balancer
Load balancer that imitates the PHP-Memcache standard hash’s behaviour

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_php_memcache_standard_balancer

## ngx_http_php_session
Extract values that are stored in a serialized PHP session

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_php_session

## ngx_http_subrange_module
Split one big HTTP/Range request to multiple subrange requesets

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_subrange_module

## ngx_http_substitutions_filter_module
Performs regular expression and string substitutions on response bodies

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_substitutions_filter_module

## ngx_http_types_filter
Changes the Content-Type output header on specified conditions

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_types_filter

## ngx_http_upstream_ketama_chash
Provides upstream load distribution by hashing a configurable variable

### Compile Command:
    --add-dynamic-module=../modules/ngx_http_upstream_ketama_chash

## ngx_log_if
Log the requests only when given conditions are met

### Compile Command:
    --add-dynamic-module=../modules/ngx_log_if

## ngx_upstream_jdomain
An asynchronous domain name resolve module for NGINX upstream

### Compile Command:
    --add-dynamic-module=../modules/ngx_upstream_jdomain

## rds-csv-nginx-module
Helps ngx_drizzle, ngx_postgres, and others emit Comma-Separated Values

### Compile Command:
    --add-dynamic-module=../modules/rds-csv-nginx-module

## rds-json-nginx-module
Helps ngx_drizzle, ngx_postgres, and others emit JSON data

### Compile Command:
    --add-dynamic-module=../modules/rds-json-nginx-module

## redis2-nginx-module
HTTP Upstream module for the full Redis 2.0 protocol

### Compile Command:
    --add-dynamic-module=../modules/redis2-nginx-module

## set-misc-nginx-module
Various set_xxx directives added to NGINX’s rewrite module

### Prerequisite:
    --add-dynamic-module=../modules/ngx_devel_kit

### Compile Command:
    --add-dynamic-module=../modules/set-misc-nginx-module

## sphinx2-nginx-module
NGINX upstream module for Sphinx 2.x

### Compile Command:
    --add-dynamic-module=../modules/sphinx2-nginx-module

## srcache-nginx-module
Transparent subrequest-based caching layout for NGINX locations

### Compile Command:
    --add-dynamic-module=../modules/srcache-nginx-module

## stream-lua-nginx-module
Embed the power of Lua into NGINX TCP servers (OpenResty Official)

### Prerequisite:
    lua5.1-dev

### Limitation:
    The stream cannot compile dynamically.

### Compile Command:
    --with-stream --add-dynamic-module=../modules/stream-lua-nginx-module

## testcookie-nginx-module
Simple robot (DDoS) mitigation module

### Compile Command:
    --add-dynamic-module=../modules/testcookie-nginx-module

## xss-nginx-module
Native support for cross-site scripting (XSS)

### Compile Command:
    --add-dynamic-module=../modules/xss-nginx-module

## nginx-auth-ldap
LDAP module which supports authentication against multiple LDAP servers

### Prerequisite:
    libldap2-dev

### Compile Command:
    --add-dynamic-module=../modules/nginx-auth-ldap

## nginx-c-function
It is a NGINX module that allow you to link your .so(c/c++) application

### Prerequisite:
    install -m 644 ../modules/nginx-c-function/src/ngx_http_c_func_module.h /usr/local/include/

### Compile Command:
    --add-dynamic-module=../modules/nginx-c-function

## nginx-clojure-embed
A module for embedding Clojure, Java, and Groovy programs

### Prerequisite:
    openjdk-8-jdk-headless
    --add-dynamic-module=../modules/nginx-clojure/src/c

### Compile Command:
    --add-dynamic-module=../modules/nginx-clojure/nginx-clojure-embed/src/c

## nginx-haskell-module
Binding Haskell code in configuration files for great good!

### Prerequisite:
    ghc

### Compile Command:
    --add-dynamic-module=../modules/nginx-haskell-module

## nginx-module-sts
A stream traffic status module

### Prerequisite:
    ---with-stream=dynamic

### Compile Command:
    --add-dynamic-module=../modules/nginx-module-sts

## ipscrub
Anonymizes IP addresses for logging

### Prerequisite:
    libbsd-dev

### Compile Command:
    --add-dynamic-module=../modules/ipscrub/ipscrub

## nginx-stream-upsync-module
Syncing upstreams from etcd or consul, needn’t reload nginx(TCP Module)

### Prerequisite:
    --with-stream=dynamic

### Compile Command:
    --add-dynamic-module=../modules/nginx-stream-upsync-module

## nginx-unzip-module
serve file directly from the archives

### Prerequisite:
    libzip-dev

### Compile Command:
    --add-dynamic-module=../modules/nginx-unzip-module

## nginx_upstream_module
HTTP Upstream module for communicate with Tarantool DB

### Prerequisite:
    libmsgpuck-dev libyajl-dev

### Compile Command:
    --add-module=../modules/nginx_upstream_module

## nginx-video-thumbextractor-module
NGINX module to extract thumbs from a video file

### Prerequisite:
    libavformat-dev libswscale-dev libavfilter-dev

### Compile Command:
    --add-dynamic-module=../modules/nginx-video-thumbextractor-module

## ngx_dynamic_limit_req_module

Dynamic lock IP and release regularly

### Prerequisite:

    libhiredis-dev

### Compile Command:

    --add-dynamic-module=../modules/ngx_dynamic_limit_req_module

## ngx_form_auth

Authentication and authorization via POST request and PAM

### Prerequisite:

	libpam0g-dev

### Compile Command:

    --add-dynamic-module=../modules/ngx_form_auth

## ngx_http_auth_pam_module

HTTP Basic Authentication using PAM

### Prerequisite:

	libpam0g-dev

### Compile Command:

    --add-dynamic-module=../modules/ngx_http_auth_pam_module

## ngx_http_secure_download

Create expiring links

### Prerequisite:

    libmhash-dev

### Compile Command:

    --add-dynamic-module=../modules/ngx_http_secure_download

## sass-nginx-module

Compiles SASS files in NGINX before sending the response

### Prerequisite:

    libsass-dev

### Compile Command:

    --add-dynamic-module=../modules/sass-nginx-module

## spnego-http-auth-nginx-module

Support for SPNEGO/gssapi in NGINX

### Prerequisite:

    libkrb5-dev

### Compile Command:

    --add-dynamic-module=../modules/spnego-http-auth-nginx-module

****

# Complex Requirements (compile not test)

## incubator-pagespeed-ngx
Rewrites webpages and associated assets to reduce latency and bandwidth

### Prerequisite:
    You need to separately download the pagespeed library:
    $ cd ../modules/incubator-pagespeed-ngx
    $ wget In a release this file would contain the URL to download the pre-compiled PSOL binary, but on development branches (like this one) you have to build PSOL from source yourself.  See:
    https://github.com/apache/incubator-pagespeed-ngx/wiki/Building-PSOL-From-Source
    $ tar -xzvf  # expands to psol/
    
    Or see the installation instructions:
    https://developers.google.com/speed/pagespeed/module/build_ngx_pagespeed_from_source

### Compile Command:
    --add-dynamic-module=../modules/incubator-pagespeed-ngx
    
## mod_rrd_graph
This module provides an HTTP interface to RRDtool’s graphing facilities

### Prerequisite:
    ngx_rrd_graph requires RRDtool 1.3 or later.
    
### Compile Command:
    --add-dynamic-module=../modules/mod_rrd_graph
    
## nginx_circle_gif
Generates simple circle images with colors/size specified in the URL

### Prerequisite:
    Prerequisite: the Circle GIF addon requires the ImageMagick library.
    
### Compile Command:
    --add-dynamic-module=../modules/nginx_circle_gif
    
## nginx-log-zmq
Log the requests via ZeroMQ

### Prerequisite:
    libzmq
    
### Compile Command:
    --add-dynamic-module=../modules/nginx-log-zmq

## ngx_http_js_module
Embedding SpiderMonkey, a full port of Perl module, and more

### Prerequisite:
    the ngx_http_js_module addon requires the jsapi headers.
    
### Compile Command:
    --add-dynamic-module=../modules/ngx_http_js_module

## ngx-stomp
A STOMP upstream module on nginx, send http to any AMQ which has stomp

### Prerequisite:

    c-stomp library not found, you need to install c-stomp library via 'https://github.com/Taymindis/c-stomp'

### Compile Command:

    --add-dynamic-module=../modules/ngx-stomp

****

# Unable to compile

## healthcheck_nginx_upstreams

Health check HTTP servers inside an upstream

### Compile Command:

    --add-dynamic-module=../modules/healthcheck_nginx_upstreams

### First Compile Error:

    ../modules/healthcheck_nginx_upstreams/ngx_http_healthcheck_module.c: In function ‘ngx_http_healthcheck_mark_finished’:
    ../modules/healthcheck_nginx_upstreams/ngx_http_healthcheck_module.c:308:44: error: ‘ngx_http_upstream_srv_conf_t {aka struct ngx_http_upstream_srv_conf_s}’ has no member named ‘health_failcount’

## ip2location-nginx

Identifies the country name/code of an IP address

### Compile Command:

    --add-dynamic-module=../modules/ip2location-nginx

### First Compile Error:

    ../modules/ip2location-nginx/ngx_http_ip2location_module.c:9:63: fatal error: ../ip2location-c-7.0.0/libIP2Location/IP2Location.h: No such file or directory

## limit_upload_rate

Limit the transmission rate of request body from a client

### Compile Command:

    --add-dynamic-module=../modules/limit_upload_rate

### First Compile Error:

    ../modules/limit_upload_rate/ngx_http_limit_upload_module.c:116:8: error: unknown type name ‘ngx_http_input_body_filter_pt’

## lua-upstream-nginx-module

Make Nginx http upstream configurations scriptable by Lua

### Compile Command:

    --add-dynamic-module=../modules/lua-upstream-nginx-module

### First Compile Error:

    ../modules/lua-upstream-nginx-module/src/ngx_http_lua_upstream_module.c:15:21: fatal error: lauxlib.h: No such file or directory

## modjpeg-nginx

Add overlays and logos to JPEGs on-the-fly without degrading the quality

### Compile Command:

    --add-dynamic-module=../modules/modjpeg-nginx

### First Compile Error:

    ../modules/modjpeg-nginx/ngx_http_jpeg_filter_module.c:77:24: fatal error: libmodjpeg.h: No such file or directory

## nginx-audio-track-for-hls-module

Generate audio track for HTTP Live Streaming (HLS) streams on the fly

### Prerequisite:

    libavcodec-dev libavformat-dev

### Compile Command:

    --add-dynamic-module=../modules/nginx-audio-track-for-hls-module

### First Compile Error:

    ../modules/nginx-audio-track-for-hls-module/ngx_http_aac_module.c: In function ‘ngx_http_aac_extract_audio’:
    ../modules/nginx-audio-track-for-hls-module/ngx_http_aac_module.c:210:5: error: ‘avcodec_copy_context’ is deprecated [-Werror=deprecated-declarations]

## nginx-backtrace

A NGINX module to dump backtrace case a worker process exits abnormally

### Compile Command:

    --add-dynamic-module=../modules/nginx-backtrace

### First Compile Error:

    ../modules/nginx-backtrace/ngx_backtrace_module.c: In function ‘ngx_backtrace_files’:
    ../modules/nginx-backtrace/ngx_backtrace_module.c:187:11: error: implicit declaration of function ‘ngx_log_create’ [-Werror=implicit-function-declaration]

## nginx-ey-balancer

Provides a request queue for limiting concurrent requests

### Compile Command:

    --add-dynamic-module=../modules/nginx-ey-balancer

### First Compile Error:

    ../modules/nginx-ey-balancer/max_connections_module.c: In function ‘dispatch’:
    ../modules/nginx-ey-balancer/max_connections_module.c:314:3: error: implicit declaration of function ‘ngx_http_upstream_connect’ -Werror=implicit-function-declaration]

## nginx-gridfs

NGINX module for serving files from MongoDB’s GridFS

### Compile Command:

    --add-dynamic-module=../modules/nginx-gridfs

### First Compile Error:

    make[1]: *** No rule to make target '../modules/nginx-gridfs/mongo-c-driver/src/*.h', needed by 'objs/addon/nginx-gridfs/ngx_http_gridfs_module.o'.  Stop.

## nginx-limit-upstream

Limits the maximum connections to each server in a upstream

### Compile Command:

    --add-dynamic-module=../modules/nginx-limit-upstream

### First Compile Error:

    ../modules/nginx-limit-upstream/ngx_http_limit_upstream_module.c: In function ‘ngx_http_limit_upstream_cleanup’:
    ../modules/nginx-limit-upstream/ngx_http_limit_upstream_module.c:372:9: error: implicit declaration of function ‘ngx_http_upstream_connect’ [-Werror=implicit-function-declaration]

## nginx_lua_module

Embed the power of Lua into NGINX

### Compile Command:

    --add-dynamic-module=../modules/nginx_lua_module

### First Compile Error:

    ../modules/nginx_lua_module/src/ngx_http_lua_module.c: In function ‘ngx_http_lua_file_request_handler’:
    ../modules/nginx_lua_module/src/ngx_http_lua_module.c:797:9: error: used struct type value where scalar is required

## nginx_mod_akamai_g2o

Restricts access to content to Akamai edge servers using G2O headers

### Compile Command:

    --add-dynamic-module=../modules/nginx_mod_akamai_g2o

### First Compile Error:

    ../modules/nginx_mod_akamai_g2o/ngx_http_akamai_g2o_module.c: In function ‘base64_signature_of_data’:
    ../modules/nginx_mod_akamai_g2o/ngx_http_akamai_g2o_module.c:341:14: error: storage size of ‘hmac’ isn’t known

## nginx-notice

Serve static file to POST requests

### Compile Command:

    --add-dynamic-module=../modules/nginx-notice

### First Compile Error:

    ../modules/nginx-notice/ngx_http_notice_module.c: In function ‘ngx_http_notice_handler’:
    ../modules/nginx-notice/ngx_http_notice_module.c:156:10: error: implicit declaration of function ‘ngx_http_discard_body’ [-Werror=implicit-function-declaration]

## nginx_ocsp_proxy-module

OCSP processing module designed for response caching

### Compile Command:

    --add-dynamic-module=../modules/nginx_ocsp_proxy-module

### First Compile Error:

    ../modules/nginx_ocsp_proxy-module/src/ngx_http_ocsp_proxy_module.c: In function ‘copy_ocsp_certid’:
    ../modules/nginx_ocsp_proxy-module/src/ngx_http_ocsp_proxy_module.c:401:13: error: dereferencing pointer to incomplete type ‘OCSP_CERTID {aka struct ocsp_cert_id_st}’

## nginx-selective-cache-purge-module

A cache purge module that allows GLOB expressions like .jpg or /test

### Compile Command:

    --add-dynamic-module=../modules/nginx-selective-cache-purge-module

### First Compile Error:

    ../modules/nginx-selective-cache-purge-module/include/ngx_selective_cache_purge_module.h:11:33: fatal error: redis_nginx_adapter.h: No such file or directory

## nginx-static-etags

Generates etags for static content

### Compile Command:

    --add-dynamic-module=../modules/nginx-static-etags

### First Compile Error:

    ../modules/nginx-static-etags/ngx_http_static_etags_module.c: In function ‘ngx_http_static_etags_header_filter’:
    ../modules/nginx-static-etags/ngx_http_static_etags_module.c:113:41: error: variable ‘log’ set but not used [-Werror=unused-but-set-variable]

## nginx-statsd

Adds the ability for NGINX to interacting with Statsd

### Compile Command:

    --add-dynamic-module=../modules/nginx-statsd

### First Compile Error:

    ../modules/nginx-statsd/ngx_http_statsd.c:367: undefined reference to `ngx_udp_connect'

## nginx-sticky-module-ng

Adds an upstream server persistance using cookies

### Compile Command:

    --add-dynamic-module=../modules/nginx-sticky-module-ng

### First Compile Error:

    ../modules/nginx-sticky-module-ng/ngx_http_sticky_misc.c: In function ‘ngx_http_sticky_misc_sha1’:
    ../modules/nginx-sticky-module-ng/ngx_http_sticky_misc.c:176:15: error: ‘SHA_DIGEST_LENGTH’ undeclared (first use in this function)

## nginx_tcp_proxy_module

TCP proxy with NGINX, includes health check and status monitor

### Compile Command:

    --add-dynamic-module=../modules/nginx_tcp_proxy_module

### First Compile Error:

    ../modules/nginx_tcp_proxy_module/ngx_tcp_core_module.c:33:40: error: ‘NGX_CONF_MULTI’ undeclared here (not in a function)

## ngx_http_set_hash

Set a variable to hash functions, including MD5, SHA1 and Murmurhash 2

### Compile Command:

    --add-dynamic-module=../modules/ngx_http_set_hash

### First Compile Error:

    ../modules/ngx_http_set_hash/ngx_http_set_hash_module.c:7:20: fatal error: ndk.h: No such file or directory

## ngx_mongo

Upstream module for direct communication with MongoDB

### Prerequisite:

    libyajl

### Compile Command:

    --add-dynamic-module=../modules/ngx_mongo

### First Compile Error:

    ../modules/ngx_mongo/src/ngx_http_mongo_module.c: In function ‘ngx_http_mongo_create_predefined_request’:
    ../modules/ngx_mongo/src/ngx_http_mongo_module.c:681:28: error: variable ‘mctx’ set but not used [-Werror=unused-but-set-variable]

## ngx_php

Embedded php script language for nginx-module

### Compile Command:

    --add-dynamic-module=../modules/ngx_php

### First Compile Error:

    ../modules/ngx_php/src/php/php_ngx.h:10:17: fatal error: php.h: No such file or directory

## ngx_sssd_info

Retrieves and exposes additional user attributes from SSSD

### Pre:

    libdbus-1-dev

### Compile Command:

    --add-dynamic-module=../modules/ngx_sssd_info

### First Compile Error:

    In file included from ../modules/ngx_sssd_info/ngx_sssd_info.c:5:0:
/usr/include/dbus-1.0/dbus/dbus.h:29:33: fatal error: dbus/dbus-arch-deps.h: No such file or directory

## ngx_webp

Webp wrapper to convert files on the fly

### Compile Command:

    --add-dynamic-module=../modules/ngx_webp

### First Compile Error:

    ../modules/ngx_webp/src/ngx_http_webp_module.c: In function ‘ngx_http_webp_handler’:
    ../modules/ngx_webp/src/ngx_http_webp_module.c:63:11: error: variable ‘parent_pid’ set but not used [-Werror=unused-but-set-variable]

## replace-filter-nginx-module

Performs regular expression substitutions on response bodies

### Compile Command:

    --add-dynamic-module=../modules/replace-filter-nginx-module

### First Compile Error:

    error: ngx_http_replace_filter_module requires agentzh's sregex library.

## set-cconv-nginx-module

Conversion between Simplified and Traditional Chinese at rewrite phase

### Compile Command:

    --add-dynamic-module=../modules/set-cconv-nginx-module

### First Compile Error:

    ../modules/set-cconv-nginx-module/src/ngx_http_set_cconv.c:3:17: fatal error: ndk.h: No such file or directory

## socks-nginx-module

SOCKS5 proxy module for NGINX

### Compile Command:

    --add-dynamic-module=../modules/socks-nginx-module

### First Compile Error:

    ../modules/socks-nginx-module/src/ngx_http_socks_upstream.c: In function ‘ngx_http_socks_upstream_send_response’:
    ../modules/socks-nginx-module/src/ngx_http_socks_upstream.c:2755:45: error: ‘ngx_http_file_cache_t {aka struct ngx_http_file_cache_s}’ has no member named ‘temp_path’; did you mean ‘use_temp_path’?

## stream-echo-nginx-module (trying)

Provides familiar shell-style commands to NGINX stream servers

### Tried:

    --with-stream=dynamic

### Compile Command:

    --add-dynamic-module=../modules/stream-echo-nginx-module

### First Compile Error:

    ../modules/stream-echo-nginx-module/src/ngx_stream_echo_module.c: In function ‘ngx_stream_echo_discarded_request_handler’:
    ../modules/stream-echo-nginx-module/src/ngx_stream_echo_module.c:1146:9: error: implicit declaration of function ‘ngx_stream_close_connection’

## summarizer-nginx-module

An upstream module for Summarizer 1.0

### Compile Command:

    --add-dynamic-module=../modules/summarizer-nginx-module

### First Compile Error:

    ../modules/summarizer-nginx-module/src/ngx_http_summarizer_proto.c:22:21: error: ‘szf’ defined but not used [-Werror=unused-const-variable=]

## traffic-accounting-nginx-module

Realtime traffic and status code monitoring (HTTP + Stream)

### Compile Command:

    --add-dynamic-module=../modules/traffic-accounting-nginx-module

### First Compile Error:

    make: *** No rule to make target 'build', needed by 'default'.  Stop.
