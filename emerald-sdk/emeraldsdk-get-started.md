---
description: >-
  To begin using the Emerald SDK, install the Emerald CLI. The Emerald CLI
  encapsulates all the best Emerald tools for end-to-end DApp development.
---

# Getting Started

## Get Emerald CLI

### Dependencies

* ​[homebrew](https://brew.sh/) \(for macOS users\)
* a node.js version manager
  * ​[nodenv](https://github.com/nodenv/nodenv) & [node-build](https://github.com/nodenv/node-build#readme) or:
  * [nvm](https://github.com/creationix/nvm)

{% hint style="warning" %}
We recommend installing node.js via a node.js version manager. If you have node.js & npm already installed on your operating system, then remove them completely before reinstalling node with a node.js manager. If you have a node manager installed, such as nodenv or nvm, then you can move onto [installing the emerald cli](../emerald-platform/emerald-cli/install.md#installing-emerald-cli).
{% endhint %}

{% tabs %}
{% tab title="MacOS" %}
Install nodenv and node-build using homebrew. 

```text
$ brew install nodenv
$ brew install node-build
```

Confirm nodenv and node-build are installed

```text
$ nodenv -v
nodenv 1.1.2
$ node-build --version
node-build 3.0.18
```

Install _stable_ node version using `nodenv install <version>` and make global using `nodenv global 8.11.1`

```text
$ nodenv install 8.11.1
$ nodenv global 8.11.1
```

Then initialize nodenv.

```text
$ nodenv init
```

You may be prompted to add or append `.bash_profile`

```text
$ nodenv init
# Load nodenv automatically by appending
# the follow to ~/.bash_profile:

eval "$(nodenv init -)"
```

Simply add  `eval "$(nodenv init -)"` to .`bash_profile` or create a `.bash_profile` if one does not exist already. Finally, run `nodenv init` when `.bash_profile` has been appended.

Confirm node directory. `Node` and `NPM` should be ready to use now.

```text
$ which node
/Users/JohnSmith/.nodenv/shims/node
```

{% hint style="success" %}
**Dependencies Installed**

Now that node and npm are installed via a node.js package manager, move onto the [Install](../emerald-platform/emerald-cli/install.md#installing-emerald-cli) of the Emerald CLI.
{% endhint %}
{% endtab %}

{% tab title="Linux" %}
{% hint style="warning" %}
Do not install node.js with `apt-get`on Ubuntu. If you installed node.js with the built in package manager, then remove it 

`sudo apt-get purge nodejs && sudo apt-get autoremove && sudo apt-get autoclean`
{% endhint %}

Installing nvm

```text
$ $ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash 
```

Confirm nvm installation

```text
$ nvm --version
```

Run the following command to increase the amount of inotify watches.

```text
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
```

Install _stable_ node version

```text
$ nvm install 10.11.0
```

Setup node version as the default

```text
$ nvm use 10.11.0
$ nvm alias default 10.11.0
```

Confirm node version

```text
$ node -v
v10.11.0
```

Update npm version

```text
$ npm install -g npm
```

Confirm node version

```text
$ npm -v
6.4.1
```

{% hint style="success" %}
**Dependencies Installed**

Now that node and npm are installed via a node.js package manager, move onto the [Install](../emerald-platform/emerald-cli/install.md#installing-emerald-cli) of the Emerald CLI.
{% endhint %}
{% endtab %}

{% tab title="Windows" %}
Coming soon...

In the mean time Windows users can install & boot Linux on a virtual machine or enable subsystem for Linux/ Unix in Windows Features.
{% endtab %}
{% endtabs %}

### Installing

#### Option 1 \(recommended\)

{% tabs %}
{% tab title="MacOS" %}
Install Emerald CLI

```text
$ brew install libgcrypt
$ npm install -g https://github.com/ETCDEVTeam/emerald.git
```

This process may take a few minutes. When it's done, Emerald will be installed globally. Open a new terminal window and run `emerald -h` to view commands and options.

```text
$ emerald -h

   emerald 0.0.2 

   USAGE

     emerald <command> [options]

   COMMANDS

     new                 Create a new project               
     testrpc             Run testnet for ethereum classic   
     wallet              Boot Emerald Wallet                
     explorer            Boot Explorer                      
     deploy              Deploy solidity to network         
     help <command>      Display help for a specific command

   GLOBAL OPTIONS

     -h, --help         Display help                                      
     -V, --version      Display version                                   
     --no-color         Disable colors                                    
     --quiet            Quiet mode - only displays warn and error messages
     -v, --verbose      Verbose mode - will also output debug messages
```

{% hint style="warning" %}
If emerald commands return nothing, then **nodenv** may simply need to rehash. 

`$ nodenv rehash`
{% endhint %}

Updating Emerald CLI

```text
$ brew upgrade libgcrypt
$ npm install -g https://github.com/ETCDEVTeam/emerald.git
```
{% endtab %}

{% tab title="Linux" %}
Install Emerald CLI

```text
$ npm install -g https://github.com/ETCDEVTeam/emerald.git
```

This process may take a few minutes. When it's done, Emerald will be installed globally. Open a new terminal window and run `emerald -h` to view commands and options.
{% endtab %}
{% endtabs %}



