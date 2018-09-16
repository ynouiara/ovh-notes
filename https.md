# HTTPS 

## Certificate

Depending on the offer you've susscribed you may have to generate a SSL certificate for your website from your OVH Web console. 
It is free, OVH is using [Let's Encrypt](https://letsencrypt.org/). 

## HTTPS (and its pitfall)

Source : [Avoid the common pitfalls of making your website secure with SSL](https://docs.ovh.com/gb/en/hosting/avoid_the_common_pitfalls_of_making_your_website_secure_with_ssl/)

### HTTP redirection to HTTPS

To be sure you'll always use HTTP over TLS (formally HTTPS), consider to redirect all requests on your HTTP port to the matching HTTPS URL.
If your website is using Apache, the redirection can be achieved through the .htaccess at the root level of your website.

```
RewriteEngine On
RewriteCond %{SERVER_PORT} 80
RewriteRule ^(.*)$ https://www.votredomaine.fr/$1 [R,L]
```

### Mixed content

Please Refer to [What Is Mixed Content?](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content) and remember as website developer you 
have the responsability to fix Mix Content issues.
