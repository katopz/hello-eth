## Get account balance
> Predefined `ether` value should show up.
```shell
npm run balance
```
> Expected
```shell
> @ balance /Users/katopz/git/ethereum-docker
> ID=${ID:-0} npm run exec -- 'eth.getBalance( eth.accounts[$ID] )'


> @ exec /Users/katopz/git/ethereum-docker
> npm run geth -- attach ipc://root/.ethereum/devchain/geth.ipc --exec "eth.getBalance( eth.accounts[$ID] )"


> @ geth /Users/katopz/git/ethereum-docker
> docker exec -it $(docker ps -a -q --filter name=ethereumdocker_eth) geth "attach" "ipc://root/.ethereum/devchain/geth.ipc" "--exec" "eth.getBalance( eth.accounts[0] )"

20000000000000000000
```

## Get specified account balance.
You can specified `ID` as index number
```shell
ID=1 npm run balance
```
> Expected
```shell
> @ balance /Users/katopz/git/ethereum-docker
> ID=${ID:-0} npm run exec -- 'eth.getBalance( eth.accounts[$ID] )'


> @ exec /Users/katopz/git/ethereum-docker
> npm run geth -- attach ipc://root/.ethereum/devchain/geth.ipc --exec "eth.getBalance( eth.accounts[$ID] )"


> @ geth /Users/katopz/git/ethereum-docker
> docker exec -it $(docker ps -a -q --filter name=ethereumdocker_eth) geth "attach" "ipc://root/.ethereum/devchain/geth.ipc" "--exec" "eth.getBalance( eth.accounts[1] )"

20000000000000000000
```

## Get all account balances
```shell
npm run balances
```
> Expected
```shell
> @ balances /Users/katopz/git/ethereum-docker
> JS=./src/gethload.js npm run load
> @ load /Users/katopz/git/ethereum-docker
> npm run exec -- 'loadScript("$JS")'
> @ exec /Users/katopz/git/ethereum-docker
> npm run geth -- attach ipc://root/.ethereum/devchain/geth.ipc --exec "loadScript(\"$JS\")"


> @ geth /Users/katopz/git/ethereum-docker
> docker exec -it $(docker ps -a -q --filter name=ethereumdocker_eth) geth "attach" "ipc://root/.ethereum/devchain/geth.ipc" "--exec" "loadScript(\"./src/gethload.js\")"

  eth.accounts[0]:      0x007ccffb7916f37f7aeef05e8096ecfbe55afc2f      balance: 20 ether
  eth.accounts[1]:      0x99429f64cf4d5837620dcc293c1a537d58729b68      balance: 20 ether
  eth.accounts[2]:      0xca247d7425a29c6645fa991f9151f994a830882d      balance: 20 ether
  eth.accounts[3]:      0x794f74c8916310d6a0009bb8a43a5acab59a58ad      balance: 20 ether
  eth.accounts[4]:      0x276ecb88715a503b00d1f15af4c17dc051991667      balance: 20 ether  eth.accounts[5]:      0x83042c0147acce98e35ed9ef52e6dfc5c67ef92e      balance: 20 ether
  eth.accounts[6]:      0x8ab7114ba0f7ca706af69f799588766c8426aa24      balance: 20 ether
  eth.accounts[7]:      0x932d9e95e5d2cac02eebbe6763ab2c7b0a9d6a2f      balance: 20 ether
  eth.accounts[8]:      0x893c3f80d2a0375b3f00f856cf8a6775e4efc26a      balance: 20 ether
  eth.accounts[9]:      0xb1d3073bcc45462a3b0dfe69902cdd12971efec9      balance: 20 ether
  eth.accounts[10]:     0x939e935909918d7043993d60f330bdaa976d196c      balance: 0 ether
  eth.accounts[11]:     0x25faa585de5a10903afeb479089686685bedae82      balance: 0 ether
  Total balance: 200 ether
true
```