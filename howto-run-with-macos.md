# How to run the RVOS in macos (included apple arm M1)

1. Install [homebrew](https://brew.sh)
```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Install [`riscv-gnu-toolchain`](https://github.com/riscv-software-src/homebrew-riscv) by `brew`
```shell
brew install riscv64-elf-gcc riscv64-elf-gdb riscv64-binutils
```

3. Patch the `code/common.mk` file （git diff > apple.patch)
```shell
git apply patches/apple.patch
```

4. Install `qemu` simulator
```shell
brew install qemu
```
