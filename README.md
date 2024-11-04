# Toolchain bug reproduction

Zed does not detect nix toolchains when started from the Dock

Steps to reproduce

1. Install nix:

```sh
sh <(curl -L https://nixos.org/nix/install)
```

2. Install and configure `direnv` and `nix-direnv`. [GitHub](https://github.com/nix-community/nix-direnv)

3. Clone and `cd` to the repo:

```sh
git clone https://github.com/WeetHet/zed-toolchains-bug-reproduction.git
cd zed-toolchains-bug-reproduction
```

4. Allow direnv:

```sh
direnv allow
```

5. Open `zed` from the terminal to see that the toolchain is detected:

```sh
zed . --foreground
```

6. Open zed from the Dock, open the cloned directory, notice that the toolchain is not detected
