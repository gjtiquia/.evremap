# evremap

https://github.com/wez/evremap

> A keyboard input remapper for Linux/Wayland systems, written by @wez

## setup

## install evremap

```bash
# find a dir for building binary from source
cd <dir>

# clones to <dir/evremap>
git clone git@github.com:wez/evremap.git

# build the binary
sudo dnf install libevdev-devel
cargo build --release

# symlink binary
ln -s <dir/evremap>/target/release/evremap /usr/bin/evremap

# verify it works
type evremap
sudo type evremap
```

## setup config

```bash
# in home dir
cd

# clones to ~/.evremap
git clone <this-repo>

# symlink config
ln -s ~/.evremap/config.toml /etc/evremap.toml

# verify it works
sudo evremap remap /etc/evremap.toml
```

## systemd system service unit setup

```bash
cd <dir/evremap>

sudo cp evremap.service /usr/lib/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable evremap.service
sudo systemctl start evremap.service

# verify it works eg. by using vim and esc
```
