Shared Libraries
================

> **Note:** This library is not actively maintained and the documentation below may not accurately reflect the current implementation. Symbol names in the code may differ from those described here. Use this library with caution.

## litemoneyconsensus

The purpose of this library is to make the verification functionality that is critical to Litemoney's consensus available to other applications, e.g. to language bindings.

### API

The interface is defined in the C header `litemoneyconsensus.h` located in  `src/script/litemoneyconsensus.h`.

#### Version

`litemoneyconsensus_version` returns an `unsigned int` with the API version *(currently at an experimental `0`)*.

#### Script Validation

`litemoneyconsensus_verify_script` returns an `int` with the status of the verification. It will be `1` if the input script correctly spends the previous output `scriptPubKey`.

##### Parameters
- `const unsigned char *scriptPubKey` - The previous output script that encumbers spending.
- `unsigned int scriptPubKeyLen` - The number of bytes for the `scriptPubKey`.
- `const unsigned char *txTo` - The transaction with the input that is spending the previous output.
- `unsigned int txToLen` - The number of bytes for the `txTo`.
- `unsigned int nIn` - The index of the input in `txTo` that spends the `scriptPubKey`.
- `unsigned int flags` - The script validation flags *(see below)*.
- `litemoneyconsensus_error* err` - Will have the error/success code for the operation *(see below)*.

##### Script Flags
- `litemoneyconsensus_SCRIPT_FLAGS_VERIFY_NONE`
- `litemoneyconsensus_SCRIPT_FLAGS_VERIFY_P2SH` - Evaluate P2SH ([BIP16](https://github.com/bitcoin/bips/blob/master/bip-0016.mediawiki)) subscripts.
- `litemoneyconsensus_SCRIPT_FLAGS_VERIFY_DERSIG` - Enforce strict DER ([BIP66](https://github.com/bitcoin/bips/blob/master/bip-0066.mediawiki)) compliance.
- `litemoneyconsensus_SCRIPT_FLAGS_VERIFY_NULLDUMMY` - Enforce NULLDUMMY ([BIP147](https://github.com/bitcoin/bips/blob/master/bip-0147.mediawiki)).
- `litemoneyconsensus_SCRIPT_FLAGS_VERIFY_CHECKLOCKTIMEVERIFY` - Enable CHECKLOCKTIMEVERIFY ([BIP65](https://github.com/bitcoin/bips/blob/master/bip-0065.mediawiki)).
- `litemoneyconsensus_SCRIPT_FLAGS_VERIFY_CHECKSEQUENCEVERIFY` - Enable CHECKSEQUENCEVERIFY ([BIP112](https://github.com/bitcoin/bips/blob/master/bip-0112.mediawiki)).
- `litemoneyconsensus_SCRIPT_FLAGS_VERIFY_WITNESS` - Enable WITNESS ([BIP141](https://github.com/bitcoin/bips/blob/master/bip-0141.mediawiki)).

##### Errors
- `litemoneyconsensus_ERR_OK` - No errors with input parameters *(see the return value of `litemoneyconsensus_verify_script` for the verification status)*.
- `litemoneyconsensus_ERR_TX_INDEX` - An invalid index for `txTo`.
- `litemoneyconsensus_ERR_TX_SIZE_MISMATCH` - `txToLen` did not match with the size of `txTo`.
- `litemoneyconsensus_ERR_DESERIALIZE` - An error deserializing `txTo`.
- `litemoneyconsensus_ERR_AMOUNT_REQUIRED` - Returned by `litemoneyconsensus_verify_script` when `VERIFY_WITNESS` is set; use `litemoneyconsensus_verify_script_with_amount` for witness validation.

### Example Implementation
- No known Litemoney-specific third-party binding examples are currently listed here.
