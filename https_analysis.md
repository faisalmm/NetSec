## Check Ciphers on HTTP
Use nmap's enumeration script

```BASH
nmap -sV --script ssl-enum-ciphers -p 443 10.23.214.16
```

A sample output is below:

```SQL
Starting Nmap 7.80 ( https://nmap.org ) at 2022-01-28 12:04 EST
Nmap scan report for 10.23.214.16
Host is up (0.00038s latency).

PORT    STATE SERVICE   VERSION
443/tcp open  ssl/https webserver
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.1 200 OK
|     Content-Type: text/html; charset=utf-8
|     Content-Length: 667347
|     Connection: close
|     Content-Security-Policy: frame-ancestors none; style-src 'self' blob: http://localhost:* https://localhost:* http://*.cisco.com:* https://*.cisco.com:* 'unsafe-inline'; script-src 'self' blob: http://localhost:* https://localhost:* http://*.cisco.com:* https://*.cisco.com:* 'unsafe-inline' 'unsafe-eval' 'nonce-e76c939a-840e-4d2e-92b5-340d63a3d74e'
|     X-Content-Security-Policy: frame-ancestors none; style-src 'self' blob: http://localhost:* https://localhost:* http://*.cisco.com:* https://*.cisco.com:* 'unsafe-inline'; script-src 'self' blob: http://localhost:* https://localhost:* http://*.cisco.com:* https://*.cisco.com:* 'unsafe-inline' 'unsafe-eval' 'nonce-e76c939a-840e-4d2e-92b5-340d63a3d74e'
|     X-WebKit-CSP: frame-ancestors none; style-src 'self' blob: http://localhost:* https://localhost:
|   GetRequest: 
|     HTTP/1.1 200 OK
|     Content-Type: text/html; charset=utf-8
|     Content-Length: 667347
|     Connection: close
|     Content-Security-Policy: frame-ancestors none; style-src 'self' blob: http://localhost:* https://localhost:* http://*.cisco.com:* https://*.cisco.com:* 'unsafe-inline'; script-src 'self' blob: http://localhost:* https://localhost:* http://*.cisco.com:* https://*.cisco.com:* 'unsafe-inline' 'unsafe-eval' 'nonce-62bc83f4-d79b-427e-8e88-3450f897e216'
|     X-Content-Security-Policy: frame-ancestors none; style-src 'self' blob: http://localhost:* https://localhost:* http://*.cisco.com:* https://*.cisco.com:* 'unsafe-inline'; script-src 'self' blob: http://localhost:* https://localhost:* http://*.cisco.com:* https://*.cisco.com:* 'unsafe-inline' 'unsafe-eval' 'nonce-62bc83f4-d79b-427e-8e88-3450f897e216'
|     X-WebKit-CSP: frame-ancestors none; style-src 'self' blob: http://localhost:* https://localhost:
|   HTTPOptions: 
|     HTTP/1.1 204 No Content
|     Date: Fri, 28 Jan 2022 17:06:35 GMT
|     Connection: close
|     Vary: Origin
|     Access-Control-Allow-Origin: dnax.ecrt.local
|     Access-Control-Allow-Methods: GET,HEAD,PUT,PATCH,POST,DELETE
|     Server: webserver
|     x-request-id: bbeb77c41a4dd11f1412c44614e1ee9f
|     Via: api-gateway
|     Cache-Control: no-store
|     Pragma: no-cache
|     Content-Security-Policy: default-src 'self' 'unsafe-inline' 'unsafe-eval' blob: data:
|     X-Content-Type-Options: nosniff
|     X-XSS-Protection: 1
|     Strict-Transport-Security: max-age=31536000; includeSubDomains
|_    X-Frame-Options: SAMEORIGIN
|_http-server-header: webserver
|_http-trane-info: Problem with XML parsing of /evox/about
| ssl-enum-ciphers: 
|   TLSv1.1: 
|     ciphers: 
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA (secp256r1) - A
|       TLS_RSA_WITH_AES_128_CBC_SHA (rsa 2048) - A
|     compressors: 
|       NULL
|     cipher preference: client
|   TLSv1.2: 
|     ciphers: 
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA (secp256r1) - A
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256 (secp256r1) - A
|       TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 (secp256r1) - A
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384 (secp256r1) - A
|       TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 (secp256r1) - A
|       TLS_RSA_WITH_AES_128_CBC_SHA (rsa 2048) - A
|       TLS_RSA_WITH_AES_128_CBC_SHA256 (rsa 2048) - A
|       TLS_RSA_WITH_AES_128_GCM_SHA256 (rsa 2048) - A
|       TLS_RSA_WITH_AES_256_CBC_SHA256 (rsa 2048) - A
|       TLS_RSA_WITH_AES_256_GCM_SHA384 (rsa 2048) - A
|     compressors: 
|       NULL
|     cipher preference: client
|_  least strength: A
```