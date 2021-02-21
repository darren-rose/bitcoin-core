# bitcoin core

run bitcoin core using docker


#### run locally

```
docker run --rm -v $(PWD)/bitcoin.conf:/conf/bitcoin.conf -v $(PWD)/data:/data --name bitcoind -p 8333:8333 -p 8332:8332  ruimarinho/bitcoin-core -conf=/conf/bitcoin.conf
```


