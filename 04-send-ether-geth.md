# Send ether
## Send 1 ether from account 0 to account 1
```shell
# From personal account 0
TO=1 VALUE=1 npm run _send

# Or from any account
FROM=0 TO=1 VALUE=1 npm run send
```

> Expected
```shell
> @ send /Users/katopz/git/ethereum-docker
> npm run exec -- 'eth.sendTransaction({from:eth.accounts[$FROM], to:eth.accounts[$TO], value: web3.toWei($AMOUNT, "ether")})'


> @ exec /Users/katopz/git/ethereum-docker
> npm run geth -- attach ipc://root/.ethereum/devchain/geth.ipc --exec "eth.sendTransaction({from:eth.accounts[$FROM], to:eth.accounts[$TO], value: web3.toWei($VALUE, \"ether\")})"


> @ geth /Users/katopz/git/ethereum-docker
> docker exec -it $(docker ps -a -q --filter name=ethereumdocker_eth) geth "attach" "ipc://root/.ethereum/devchain/geth.ipc" "--exec" "eth.sendTransaction({from:eth.accounts[0], to:eth.accounts[1], value: web3.toWei(1, \"ether\")})"

"0x8b3891e6c1d6c7318200de6f7a026afe3b9883b128cec056fa70e385ef71d768"
```