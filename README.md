# dss-chain-log

An auth-managed on-chain changelog for the MCD system

[comment]: <> (## Usage)

[comment]: <> (Contract Address: `0xdA0Ab1e0017DEbCd72Be8599041a2aa3bA7e740F`)

[comment]: <> (* [Mainnet]&#40;https://etherscan.io/address/0xda0ab1e0017debcd72be8599041a2aa3ba7e740f#code&#41;)

[comment]: <> (* [Kovan]&#40;https://kovan.etherscan.io/address/0xda0ab1e0017debcd72be8599041a2aa3ba7e740f#code&#41;)

[comment]: <> (* [Goerli]&#40;https://goerli.etherscan.io/address/0xda0ab1e0017debcd72be8599041a2aa3ba7e740f#code&#41;)

[comment]: <> (* [Rinkeby]&#40;https://rinkeby.etherscan.io/address/0xda0ab1e0017debcd72be8599041a2aa3ba7e740f#code&#41;)

[comment]: <> (* [Ropsten]&#40;https://ropsten.etherscan.io/address/0xda0ab1e0017debcd72be8599041a2aa3ba7e740f#code&#41;)

### Public functions

* `list()(bytes32[] memory)`: return all of the keys in the changelog
* `getAddress(bytes32)(address)`: for a given key, return the address
* `count()(uint256)`: return the number of keys in the changelog
* `get(uint256)(bytes32,address)`: return the key and address of an item in the array
* `version()(string)`: Returns a version for the changelog (if set)
* `wards(address)(uint256)`: 0 if address is not a ward, 1 if it is.

### Auth functions

* `rely(address)`/`deny(address)`: add and remove authorization
* `setAddress(bytes32,address)`: add or update a key/address pair
* `removeAddress(bytes32)`: remove a key (warning: this can shuffle the array)
* `setVersion(string memory)`: set the version of the current changelog

## Development

### Requirements

* [Dapptools](https://github.com/dapphub/dapptools)

### Testing

```
$ dapp update
$ make test
```


