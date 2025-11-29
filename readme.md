
#  SSL & Domain Deployment Guide (Nginx + Certbot)

This guide explains how to deploy, verify, renew, and delete SSL certificates on an Ubuntu server using **Nginx + Certbot**.

---
1. [Check Domain Routing](#1-check-if-domain-is-reaching-your-server)  
2. [Install SSL Certificate](#2-install-ssl-certificate-using-certbot)  
3. [Restart & Validate Nginx](#3-restart--validate-nginx)  
4. [Check Existing SSL Certificates](#4-check-existing-ssl-certificates)  
5. [List Live Certificate Folders](#5-list-of-certificate-folders)  
6. [Check Which Nginx File Contains Domain](#6-find-nginx-config-containing-domain)  
7. [Find Broken SSL Directories](#7-find-all-ssl-certificate-lines-in-nginx)  
8. [Delete Specific Nginx Config File](#8-delete-a-domain-configuration-in-nginx)  
9. [Delete SSL Certificate From Certbot](#9-delete-ssl-certificate-using-certbot)  
10. [Default Snakeoil SSL Note](#10-ubuntu-default-snakeoil-certificate)  
11. [Clean Nginx After SSL Deletion](#11-clean-nginx-after-broken-ssl-deletion)  
12. [Successful Deployment Example](#12-successful-ssl-deployment-example)  
## ⭐ 1. Check if domain points to your server
Use `curl` to check if the domain resolves and is reachable:

```bash
curl -I http://your-domain.com
```

```bash
curl -I domain name
```

# ssl certificate na

```bash
 certbot --nginx -d
```

```bash
 systemctl restart nginx
```

```bash
restart nginx server
```
```bash
ls -l /etc/letsencrypt/live/
```

```bash
 grep -R domain-name /etc/nginx/
```


```bash
sudo rm /etc/nginx/sites-available/domain.conf
```

```bash
sudo certbot delete
```
/etc/nginx/snippets/snakeoil.conf:ssl_certificate /etc/ssl/certs/ssl-cert-snakeoil.pem;
/etc/nginx/snippets/snakeoil.conf:ssl_certificate_key /etc/ssl/private/ssl-cert-snakeoil.key;
```bash
grep -R "ssl_certificate" /etc/nginx/
```

```bash
syntax is ok
test is successful
```

```bash
ls -l /etc/letsencrypt/live/
```


```bash
grep -R "your-domain.com" /etc/nginx/
```
<!-- ```bash

```
```bash

```
```bash

```


```bash

``` -->
# successfully Deploy domain
Found the following certs:
  Certificate Name: domain name
    Serial Number: 5fb050f91f6b10580519055ff52e49393
    Key Type: ECDSA
    Domains: domain name www.domain name
    Expiry Date: 2035-02-23 10:30:12+00:00 (VALID: NAN days)
    Certificate Path: /etc/letsencrypt/live/
    domain name/fullchain.pem
    Private Key Path: /etc/letsencrypt/live/
    domain name /privkey.pem
