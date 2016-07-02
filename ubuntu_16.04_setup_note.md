# Ubuntu 16.04 安裝筆記

## 設備

- ASUS N82JQ

## 安裝 git

sudo apt-get install git-core

git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global color.ui true

### SSH
參考：https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
sudo apt-get install xclip
xclip -sel clip < ~/.ssh/id_rsa.pub
ssh -T git@github.com

### Git Aware Prompt
參考：https://github.com/jimeh/git-aware-prompt

mkdir ~/.bash
cd ~/.bash
git clone git://github.com/jimeh/git-aware-prompt.git


## 安裝 nodejs, npm

sudo apt-get update  
sudo apt-get install nodejs  
sudo ln -s /usr/bin/nodejs /usr/bin/node  
sudo apt-get install npm  

### 安裝 hexo

npm install hexo-cli -g


## 在Gnome裡手動調整語系何輸入法

### 安裝 ibus 裡的新酷音
sudo apt-get install ibus-chewing


## 手動安裝

- Atom
- Chrome

deb檔可能會遇到執行有問題，系統update完之後就可以順利執行。
