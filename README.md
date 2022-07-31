# Born2beRoot
### Общие важные команды
lsblk - посмотреть разбивку

su - - переход в режим суперпользователя

sudo ufw status

systemctl status ssh

nano /etc/ssh/sshd_config - конфиг ssh

Устанавливаем sudo:

apt update

apt upgrade

apt install sudo

## 1. Пользователи
sudo cut -d: -f1 /etc/passwd - Посмотреть всех пользователей

lastlog - Показывает всех пользователей плюс кто когда входил (журнал)

### Создать пользователя:

sudo adduser user - создает пользователя
  
sudo useradd user - создает пользователя без папки в директории /home

### Посмотреть в каких группах находится пользователь
  
id -Gn user
	
groups user 
  
### Удалить пользователя
  
sudo deluser user
  
sudo userdel user
  
sudo gpasswd -d user group - удалить пользователя из группы
  
## 2. Группы
	
getent group - Посмотреть группы
	
groupadd group - Создать группу
	
groupdel group - Удалить группу
	
usermod -aG group user - добавить пользователя в группу (сначала указываем группу потом пользователя)
	
## 3. Смена имени хоста
nano /etc/hosts

nano /etc/hostname

## 4. UFW

ufw enable - запустить файервол

ufw status - проверка статуса

ufw allow 4242 - разрешить порт ssh

ufw delete (номер строки ненужного порта) - удалить порт

## 5. Политика паролей

правим файл политики паролей

nano /etc/login.defs

## 6. Скрипт

cd /usr/local/bin/

crontab -e - Открыть крон

\* * * * * /usr/local/bin/monitoring.sh - запуск каждую минуту

\* * * * * ( sleep 30 ; /usr/local/bin/monitoring.sh ) - установить запуск каждые 30 секунд
