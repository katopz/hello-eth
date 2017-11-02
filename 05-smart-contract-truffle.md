# Truffle Framework
Build - Run - Test - Deploy

# Setup truffle
```shell
npm install -g truffle
```

# Setup testrpc
```shell
# Install
npm install -g ethereumjs-testrpc

# Run
testrpc
```

# Setup project
```shell
truffle init
```

# Build
```shell
truffle compile --all
```

# Deploy
```shell
truffle migrate --reset
```

# Develop
> This will use `testrpc` inside `truffle` port `9545`
```shell
# To getting in
truffle develop

# To getting out
.exit
```

# Console
```shell
# To getting in
truffle console

# To getting out
.exit
```

# Example
SimpleStorage example with getter/setter and simple test
Source : https://github.com/katopz/truffle-simple-storage-example
