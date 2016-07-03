# Ubuntu 16.04 安裝筆記

## 設備

- ASUS N82JQ


## 安裝 git

```
sudo apt-get install git-core

git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global color.ui true
```

### 設定 ssh
參考：https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
sudo apt-get install xclip
xclip -sel clip < ~/.ssh/id_rsa.pub
ssh -T git@github.com
```

### 設定 Git Aware Prompt

```
mkdir ~/.bash
cd ~/.bash
git clone git://github.com/jimeh/git-aware-prompt.git
```

其他手動設定參考來源：https://github.com/jimeh/git-aware-prompt


## 安裝 nodejs, npm

```
sudo apt-get update  
sudo apt-get install nodejs  
sudo ln -s /usr/bin/nodejs /usr/bin/node  
sudo apt-get install npm  
```

### 安裝 hexo

```
npm install hexo-cli -g
```


## 在Gnome裡手動調整語系和輸入法

### 安裝 ibus 裡的新酷音

```
sudo apt-get install ibus-chewing
```

## 手動安裝

### Atom

- 從[ Atom 官網 ](https://atom.io/)下載 .deb 檔，手動執行。
- 尚未測試，以指令列下載並安裝：

```
wget https://atom.io/download/deb
sudo dpkg -i deb
rm -rf deb
```

- 手動安裝 Chrome

deb檔可能會遇到執行有問題，系統update完之後就可以順利執行。這裡的安裝能用 script 一起完成執行？


## Ubuntu gnome-terminal Profile Reset

https://github.com/Anthony25/gnome-terminal-colors-solarized

> Gnome 3.8 or higher

> Be sure to have the dconf-cli package installed and do:

> $ dconf reset -f /org/gnome/terminal/legacy/profiles:/PROFILE_ID"

> Replace PROFILE_ID by your profile ID (you can get it in your profile configuration in gnome-terminal).


## Ubuntu gnome-terminal working directory at start

Modify the ~/.bashrc file and add:

```
cd /directory/of/your/choice
```
