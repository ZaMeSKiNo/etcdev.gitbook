# Usage

## Usage <a id="usage"></a>

Usage help description is based on [clap](https://clap.rs/). Use `-h | --help` for help menu:

```text
$ emerald --help

emerald
Command-line interface for Emerald platform

USAGE:
    emerald [FLAGS] [OPTIONS] [SUBCOMMAND]

FLAGS:
    -h, --help       Prints help information
    -v               Sets the level of verbosity
    -V, --version    Display version

OPTIONS:
    -p, --base-path <base-path>    Set path for chain storage
    -c, --chain <chain>            Sets a chain name [default: mainnet]

SUBCOMMANDS:
    account        Account related commands
    balance        Request account's balance from ethereum node through RPC
    help           Prints this message or the help of the given subcommand(s)
    mnemonic       Create mnemonic phrase according to BIP39 spec
    server         Start local RPC server
    transaction    Transaction related commands
```

Use `-h | --help` for subcommand help menu:

```text
$ emerald account --help

emerald-account
Account related commands

USAGE:
    emerald account [SUBCOMMAND]

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

SUBCOMMANDS:
    export    Export keyfile(s) from keystore
    help      Prints this message or the help of the given subcommand(s)
    hide      Hide selected account from being listed
    import    Import keyfile(s) into storage
    list      List account from `Keyfile` storage
    new       Create new account
    strip     Extract private key from a keyfile
    unhide    Unhide selected account from being listed
    update    Update `name` and `description` for selected account
```

### Environment variables <a id="_environment_variables"></a>

Environment variables allow you to redefine the default settings:

* `EMERALD_HOST` - RPC server listen host
* `EMERALD_PORT` - RPC server listen port
* `EMERALD_CHAIN` - chain name \(`mainnet` \| `morden`\), has a higher priority relative to `EMERALD_CHAIN_ID`
* `EMERALD_CHAIN_ID` - chain id number, has a lower priority relative to `EMERALD_CHAIN`
* `EMERALD_GAS` - maximum gas limit to use by transaction
* `EMERALD_GAS_PRICE` - gas cost to use by transaction \(in Gwei\)
* `EMERALD_SECURITY_LEVEL` - security level \(`normal` \| `high` \| `ultra`\)
* `EMERALD_NODE` - url to upstream node. Used for sign and send of transactions

### Output details level <a id="_output_details_level"></a>

Use `-v` flag to manipulate verbosity

## emerld -v <a id="_emerld_v"></a>

Will set verbose level to 1 - only info messages.

## emerald -vv <a id="_emerald_vv"></a>

Will set verbose level to 2 - info and debug messages.

