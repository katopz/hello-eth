# Test Smart Contract
Will use MetaCoin example for run tests, aim to learn how we test with `.sol` and `.js`.
Source : https://github.com/katopz/truffle-metacoin-example

```shell
truffle test
```
> Expected
```shell
  TestMetacoin
    ✓ testInitialBalanceUsingDeployedContract (53ms)
    ✓ testInitialBalanceWithNewMetaCoin (50ms)

  Contract: MetaCoin
    ✓ should put 10000 MetaCoin in the first account
    ✓ should call a function that depends on a linked library (64ms)
    ✓ should send coin correctly (154ms)


  5 passing