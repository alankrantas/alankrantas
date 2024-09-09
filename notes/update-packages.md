# Installation/Upgrade Packages

## Python

#### Linux

```bash
sudo apt install python3 python3-pip python3-dev python3-venv python3-wheel python3-setuptools

sudo python3 -m pip install --upgrade pip

sudo pip3 install --upgrade numpy scipy matplotlib pandas seaborn scikit-learn opencv-python flask

sudo pip3 install --upgrade tensorflow autokeras flaml flaml[automl]

sudo pip3 cache purge
```

#### Windows

```bash
python -m pip install --upgrade pip

pip3 install --upgrade wheel setuptools numpy scipy matplotlib pandas seaborn scikit-learn flaml flaml[automl] opencv-python flask --user

pip3 install --upgrade tensorflow tensorflow-cpu

pip3 cache purge
```

## Node.js

```bash
sudo apt install curl
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install nodejs
sudo npm i -g npm@latest yarn@latest
```

[Install Node.js on ARMv6](https://blog.rodrigograca.com/how-to-install-latest-nodejs-on-raspberry-pi-0-w/)

## Golang (Linux)

Find the [platform version](https://go.dev/dl/) you need and

#### AMD64

```bash
wget https://go.dev/dl/go1.23.1.linux-amd64.tar.gz
sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go1.23.1.linux-amd64.tar.gz
```

#### ARM64

```bash
wget https://go.dev/dl/go1.23.1.linux-arm64.tar.gz
sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go1.23.1.linux-arm64.tar.gz
```

#### ARM 32-bit

```bash
wget https://go.dev/dl/go1.23.1.linux-armv6l.tar.gz
sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go1.23.1.linux-armv6l.tar.gz
```

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

## TinyGo (Linux)

Find the [platform version](https://github.com/tinygo-org/tinygo/releases) you need and

#### AMD64

```
wget https://github.com/tinygo-org/tinygo/releases/download/v0.33.0/tinygo_0.33.0_amd64.deb
sudo dpkg -i tinygo_0.33.0_amd64.deb
```

#### ARM64

```
wget https://github.com/tinygo-org/tinygo/releases/download/v0.33.0/tinygo_0.33.0_arm64.deb
sudo dpkg -i tinygo_0.33.0_arm64.deb
```

#### ARM 32-bit

```
wget https://github.com/tinygo-org/tinygo/releases/download/v0.33.0/tinygo_0.33.0_armhf.deb
sudo dpkg -i tinygo_0.33.0_armhf.deb
```

#### First Installation

Add  ```export PATH=$PATH:/usr/local/tinygo/bin``` in ```~/.bashrc```.

## Rust

```bash
curl https://sh.rustup.rs -sSf | sh
rustup update
```

## .NET (Ubuntu AMD64)

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
