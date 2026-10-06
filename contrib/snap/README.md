# Litemoney Snap Packaging

Commands for building and uploading a Litemoney Core Snap to the Snap Store. Anyone on amd64 (x86_64), arm64 (aarch64), or i386 (i686) should be able to build it themselves with these instructions. This would pull the official Litemoney binaries from the releases page, verify them, and install them on a user's machine.

## Building Locally
```
sudo apt install snapd
sudo snap install --classic snapcraft
sudo snapcraft
```

### Installing Locally
```
snap install \*.snap --devmode
```

### To Upload to the Snap Store
```
snapcraft login
snapcraft register litemoney-core
snapcraft upload \*.snap
sudo snap install litemoney-core
```

### Usage
```
litemoney-unofficial.cli # for litemoney-cli
litemoney-unofficial.d # for litemoneyd
litemoney-unofficial.qt # for litemoney-qt
litemoney-unofficial.test # for test_litemoney
litemoney-unofficial.tx # for litemoney-tx
```

### Uninstalling
```
sudo snap remove litemoney-unofficial
```