# ETC Nodes

## Overview

![](../.gitbook/assets/blockchain-node-overview.png)

A blockchain node is **a machine running an implementation of the blockchain**. Running an Ethereum Classic node allows a user to be part of the Ethereum Classic network enabling a user or AI to:

* Create and sign transactions
* Manage accounts
* Read information from the network
* Mine ETC
* and more...

Running an Ethereum Classic node downloads and syncs the entire blockchain to a machine. This implementation is known as a **Full Node** or **Local Node**. Since running a full node can be process intensive for some machines, users may utilize a third party implementation known as a **Light Node** or **Remote Node**.

{% hint style="info" %}
Interactions performed on the blockchain are done through a node. Many app wallet users don't realize that their wallets submit transactions through a third party node being the wallet app provider or other party.
{% endhint %}

### Why Run Your Own Node

1. **Control YOUR transactions:** Utilizing your own node to perform activity on the Ethereum Classic network ensures you are in control of your activity. Using a third party node can be ideal for some users, but trust third parties at your own risk.
2. **Take Part in the ETC Network:** More independent nodes ensures the security and resilience of the network, as well as increased performance such as, reduced latency.
3. **Developers! Developers! Developers!:** Developers can use nodes to deploy and interact with Smart Contracts for their DApps.

## How To Setup an ETC Node

**Go Ethereum**, commonly known as **Geth** or ****_**Classic**_ **Geth**, is the command line interface for running an Ethereum Classic node.

{% hint style="info" %}
Ethereum ETH and Ethereum Classic ETC both have a Geth implementation. _Classic_ Geth simply emphasizes that we're using Ethereum Classic's Geth implementation.
{% endhint %}

### Dependencies

{% tabs %}
{% tab title="MacOS" %}
#### Dependencies

Install [Homebrew](https://brew.sh/) package manager.

```text
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Check installation of Homebrew.

```text
$ brew -v
```

Install Go programming language by downloading a binary distribution at the [Go Lang.](https://golang.org/) website.

Check installation of Go Lang.

```text
$ go version
```

Install a C compilar \(X Code\).

```text
$ xcode-select --install
```
{% endtab %}
{% endtabs %}

### Install _Classic_ Geth

{% tabs %}
{% tab title="MacOS" %}
**Installing Classic Geth**

Install _Classic_ Geth using Homebrew package manager.

```text
$ brew install ethereumproject/classic/geth
```

Check installation of _Classic_ Geth

```text
$ geth version
```

Update Geth \(if applicable\) 

The Ethereum Classic protocol is always being improved and maintained by the love of the Ethereum Classic developer community. Sometimes bugs are discovered, improvements are made, features are added, etc... To upgrade geth to the latest version simply run:

```text
$ brew upgrade geth
```
{% endtab %}
{% endtabs %}

### Initialize _Classic_ Geth

Running a node downloads and syncs the Ethereum Classic blockchain. When a node is not running, it will download and sync blocks to the current state of the chain.

{% tabs %}
{% tab title="MacOs" %}
Initialize _Classic_ Geth by running `geth` , however consider reading on before running geth.

`--fast` Increase performance to sync at the cost of downloading only block state data.

`--cache=VALUE` Further increase performance by adjusting memory \(megabytes\) allowance of the database. Default is 1024 MB.

```text
$ geth --fast --cache=1024
```

Running Classic Geth downloads and syncs the entire Ethereum Classic blockchain. Geth will return sync status such as:

```text
2018-07-25 22:51:36 Sync       #151305 of  #6031258 36529b08   638/ 517/12 blk/txs/mgas sec  8/25 peers
```

When Geth has synced to the current block height, it will continue to import newest blocks.
{% endtab %}
{% endtabs %}

### Commands and Flags

To view commands and flags run

`$ geth -h` or `$ geth -help` or `$ geth -help`

## Basic Usage

Default Data Directory

`$HOME/Library/EthereumClassic/`

File Structure

By default, geth stores node and blockchain data in parent directory depending on OS:

{% tabs %}
{% tab title="MacOs" %}
`$HOME/Library/EthereumClassic/`
{% endtab %}

{% tab title="Linux" %}
`$HOME/.ethereum-classic/`
{% endtab %}

{% tab title="Windows" %}
`$HOME/AppData/Roaming/EthereumClassic/`
{% endtab %}
{% endtabs %}

```text
$ cd Library/EthereumClassic/mainnet/
$ ls
chaindata	indexes		log		nodekey
dapp		keystore	mlogs		nodes
```

You can specify the **parent directory** with `--data-dir=$HOME/id/rather/put/it/here`.

Within the **parent directory**, `EthereumClassic/`, geth uses a **sub directory** for each network run on the node. The defaults are:

* /mainnet: for mainnet or main Ethereum Classic network
* /morden: for the morden testnet

You can specify a subdirectory ****with `--chain=mycustomnet`.

{% hint style="info" %}
**Migrating**: If you have existing data created prior to the [3.4 Release](https://github.com/ethereumproject/go-ethereum/releases), geth will attempt to migrate your existing standard ETC data to this structure. To learn more about managing this migration please read our [3.4 release notes on our Releases page](https://github.com/ethereumproject/go-ethereum/wiki/Release-3.4.0-Notes).
{% endhint %}

Run a Full Node by initializing `geth`.

```text
$ geth
```

For faster download and sync

```text
$ geth --fast --cache=<VALYE IN MEGABYTES DEFAULT 1024>
```

If your machine has more memory available, don't be shy to increase `--cache=VALUE`.  This significantly increases download and sync of the blockchain.

### Create and Manage Accounts

Geth is able to create, import, update, unlock, and otherwise manage your private \(encrypted\) key files. Key files are in JSON format and, by default, stored in the respective chain folder's `/keystore` directory; you can specify a custom location with the `--keystore` flag.

```text
$ geth account new
```

This command will create a new account and prompt you to enter a passphrase to protect your account.

Other `account` subcommands include:

```text
SUBCOMMANDS:

        list    print account addresses
        new     create a new account
        update  update an existing account
        import  import a private key into a new account

```

Learn more at the [Accounts Wiki Page](https://github.com/ethereumproject/go-ethereum/wiki/Managing-Accounts). If you're interested in using geth to manage a lot \(~100,000+\) of accounts, please visit the [Indexing Accounts Wiki page](https://github.com/ethereumproject/go-ethereum/wiki/Indexing-Accounts).

#### Interact with the Javascript console

```text
$ geth console
```

This command will start up Geth's built-in interactive [JavaScript console](https://github.com/ethereumproject/go-ethereum/wiki/JavaScript-Console), through which you can invoke all official [`web3`methods](https://github.com/ethereumproject/wiki/wiki/JavaScript-API) as well as Geth's own [management APIs](https://github.com/ethereumproject/go-ethereum/wiki/Management-APIs). This too is optional and if you leave it out you can always attach to an already running Geth instance with `geth attach`.

Learn more at the [Javascript Console Wiki page](https://github.com/ethereumproject/go-ethereum/wiki/JavaScript-Console).

#### And so much more!

For a comprehensive list of command line options, please consult our [CLI Wiki page](https://github.com/ethereumproject/go-ethereum/wiki/Command-Line-Options).



