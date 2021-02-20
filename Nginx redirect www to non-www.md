---
created: 2021-02-17T13:24:09.554Z
modified: 2021-02-17T13:24:48.006Z
---
#backend    #nginx

```nginx
server {
  listen 0.0.0.0:80;
  listen [::]:80;
  server_name www.example.com;
  return 301 $scheme://example.com$request_uri;
}
```