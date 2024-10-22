# Command Dasar Untuk Garap Node

### 1. BUAT & HAPUS FOLDER/FILE

```
#buat folder
mkdir nama-folder
```
```
#check folder
ls
```
```
#buat file
nano nama-file
```
```
#save file nano
CTRL + X + Y + `Enter`
```
```
#hapus-file-folder
rm -rf nama-folder/file
```
### 2. GIT

```
#install git
apt install git
```
```
#check versi git
git --version
```
```
#clone GitHub
git clone link-github-yg-mau-di-clone
```
```
#hapus git
sudo apt remove git
```
### 3. SCREEN

```
#install screen
apt install screen
```
```
#buat screen
screen -S namascreen
```
```
#simpan screen
CTRL + A + D
```
```
#balik ke screen yang ada
screen -r namascreen
```
```
#check screen yang berjalan
screen -ls
```
```
#hapus screen
screen -X -S namascreen quit
```

### 4. Docker
```
#install docker
sudo apt-get install -y ca-certificates curl gnupg lsb-release && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && sudo apt-get update && sudo apt-get install -y docker-ce docker-ce-cli containerd.io && sudo apt-mark hold docker-ce docker-ce-cli containerd.io
```
```
#uninstall docker
sudo apt-mark unhold docker-ce docker-ce-cli containerd.io && sudo apt-get remove --purge -y docker-ce docker-ce-cli containerd.io && sudo rm -rf /var/lib/docker /var/lib/containerd && sudo rm /etc/apt/sources.list.d/docker.list && sudo apt-get autoremove -y && sudo apt-get autoclean
```

### 5. Go (Golang)
```
#install go
LATEST_GO=$(curl -s https://go.dev/VERSION?m=text) && wget https://go.dev/dl/${LATEST_GO}.linux-amd64.tar.gz && sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf ${LATEST_GO}.linux-amd64.tar.gz && echo "export PATH=\$PATH:/usr/local/go/bin:\$HOME/go/bin" >> ~/.bash_profile && source ~/.bash_profile && go version
```
```
#uninstall go
sudo rm -rf /usr/local/go && sed -i '/\/usr\/local\/go\/bin/d' ~/.bash_profile && sed -i '/\/go\/bin/d' ~/.bash_profile && source ~/.bash_profile
```

### 6. Node js
```
#install node js
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.4/install.sh | bash && source ~/.bashrc && nvm install node && nvm use node && node -v
```
```
#uninstall node js
rm -rf ~/.nvm && sed -i '/NVM_DIR/d' ~/.bashrc && source ~/.bashrc
```

### 7. Python
```
#install Python
sudo apt-get update && sudo apt-get install -y software-properties-common && sudo add-apt-repository -y ppa:deadsnakes/ppa && sudo apt-get update && sudo apt-get install -y python3 python3-pip && python3 --version && pip3 --version
```
```
#uninstall python
sudo apt-get remove --purge -y python3 python3-pip && sudo add-apt-repository --remove ppa:deadsnakes/ppa && sudo apt-get autoremove -y && sudo apt-get autoclean
```

### 8. Update Sistem VPS
```
sudo apt update && sudo apt upgrade -y
sudo apt install curl tar wget clang pkg-config libssl-dev jq build-essential bsdmainutils git make ncdu gcc jq chrony liblz4-tool -y
```
