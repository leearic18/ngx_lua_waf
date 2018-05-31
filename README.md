# ngx_lua_waf

本项目基于： https://github.com/unixhot/waf

在原有的功能上新增了基于域名白名单.

#### WAF部署简要

<pre>
修改Nginx的配置文件，加入以下配置。注意路径，同时WAF日志默认存放在/tmp/日期_waf.log

  lua_shared_dict      limit 50m;
  lua_package_path     "/opt/wd/etc/nginx/lua/waf/?.lua";
  init_by_lua_file     "/opt/wd/etc/nginx/lua/waf/init.lua";
  access_by_lua_file   "/opt/wd/etc/nginx/lua/waf/access.lua";

# nginx –t
# nginx
</pre>

