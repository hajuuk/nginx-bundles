# Nginx 1.15.3 with all available modules bundle

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
