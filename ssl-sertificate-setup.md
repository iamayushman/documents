
```sh 
nohup yarn dev -H 0.0.0.0 > output.log 2>&1 &
```

# enable https

http://dm-cloud.eastus.cloudapp.azure.com/


```sh
sudo certbot --apache
```

## then access at
https://dm-cloud.eastus.cloudapp.azure.com/


```sh
sudo nano /etc/apache2/sites-available/000-default-le-ssl.conf
```

```htaccess
<IfModule mod_ssl.c>
<VirtualHost *:443>

    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/html

    <Directory /var/www/html>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined

    ServerName dm-cloud.eastus.cloudapp.azure.com
    Include /etc/letsencrypt/options-ssl-apache.conf
    SSLCertificateFile /etc/letsencrypt/live/dm-cloud.eastus.cloudapp.azure.com/fullchain.pem
    SSLCertificateKeyFile /etc/letsencrypt/live/dm-cloud.eastus.cloudapp.azure.com/privkey.pem


    # Allow WebSocket connections
    ProxyPass /gateway/websocket ws://10.0.0.4:8765/websocket
    ProxyPassReverse /gateway/websocket ws://10.0.0.4:8765/websocket

    # Reverse proxy for /gateway to localhost:8765
    ProxyPass /gateway http://10.0.0.4:8765
    ProxyPassReverse /gateway http://10.0.0.4:8765

    # Reverse proxy for /eureka to localhost:8761
    ProxyPass /discovery http://localhost:8761/
    ProxyPassReverse /discovery http://localhost:8761/
    ProxyPass /eureka http://localhost:8761/eureka
    ProxyPassReverse /eureka http://localhost:8761/eureka

</VirtualHost>
</IfModule>
```

# create `/var/www/html/.htaccess`

```htaccess
<IfModule mod_rewrite.c>
   RewriteEngine On
   RewriteBase /

   RewriteCond %{REQUEST_URI} !^/gateway/ [NC]
   RewriteCond %{REQUEST_URI} !^/discovery/ [NC]
   RewriteCond %{REQUEST_URI} !^/eureka/ [NC]
   RewriteCond %{REQUEST_URI} !^/login/oauth2/* [NC]

   RewriteRule ^index\.html$ - [L]
   RewriteCond %{REQUEST_FILENAME} !-f
   RewriteCond %{REQUEST_FILENAME} !-d
   RewriteRule . /index.html [L]

</IfModule>

```

# logs of services

```sh
pm2 log auth-service --lines 400
```
