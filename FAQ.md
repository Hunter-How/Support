# FAQ

# Favicon Related 
### 1.How to generate a favicon hash?
For favicon > 256KB Hunter only take head 256KB of the favicon
Hunter use md5 hash for all favicons
Favicon md5's generating mechanism:
```
import hashlib
def favicon_hash(favicon_path):
        print(hashlib.md5(open(favicon_path,'rb').read()).hexdigest())
```
### 2. How to search with favicon?
There are two methods you could try out through hunter platfom:
* Use query favicon-hash="md5 value" to search for internet services that uses this favicon
* Click on the favicon button on your result list, we will search on that target favicon hash straught away which reduce the trouble of md5 conversion
Here is the example: 
<img width="653" alt="Screen Shot 2023-03-29 at 17 05 13" src="https://user-images.githubusercontent.com/112148057/228484818-11f23c1b-d7c3-4c55-8182-8af860881460.png">
<img width="666" alt="Screen Shot 2023-03-29 at 17 06 53" src="https://user-images.githubusercontent.com/112148057/228484819-6912b61d-a6c5-45a7-b248-c355153aa730.png">

### 3. What is related favicon?
Hunter will recommend similar favicons to your retrieved favicon results
This recommendation is 


# Domain Related 
## 1. How can I search for subdomains of a given domain?

domain.suffix="google.com"

[https://hunter.how/list?searchValue=domain.suffix%3D%22google.com%22&timestamp=1679566378561](domain.suffix="google.com")

## 2. How to exclude a domain, web title etc what should i write?

Not equal to: "!=" 
Not exactly equal to: "!==" 

domain="google.com"&&domain.suffix!=="google.com"

https://hunter.how/list?searchValue=domain%3D%22google.com%22%26%26domain.suffix%21%3D%3D%22google.com%22

web.title="Login"&&web.title!="Webmail"

https://hunter.how/list?searchValue=web.title%3D%22Login%22%26%26web.title%21%3D%22Webmail%22
