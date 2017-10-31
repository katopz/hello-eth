# Deploy
```shell
truffle migrate
```
> Expected
```shell
Using network 'development'.

Running migration: 1_initial_migration.js
  Deploying Migrations...
  ... 0x933bca8d758c0089774713537caf65bae03f9703a49ed15f979c2d042b478c27
  Migrations: 0x8dc442794780f058ed0e9a25fdcc9699c28bed6d
Saving successful migration to network...
  ... 0xcf4912e3275c2728f354a29aa3d8c6f695c813812dc9b2a49bd7c3ec85cde7d7
Saving artifacts...
Running migration: 2_deploy_contracts.js
  Deploying ConvertLib...
  ... 0x58ba6b79c75a4d3937c4f07618c60e63cd79143be82b1af6c5101474d44c8f3f
  ConvertLib: 0x409b83d44d00a755051242fe473b2d7893d99bdf
  Linking ConvertLib to MetaCoin
  Deploying MetaCoin...
  ... 0xc14d3023257fb6b1bc2339a5b94deeb3b49798893d73042ccbefe40aefd564ef
  MetaCoin: 0xf36944168273f78ddeb77bb9ef538e31d2b0170b
Saving successful migration to network...
  ... 0x535f370f186a2ab7ef7ae221dec7d61ffd30013b4ab65f53480f55af0391637c
Saving artifacts...
```