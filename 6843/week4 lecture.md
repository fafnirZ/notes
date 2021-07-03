# Server side attacks



Probing for vulnerabilities

![Screen Shot 2021-06-24 at 2.05.21 pm](./images/11.png)

think like the developer, how would I implement e.g. the query table

first thing to do when I deploy database, rename default information.schema 



## Blind SQLi

exfiltrate data using function primitives

- functions and can use if statements and functions like sleep
  - time based blind sqli



![Screen Shot 2021-06-24 at 4.26.19 pm](./images/12.png)



## Local file inclusion

- getting `/etc/passwd` of server?

## Cmd injection

![Screen Shot 2021-06-24 at 7.46.08 pm](./images/13)



## Sqli tells

- error messages
- boolean based
- comments
- time based

![Screen Shot 2021-06-27 at 12.08.46 am](./images/14.png)

![Screen Shot 2021-06-27 at 12.43.08 am](./images/15.png)

- using injecting subqueries

- using sql functions

  - `Chr(), cast(), concat(), xpcmdshell()`

- fingerprinting the DBMS

  - `@@version, version(), sqlite_version()`

  

blind sql payload example

`' or (select (subset((select password from users where sid='s5000009'), 1,1) = 'a')-- )`

## NOSQL injections

### Template injection

![Screen Shot 2021-06-27 at 1.45.32 am](./images/1.png)



injecting a object payload

- `{"$exists":true}`



### SSTI (server side template injection)

example payload for RCE

`{{ "".__class__.__mro__[1].subclasses__()[444](["cat","/etc/passwd"],stdout=-1).communicate }}`



### Business logic exploitation

- challenging assumptions of developer
- edge cases
- overwriting some files

