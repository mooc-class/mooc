## nginx 配置样例

#### 阿里云配置样例（放在server区域里面）
```
listen 443 ssl;
ssl_certificate /path/www.weiyum.cn.pem;
ssl_certificate_key /path/www.weiyum.cn.key;
ssl_session_timeout 5m;
ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
ssl_ciphers ALL:!ADH:!EXPORT56:RC4+RSA:+HIGH:+MEDIUM:+LOW:+SSLv2:+EXP;
ssl_prefer_server_ciphers on;
```

#### Let's Encrypt配置样例（放在server区域里面）
```
listen 443 ssl;
ssl_certificate /path/fullchain.cer;
ssl_certificate_key /path/www.weiyum.cn.key;
ssl_session_timeout 5m;
ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
ssl_ciphers ECDHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES128-GCM-SHA256:DHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-SHA384:ECDHE-RSA-AES128-SHA256:ECDHE-RSA-AES256-SHA:ECDHE-RSA-AES128-SHA:DHE-RSA-AES256-SHA:DHE-RSA-AES128-SHA;
ssl_session_cache shared:SSL:50m;
```