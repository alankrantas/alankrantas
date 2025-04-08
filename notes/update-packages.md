# Installation/Upgrade Packages

## [Python](https://www.python.org/downloads/)

#### Linux

```bash
sudo apt install python3 python3-pip python3-dev python3-venv python3-wheel python3-setuptools

sudo pip3 install --upgrade numpy scipy matplotlib pandas seaborn scikit-learn opencv-python flaml flaml[automl] flask --break-system-packages

sudo pip3 install --upgrade tensorflow autokeras transformers --break-system-packages

sudo pip3 cache purge
```

`--break-system-packages` is required for changing certain packages on Ubuntu.

#### Windows

```bash
python -m pip install --upgrade pip --user

pip3 install --upgrade wheel setuptools numpy scipy matplotlib pandas seaborn scikit-learn flaml flaml[automl] opencv-python flask --user

pip3 install --upgrade tensorflow tensorflow-cpu transformers --user

pip3 cache purge
```

## [Node.js](https://nodejs.org/zh-tw/download)

#### Linux

```bash
sudo apt install curl
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install nodejs
sudo npm i -g npm@latest yarn@latest
npm cache clean --force
yarn cache clean --all
```

[Install Node.js on ARMv6](https://blog.rodrigograca.com/how-to-install-latest-nodejs-on-raspberry-pi-0-w/)

## [Golang](https://go.dev/dl/)

```bash
GO_VERSION="1.xx.x"
GO_PLATFORM="amd64"
wget "https://go.dev/dl/go${GO_VERSION}.linux-${GO_PLATFORM}.tar.gz"
sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf "go${GO_VERSION}.linux-${GO_PLATFORM}.tar.gz"
```

The platform can be `amd64` (x64), `arm64` (ARM 64-bit) or `armv6l` (ARM 32-bit)

#### First Installation

Edit ```~/.bashrc```:

```bash
sudo nano ~/.bashrc
```

Add the following line:

```bash
export PATH=$PATH:/usr/local/go/bin
```

Press `Ctrl` + `X` to save and make the new setting to take effect in the terminal:

```bash
source ~/.bashrc
```

## [Rust](https://www.rust-lang.org/tools/install)

```bash
curl https://sh.rustup.rs -sSf | sh
rustup update
```

Uninstall:

```
rustup self uninstall
```

## [.NET](https://dotnet.microsoft.com/zh-tw/download)

#### Ubuntu AMD64

Setup the feed:

```bash
sudo sh -c "cat > /etc/apt/preferences.d/dotnet <<'EOF'
Package: dotnet*
Pin: origin packages.microsoft.com
Pin-Priority: 1001
EOF"
sudo sh -c "cat > /etc/apt/preferences.d/aspnet <<'EOF'
Package: aspnet*
Pin: origin packages.microsoft.com
Pin-Priority: 1001
EOF"
```

Installation:

```bash
sudo apt-get update && sudo apt-get install -y dotnet-sdk-8.0
```

## Misc

[Install VS Code in Linux](https://code.visualstudio.com/docs/setup/linux)

Install Docker Desktop in Ubuntu
* [Docker engine](https://docs.docker.com/engine/install/ubuntu/) (change `$(lsb_release -cs)` if needed)
* [Docker Desktop](https://docs.docker.com/desktop/install/ubuntu/)

[Setup git ssh](https://kbroman.org/github_tutorial/pages/first_time.html)

[Install Chinese/Japanese/Korean fonts in Debian](https://help.accusoft.com/PrizmDoc/v12.2/HTML/Installing_Asian_Fonts_on_Ubuntu_and_Debian.html)

#### Install Doom (Raspberry Pi)

```bash
sudo apt install chocolate-doom
sudo wget http://www.doomworld.com/3ddownloads/ports/shareware_doom_iwad.zip
sudo unzip shareware_doom_iwad.zip
chocolate-doom-setup
chocolate-doom -iwad DOOM1.WAD
```

#### Install piKiss (Raspberry Pi)

```bash
curl -sSL https://git.io/JfAPE | bash
```
