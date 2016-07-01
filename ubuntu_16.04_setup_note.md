# 安裝 git

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


# 在Gnome裡手動調整語系何輸入法

### 安裝 ibus 裡的新酷音
sudo apt-get install ibus-chewing


# 手動安裝 Atom
