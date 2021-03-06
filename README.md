certbot-zerossl
===============

This repository contains a wrapper script that makes it easier to use certbot
with the ZeroSSL ACME server

Installation
------------

1. Install the operating system packages for `curl` and `certbot` 
2. Install the ZeroSSL certbot wrapper script
   1. Quick: 
      1. run `bash <(curl -s https://https://certbot.zerossl.com/install)`
      2. Done!
   2. Careful: 
      1. Run `curl -s https://certbot.zerossl.com/install > get-certbot.sh`
      2. Inspect the file to see that it does what it is supposed to do
      3. Run `source get-certbot.sh`
      
Usage
-----

To use the ZeroSSL ACME server instead of running `certbot` run `certbot-zerossl`.

### Examples

```bash
sudo certbot-zerossl certonly --standalone -m anton@example.com -d mydomain.example.com
```

```bash
sudo certbot-zerossl --apache -m barbara@example.com -d myotherdomain.example.com
```

```bash
sudo certbot-zerossl --apache -d mythirddomain.example.com --zerossl-api-key 1234567890abcdef1234567890abcdef
```

