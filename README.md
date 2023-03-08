# Create Selfsigned certificate

1. Create close key 

``` bash
openssl genrsa -out rootCA.key 2048
```

2. Create ROOT certificate
``` bash
openssl req -x509 -new -nodes -key rootCA.key -sha256 -days 1024 -out rootCA.pem
```

3. run ./create-cert.sh with our domain name
``` bash
./create-cert.sh mydomain.com
```

mydomain.com.crt - our ssl_certificate
device.key - our ssl_certificate_key


