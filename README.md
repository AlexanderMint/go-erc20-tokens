ERC20
=====

This is a package for the ERC20 ABI (Application Binary Interface) for Ethereum
tokens.

Usage
-----

```go
client, err := ethclient.Dial("...")

tokenAddress := common.HexToAddress("0x845faaA428F26fFf45f759851B76FA66D5fAe4df")
instance, err := token.NewToken(tokenAddress, client)

name, err := instance.Name(&bind.CallOpts{})

symbol, err := instance.Symbol(&bind.CallOpts{})

decimals, err := instance.Decimals(&bind.CallOpts{})
```

This is just an example, but there's a bunch of methods to an ERC20 token.

Resources
---------

I found the following resource helpful:
- https://goethereumbook.org/smart-contract-read/
- https://github.com/miguelmota/ethereum-development-with-go-book
- https://github.com/miguelmota/ethereum-development-with-go-book/tree/master/code/contracts_erc20