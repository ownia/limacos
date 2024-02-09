# limacos
Linux kernel built natively on macOS

### how to build

```
git clone https://github.com/ownia/limacos.git
cd limacos
git submodule update --init
source build.sh
```

### dependencies

```
brew tap messense/macos-cross-toolchains
brew install aarch64-unknown-linux-gnu
brew install openssl
```

### available version

| tags     | commit                                   |
|----------|------------------------------------------|
| v6.8-rc3 | 54be6c6c5ae8e0d93a6c4641cb7528eb0b6ba478 |


### tested devices

| chip         | macOS            |
|--------------|------------------|
| Apple M1     | Sonoma 14.4 Beta |
| Apple M2 Pro | Sonoma 14.0      |
