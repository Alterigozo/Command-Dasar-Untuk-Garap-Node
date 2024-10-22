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
