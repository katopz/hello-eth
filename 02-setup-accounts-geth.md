# Setup Accounts

## List accounts with `geth`
This will list all accounts in `dev` by `geth`
```shell
npm run ls-dev
```
> Expected
```
> @ ls-dev /Users/katopz/git/ethereum-docker
> npm run geth -- --dev --datadir /root/.ethereum/devchain account list


> @ geth /Users/katopz/git/ethereum-docker
> docker exec -it $(docker ps -a -q --filter name=ethereumdocker_eth) geth "--dev" "--datadir" "/root/.ethereum/devchain" "account" "list"

Account #0: {007ccffb7916f37f7aeef05e8096ecfbe55afc2f} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-41.334222730Z--007ccffb7916f37f7aeef05e8096ecfbe55afc2f
Account #1: {99429f64cf4d5837620dcc293c1a537d58729b68} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-44.914646739Z--99429f64cf4d5837620dcc293c1a537d58729b68
Account #2: {ca247d7425a29c6645fa991f9151f994a830882d} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-46.400585045Z--ca247d7425a29c6645fa991f9151f994a830882d
Account #3: {794f74c8916310d6a0009bb8a43a5acab59a58ad} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-47.838345060Z--794f74c8916310d6a0009bb8a43a5acab59a58ad
Account #4: {276ecb88715a503b00d1f15af4c17dc051991667} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-49.151752132Z--276ecb88715a503b00d1f15af4c17dc051991667
Account #5: {83042c0147acce98e35ed9ef52e6dfc5c67ef92e} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-50.513483270Z--83042c0147acce98e35ed9ef52e6dfc5c67ef92e
Account #6: {8ab7114ba0f7ca706af69f799588766c8426aa24} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-51.693207415Z--8ab7114ba0f7ca706af69f799588766c8426aa24
Account #7: {932d9e95e5d2cac02eebbe6763ab2c7b0a9d6a2f} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-53.093803426Z--932d9e95e5d2cac02eebbe6763ab2c7b0a9d6a2f
Account #8: {893c3f80d2a0375b3f00f856cf8a6775e4efc26a} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-54.549724060Z--893c3f80d2a0375b3f00f856cf8a6775e4efc26a
Account #9: {b1d3073bcc45462a3b0dfe69902cdd12971efec9} keystore:///root/.ethereum/devchain/keystore/UTC--2016-02-29T14-52-55.760047216Z--b1d3073bcc45462a3b0dfe69902cdd12971efec9
```

## New account with `geth`
You wll ask for `Passphrase:`, do type something you can remember.
```shell
npm run new-dev
```
> Expected
```shell
> @ new-dev /Users/katopz/git/ethereum-docker> npm run geth -- --dev  --datadir /root/.ethereum/devchain account new

> @ geth /Users/katopz/git/ethereum-docker> docker exec -it $(docker ps -a -q --filter name=ethereumdocker_eth) geth "--dev" "--datadir" "/root/.ethereum/devchain" "account" "new"

WARN [10-29|07:32:34] No etherbase set and no accounts found as default
Your new account is locked with a password. Please give a password. Do not forget this password.
Passphrase:
Repeat passphrase:
Address: {939e935909918d7043993d60f330bdaa976d196c}
```
## New account with `geth --exec`
```shell
npm run _new
```
> Expected
```shell
> @ _new /Users/katopz/git/ethereum-docker
> npm run exec -- 'personal.newAccount()'


> @ exec /Users/katopz/git/ethereum-docker
> npm run geth -- attach ipc://root/.ethereum/devchain/geth.ipc --exec "personal.newAccount()"


> @ geth /Users/katopz/git/ethereum-docker
> docker exec -it $(docker ps -a -q --filter name=ethereumdocker_eth) geth "attach" "ipc://root/.ethereum/devchain/geth.ipc" "--exec" "personal.newAccount()"

Passphrase:
Repeat passphrase:
"0x25faa585de5a10903afeb479089686685bedae82"
```

List account with `geth -exec`
```shell
npm run _ls
```
> Expected
```shell
> @ _ls /Users/katopz/git/ethereum-docker
> npm run exec -- personal.listAccounts


> @ exec /Users/katopz/git/ethereum-docker
> npm run geth -- attach ipc://root/.ethereum/devchain/geth.ipc --exec "personal.listAccounts"


> @ geth /Users/katopz/git/ethereum-docker
> docker exec -it $(docker ps -a -q --filter name=ethereumdocker_eth) geth "attach" "ipc://root/.ethereum/devchain/geth.ipc" "--exec" "personal.listAccounts"

["0x007ccffb7916f37f7aeef05e8096ecfbe55afc2f", "0x99429f64cf4d5837620dcc293c1a537d58729b68", "0xca247d7425a29c6645fa991f9151f994a830882d", "0x794f74c8916310d6a0009bb8a43a5acab59a58ad", "0x276ecb88715a503b00d1f15af4c17dc051991667", "0x83042c0147acce98e35ed9ef52e6dfc5c67ef92e", "0x8ab7114ba0f7ca706af69f799588766c8426aa24", "0x932d9e95e5d2cac02eebbe6763ab2c7b0a9d6a2f", "0x893c3f80d2a0375b3f00f856cf8a6775e4efc26a", "0xb1d3073bcc45462a3b0dfe69902cdd12971efec9", "0x939e935909918d7043993d60f330bdaa976d196c", "0x25faa585de5a10903afeb479089686685bedae82"]
```
