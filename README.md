# SNIProxy
#### DNS Server listen on port 53 by utilizing OpenResty, Lua code included in nginx.conf to check redis and record all requests, in proxy server's OpenResty is also check the record in redis and if there was an available TTL for source IP it's proxying it otherwise redirect it back to dns server to get one

##### you may wanna to generate Bind9 zone and its related DB files using webmin, or in VM machines you can also install bind9 through the webmin GUI

##### Why OpenResty instead of nginx?
##### _Embed the power of Lua into Nginx HTTP Server_
##### Why Redis?
##### _redis used to ensure the client/user do not passthrough his request directly to proxy server or bypass the zone config in bind9_
