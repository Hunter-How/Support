# FAQ

## 1. How to search favicon?

For favicon > 256KB Hunter only take head 256KB of the favicon
Hunter use md5 hash for all favicons

```
import hashlib
def favicon_hash(favicon_path):
        print(hashlib.md5(open(favicon_path,'rb').read()).hexdigest())
```

## 2. How can I search for subdomains of a given domain?

domain.suffix="google.com"

[https://hunter.how/list?searchValue=domain.suffix%3D%22google.com%22&timestamp=1679566378561](domain.suffix="google.com")

## 3. How to exclude a domain, web title etc what should i write?

Not equal to: "!=" 
Not exactly equal to: "!==" 

domain="google.com"&&domain.suffix!=="google.com"

https://hunter.how/list?searchValue=domain%3D%22google.com%22%26%26domain.suffix%21%3D%3D%22google.com%22

web.title="Login"&&web.title!="Webmail"

https://hunter.how/list?searchValue=web.title%3D%22Login%22%26%26web.title%21%3D%22Webmail%22
