# BIOS

 - Make sure that you have Virtualization enabled
 - Make sure that you have TPM enabled

# Windows applications

 - Chocolatey
 - Firefox
 - VMWare Workstation Player
 - Steam
 - Ubisoft Connect

# Chocolatey applications

```bash
choco install cascadiacode discord foobar2000 git qbittorrent skype starship vlc vscode-insiders
```

# WSL

## Install distribution

Open up Windows PowerShell in Administrator mode and run

```bash
wsl --install
```

Once installed open up Ubuntu Shell and setup the credentials

## Install better PHP Repositories

Open up Ubuntu shell and run 

```bash
sudo apt install software-properties-common
sudo add-apt-repository ppa:ondrej/php
```

## Installing Aptitude packages

```bash
sudo apt install stow \
curl \
universal-ctags \
htop \
unrar \
bash-builtins \
bash-completion \
silversearcher-ag \
mysql-server \
php-mbstring \
php8.1-bcmath \
php8.1-cgi \
php8.1-curl \
php8.1-gd \
php8.1-intl \
php8.1-mbstring \
php8.1-mysql \
php8.1-soap \
php8.1-sqlite3 \
php8.1-xml \
php8.1-zip \
php8.1 \
libapache2-mod-php8.1
```

## Setting up MySQL 

```bash
sudo /etc/init.d/mysql start
sudo mysql_secure_installation
```

## Map Silversearch to ACK

```bash
sudo ln -sf /usr/bin/ag /usr/bin/ack
```

## Install Composer

```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '906a84df04cea2aa72f40b5f787e49f22d4c2f19492ac310e8cba5b96ac8b64115ac402c8cd292b8a03482574915d1a8') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

sudo mv composer.phar /usr/local/bin/composer

composer global require friendsofphp/php-cs-fixer \
phpunit/phpunit \
phpmd/phpmd \
squizlabs/php_codesniffer \
phploc/phploc
```

## Install Node

```bash
curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install -y nodejs yarn
```

## Install Bash-It and FZF

```bash
git clone --depth=1 https://github.com/Bash-it/bash-it.git ~/.bash_it
~/.bash_it/install.sh

source ~/.bashrc
bash-it enable completion bash-it git gulp npm ssh system
bash-it enable plugin alias-completion base fzf git
bash-it enable alias general apt curl git npm vim

git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
source ~/.bashrc
```

## Install bin directory

```bash
git clone --depth 1 git@github.com:joshbenham/bin.git ~/bin
```
