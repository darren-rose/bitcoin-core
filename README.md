# bitcoin core

run bitcoin core using docker


#### run node

```
docker run --rm -v $(PWD)/bitcoin.conf:/conf/bitcoin.conf -v $(PWD)/data:/data --name bitcoind -p 8333:8333 -p 8332:8332  coblox/bitcoin-core -conf=/conf/bitcoin.conf
```

#### query getblockchaininfo

```
curl -v --user rpcuser:rpcpass --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getblockchaininfo", "params": []}' -H 'content-type: text/plain;' http://localhost:8332 | jq
```


