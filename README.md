##安装zsh
```
apt-get update
apt-get install git -y
apt-get install zsh -y
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

##安装vim
```
apt-get install vim
git clone https://github.com/haharazer/dotfile
cp -r vim ~/.vim
cp vimrc ~/.vimrc
git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
#打开vim
:BundleInstall
```

##安装nmp
```
apt-get install python-software-properties
add-apt-repository ppa:ondrej/php5-5.6
apt-get update
apt-get install nginx -y //安装Nginx服务器
apt-get install php5 -y //安装php5
apt-get install mysql-server-5.6 -y
```

##安装composer
```
curl -sS https://getcomposer.org/installer | php
mv composer.phar /usr/local/bin/composer
composer config -g repo.packagist composer http://packagist.phpcomposer.com
```

##安装pip 
```
apt-get -y install python-pip
apt-get -y install libmysqlclient-dev python-dev
```

##映射配置
```
cd ~ && mkdir -p config && cd config
ln -s /etc/php5/fpm/php.ini ./php.ini
ln -s /etc/nginx/sites-available/default ./nginx-server.conf
ln -s /etc/php5/fpm/php-fpm.conf ./php-fpm.conf
```

##启动服务
```
service php5-fpm start
service mysql start
```
