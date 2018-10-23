# Install

## Installing Emerald CLI

### Download stable binary <a id="_download_stable_binary"></a>

Binaries for all platforms are currently published at [https://github.com/ETCDEVTeam/emerald-cli/releases](https://github.com/ETCDEVTeam/emerald-cli/releases)

### Install with Homebrew \(OSX only\) <a id="_install_with_homebrew_osx_only"></a>

Installs latest stable binary.

```text
$ brew install ethereumproject/classic/emerald-cli
```

### Download development build <a id="_download_development_build"></a>

| Warning | Development builds are usually unstable and may contain critical issues that can lead to loss of funds. Use it on your risk |
| :--- | :--- |


ETCDEV has a dedicated website for all build artifacts, which are published on each new commit into `master` branch. To download a latest development build, please open [https://builds.etcdevteam.com](https://builds.etcdevteam.com/)and choose _Emerald CLI_ tab

### Build from sources <a id="_build_from_sources"></a>

#### Requirements <a id="_requirements"></a>

Install Rust from [https://www.rust-lang.org/en-US/install.html](https://www.rust-lang.org/en-US/install.html)

Unix one-liner:

```text
$ curl https://sh.rustup.rs -sSf | sh
```

| Note | On Windows, Rust additionally requires the C build tools for Visual Studio 2013 or later. The easiest way to acquire the build tools is by installing Microsoft Visual C Build Tools 2017 which provides just the Visual C++ build tools. |
| :--- | :--- |


#### Compile <a id="_compile"></a>

**Step 1**

Clone the repository

```text
$ git clone https://github.com/etcdevteam/emerald-cli.git
$ cd emerald-cli
```

**Step 2**

Compile with cargo

```text
$ cargo build --release
```

**Step 3**

Run `emerald`

```text
$ ./target/release/emerald --help
```

