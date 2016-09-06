blesta-nginx
============

Nginx Configurations for Blesta v3

Note: This site specific configuration file can also be placed in ```/etc/nginx/conf.d/*.conf```. This way you don't have to deal with symbolic links.

I try to keep the TLS/SSL configuration updated with the most recent security findings. If someone notices a security parameter, please submit a pull request.


### Forward Secrecy & Diffie Hellman Ephemeral Parameters

Generate your own Diffie-Hellman key with a higher bit.
```
cd /etc/ssl/certs
openssl dhparam -out dhparam.pem 4096
chmod 600 dhparam.pem
```
