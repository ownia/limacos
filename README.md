# limacos
Linux kernel built natively on macOS

### how to build

```
git clone https://github.com/ownia/limacos.git
cd limacos
git submodule update --init --progress
./limacos build
```

### run with qemu-system-aarch64

```
./limacos run
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
| v6.9-rc3 | fec50db7033ea478773b159e0e2efb135270e3b7 |
| v6.10    | 0c3836482481200ead7b416ca80c68a29cfdaabd |
| v6.11    | 98f7e32f20d28ec452afb208f9cffc08448a2652 |
| v6.12    | adc218676eef25575469234709c2d87185ca223a |
| v6.13    | ffd294d346d185b70e28b1a28abe367bbfe53c04 |
| v6.14    | 38fec10eb60d687e30c8c6b5420d86e8149f7557 |
| v6.15    | 0ff41df1cb268fc69e703a08a57ee14ae967d0ca |


### tested devices

| chip                                | macOS            |
|-------------------------------------|------------------|
| Apple M1                            | Sonoma 14.4 Beta |
| Apple M2 Pro                        | Sonoma 14.5      |
| GitHub-hosted runners macos-14 (M1) | Sonoma 14        |


### update linux kernel tags

```
git submodule update --init --progress --depth=1
git -C linux fetch --progress --depth=1 origin refs/tags/<tag>:refs/tags/<tag>
git -C linux checkout <tag>
```

