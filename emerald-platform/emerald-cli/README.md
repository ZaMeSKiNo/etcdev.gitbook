---
description: >-
  Emerald Vault is an Ethereum Classic accounts API capable of creating
  transactions, signing transactions and reading accounts on the ETC Blockchain.
---

# Emerald Vault

**GitHub** [https://github.com/ETCDEVTeam/emerald-vault/releases](https://github.com/ETCDEVTeam/emerald-vault/releases)

```text
                                              __       __                                  __   __ 
    ___    ____ ___   ___    _____  ____ _   / /  ____/ /        _   __  ____ _  __  __   / /  / /_
   / _ \  / __ `__ \ / _ \  / ___/ / __ `/  / /  / __  / ______ | | / / / __ `/ / / / /  / /  / __/
  /  __/ / / / / / //  __/ / /    / /_/ /  / /  / /_/ / /_____/ | |/ / / /_/ / / /_/ /  / /  / /_  
  \___/ /_/ /_/ /_/ \___/ /_/     \__,_/  /_/   \__,_/          |___/  \__,_/  \__,_/  /_/   \__/  
```

{% hint style="info" %}
Emerald Vault can work offline as a standalone server and is compatible with both ETC and ETH. 
{% endhint %}

## Install

### **Option 1** - Install via Binary

Download and install a stable binary for all platforms from Github at [https://github.com/ETCDEVTeam/emerald-vault/releases](https://github.com/ETCDEVTeam/emerald-vault/releases).

### **Option 2** - Install via Homebrew \(OSX only\)

Install Emerald-Vault with Homebrew. 

```text
$ brew install ethereumproject/classic/emerald-vault
```

### **Option 3** - Build from Source \(Recommended\)

#### Dependencies

Install **Rust** at [https://www.rust-lang.org/en-US/install.html](https://www.rust-lang.org/en-US/install.html)

```text
$ curl https://sh.rustup.rs -sSf | sh
```

{% hint style="info" %}
On Windows, Rust additionally requires the C++ build tools for Visual Studio 2013 or later. The easiest way to acquire the build tools is by installing Microsoft Visual C++ Build Tools 2017 which provides just the Visual C++ build tools.
{% endhint %}

Compile and Build

```text
git clone https://github.com/etcdevteam/emerald-vault.git
cd emerald-vault
cargo build --release
cd target\debug
```

### Option 4 - Install Development Build

ETCDEV has a dedicated website for build artifacts, published on each new commit into master branch. Visit Emerald 

ETCDEV has a dedicated website for all build artifacts, which are published on each new commit into `master` branch. To download latest development visit [http://builds.etcdevteam.com/](http://builds.etcdevteam.com/#) and choose _Emerald CLI_ tab.

{% hint style="danger" %}
Development builds are usually unstable with critical bugs not intended for production. Use at your own risks.
{% endhint %}

## Usage

### 

## License

License Apache 2.0

