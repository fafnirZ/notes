# Week 3 lecture

## http and https

- Tcp connection opened with the server
- Bidirectional communication stream

## TLS

- TLS handshake

  - server sends a certificate and the client verifies that the certificate
  - certificate chain
  - OS come loaded with certificate authorities

- Can HTTPS be MITM'd?

  ![](./images/Screen%20Shot%202021-06-18%20at%205.29.55%20pm.png)

- http redirect to https is problematic
  - the http site is still susceptible to MITM

## Session management

![](./images/2.png)

