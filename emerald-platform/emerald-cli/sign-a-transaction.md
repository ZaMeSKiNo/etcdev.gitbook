# Sign a Transaction

## Sign a Transaction <a id="sign-a-transaction"></a>

## Offline <a id="_offline"></a>

```text
$ emerald transaction \
    0x0e7c045110b8dbf29765047380898919c5cb56f4 \
    0x0e7c045110b8dbf29765047380898919c5cb56f4 \
    0x1000 \
    --gas=0x2100 \
    --nonce=0x10001 \
    < echo "secret passphrase"
```

## Sign and Broadcast <a id="_sign_and_broadcast"></a>

Send transaction for execution through a remote node:

```text
$ emerald transaction \
    0x0e7c045110b8dbf29765047380898919c5cb56f4 \
    0x0e7c045110b8dbf29765047380898919c5cb56f4 \
    0x1000 \
    --gas=0x2100 \
    --upstream=127.0.0.1:8545 \
    < echo "secret passphrase"
```

