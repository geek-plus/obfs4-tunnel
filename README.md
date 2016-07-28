# obfs4-tunnel

It's a fork of https://github.com/Yawning/obfs4

To start your server:

```
env TOR_PT_MANAGED_TRANSPORT_VER=1 TOR_PT_STATE_LOCATION=/tmp TOR_PT_SERVER_TRANSPORTS=obfs4 TOR_PT_SERVER_BINDADDR=obfs4-0.0.0.0:1231 TOR_PT_ORPORT=127.0.0.1:1080 obfs4proxy
```

Output:

```
VERSION 1
SMETHOD obfs4 [::]:1231 ARGS:cert=gtgDd0S7Xy0vMjHbJ4ceORtmDnSV9FYrV2plA9rAWdj9iHHamIi7w3K0kODKkW9H2ygaVQ,iat-mode=0
SMETHODS DONE
```

To start your client:

```
env TOR_PT_CERT=gtgDd0S7Xy0vMjHbJ4ceORtmDnSV9FYrV2plA9rAWdj9iHHamIi7w3K0kODKkW9H2ygaVQ TOR_PT_TARGET=127.0.0.1:1231 TOR_PT_MANAGED_TRANSPORT_VER=1 TOR_PT_STATE_LOCATION=/tmp TOR_PT_CLIENT_TRANSPORTS=obfs4 obfs4proxy -unsafeLogging -enableLogging
```
