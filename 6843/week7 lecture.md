# Week 7 Same origin policy



CORS protects against the first scenario but not the second

![image-20210716214211643](./images/26.png)

CORS protects against javascript executed code such as fetch(), but not web forms or script/image tags 

![image-20210716214024962](./images/25.png)

# Cross origin Vs Cross site

- cookies such as HTTP only follows same site rule 
- javascript methods such as fetch follow same origin policy

those two are different

- HttpOnly - allow/deny JS accessing cookie
- Secure - set/send cookie through TLS
- SameSite - send/block cookie to cross-site

![image-20210716203902615](./images/23)

![image-20210716204403550](./images/24.png)



If an attacker has access to a subdomain, they are same site and any strict cookie tags are circumvented, i.e. they can bypass the strict rule since it is a same site request.

- subdomain takeover



## Click Jacking

![image-20210716220259872](./images/27.png)



## HTML injection

![image-20210716221414145](./images/28.png)
