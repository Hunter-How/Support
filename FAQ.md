# FAQ
<a href="#general">General</a> •
<a href="#subscription-and-payment">Subscription and payment</a> •
<a href="#favicon-search">Favicon Search</a> •
<a href="#domain-related">Domain Related</a> •
<a href="#my-watchlist-related">My watchlist Related</a> •


## General

### 1. Do I have to register before the search?
We do recommend users log in with a Google account, this service ensures the security of user passwords and user privacy.
However, you could still explore our site without signing in.

### 2. Why is there no corresponding search result for the IP/domain/port/etc. I search for?
Please browse the returned error message or switch the date filter. Hunter displays our data results for the past month by default.
If you still can't find satisfactory results, please feel free to comment on our GitHub space.

### 3. How frequently does hunter.how scans the internet?
Hunter scans the internet without having a uniform frequency, we prioritize our scanning tasks regarding port usage. 
Hunter scans commonly used ports of global IP within 30 days. Other less-used ports at a less frequent pace

### 4. Why is the login page unresponsive?
Our login service uses Google accounts to verify identity. You need to ensure that your IP is in an area that supports Google identity verification services.

## Subscription and payment
### 1. Can I pay with my credit card?
Currently, all payments need to go through the Paypal channel, Paypal accepts major credit cards and debit cards.
If you are still facing any payment issues please contact us through **[Email](hunter.how00@gmail.com)**

### 2. How long does it take for a subscription to be activated after a successful payment？
After your successful payment, hunter.how will send a successful subscription message and the validity period to the email address associated with your Google account.

### 3. Can I repurchase a subscription plan when my data quota is used up within 30 days?
A single subscription plan only supports a single purchase within 30 days. If you need a higher data quota, please upgrade your current subscription plan or contact our sales team to customize an exclusive data quota for you.


## Favicon Search

### 1. How to generate a favicon hash?
For favicon > 256KB Hunter only takes head 256KB of the favicon
Hunter uses md5 hash for all favicons
Favicon md5's generating mechanism:
```
import hashlib
def favicon_hash(favicon_path):
        print(hashlib.md5(open(favicon_path,'rb').read()).hexdigest())
```
### 2. How to search with Favicon?
There are two methods you could try out through Hunter platform:
* Use query favicon_hash="md5 value" to search for internet services that use this favicon
* Click on the favicon button on your result list, and we will search on that target favicon hash straight away which reduces the trouble of md5 conversion
Here is an example: 
<img width="653" alt="Screen Shot 2023-03-29 at 17 05 13" src="https://user-images.githubusercontent.com/112148057/228484818-11f23c1b-d7c3-4c55-8182-8af860881460.png">
<img width="666" alt="Screen Shot 2023-03-29 at 17 06 53" src="https://user-images.githubusercontent.com/112148057/228484819-6912b61d-a6c5-45a7-b248-c355153aa730.png">

### 3. What is a related favicon?
Hunter will recommend similar favicons to your favicon query results. These favicons are commonly hard to differentiate with eyes.
This recommendation is based on the appearance of the favicon you have searched, our algorithm will be based on your input favicon appearance to provide you with more possible results.

 <img src="images/favicon.png" img style="width:40%;"> 


## Domain Related 

### 1. How can I search for subdomains of a given domain?

domain.suffix="google.com"

[https://hunter.how/list?searchValue=domain.suffix%3D%22google.com%22&timestamp=1679566378561](domain.suffix="google.com")

### 2. How do I exclude a domain, web title, etc what should I write?

Not equal to: "!=" 
Not exactly equal to: "!==" 

domain="google.com"&&domain.suffix!=="google.com"

https://hunter.how/list?searchValue=domain%3D%22google.com%22%26%26domain.suffix%21%3D%3D%22google.com%22

web.title="Login"&&web.title!="Webmail"

https://hunter.how/list?searchValue=web.title%3D%22Login%22%26%26web.title%21%3D%22Webmail%22


## My Watchlist Related 

### 1. Why can’t I receive new port monitoring alerts?
Alert messages will be sent to the email address bound to your Google account. Please make sure your email inbox is not full.
If you have not logged in to your account for a long time, your monitoring tasks will be suspended.


