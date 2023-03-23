# FAQ
## How to search favicon?
For favicon > 256KB Hunter only take head 256KB of the favicon
Hunter use md5 hash for all favicons

```
import hashlib
def favicon_hash(favicon_path):
        print(hashlib.md5(open(favicon_path,'rb').read()).hexdigest())
```
