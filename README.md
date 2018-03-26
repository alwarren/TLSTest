# Android TLS Test (Kotlin)

#### OkHttp3 and Android API Versions <= 19

Demonstrates TLS failures with OkHttp3 and API Versions <= 19.

Failures occur with the following configuration:

- minSdkVersion 19
- OkHttp3 version 3.10.0

URLs Tested:

- FAIL - https://api.github.com/iammert/nocode/readme
- PASS - https://api.apis.guru/v2/metrics.jsonError

Error:

```
D/OkHttp: <-- HTTP FAILED: javax.net.ssl.SSLHandshakeException: javax.net.ssl.SSLProtocolException: SSL handshake aborted: ssl=0xb8c33eb0: Failure in SSL library, usually a protocol error
D/OkHttp: error:1407742E:SSL routines:SSL23_GET_SERVER_HELLO:tlsv1 alert protocol version (external/openssl/ssl/s23_clnt.c:741 0x8d9d4990:0x00000000)
```