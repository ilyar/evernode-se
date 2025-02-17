# SafeMultisig Wallet

This directory contains SafeMultisig Wallet contract for testing purposes.

In Evernode SE this contract is predeployed at `0:d5f5cfc4b52d2eb1bd9d3a8e51707872c7ce0c174facddd0e06ae5ffd17d2fcd` address 
with one single custodian and its initial balance is about 1 million tokens. 

## Custodian Keys:
* Public: `99c84f920c299b5d80e4fcce2d2054b05466ec9df19532a688c10eb6dd8d6b33`
* Secret: `73b60dc6a5b1d30a56a81ea85e0e453f6957dbfbeefb57325ca9f7be96d3fe1a`
* Seed Phrase: `"fan harsh baby section father problem person void depth already powder chicken"`


## Basic Usage
Method: `submitTransaction`

Sends transaction to the specified address.

Parameters: 
* `dest`: `address` - destination address;
* `value`: `uint128` - amount to send, in nanotokens;
* `bounce`: `bool` - bounce flag of the message;
* `allBalance`: `bool` - if true, all wallet's balance will be sent;
* `payload`: `cell` - payload to send with transaction.

### Using tonos-cli:
```commandline
tonos-cli call 0:d5f5cfc4b52d2eb1bd9d3a8e51707872c7ce0c174facddd0e06ae5ffd17d2fcd \
    submitTransaction '{"dest":"<raw_address>","value":<nanotokens>,"bounce":false,"allBalance":false,"payload":""}' \
    --abi SafeMultisigWallet.abi.json \
    --sign SafeMultisigWallet.keys.json  
```

For more information about `SafeMultisigWallet` contract and `tonos-cli` usage see in 
[documentation](https://docs.ton.dev/86757ecb2/p/94921e-multisignature-wallet-management-in-tonos-cli).

## Files
* ABI: [SafeMultisigWallet.json](SafeMultisigWallet.abi.json)
* Keypair: [SafeMultisigWallet.keys.json](SafeMultisigWallet.keys.json)
* TVC file: [SafeMultisigWallet.tvc](SafeMultisigWallet.tvc)
* Source code: [SafeMultisigWallet.sol](SafeMultisigWallet.sol)