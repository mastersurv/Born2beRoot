# Born2beRoot
Поменять видюху для виртуалки на первую
### Общие важные команды
lsblk - посмотреть разбивку

su - - переход в режим суперпользователя

Устанавливаем sudo:

apt update

apt upgrade

apt install sudo

## 1. Пользователи
sudo cut -d: -f1 /etc/passwd - Посмотреть всех пользователей

lastlog - Показывает всех пользователей плюс кто когда входил (журнал)

Создать пользователя:

sudo adduser user - создает пользователя
  
sudo useradd user - создает пользователя без папки в директории /home
  
id -Gn <user> - Посмотреть в каких группах находится пользователь
  
Удалить пользователя
  
sudo deluser user
  
sudo userdel user
  
sudo gpasswd -d user group - удалить пользователя из группы
  
## 2. Группы
	
getent group - Посмотреть группы
	
groupadd group - Создать группу
	
groupdel group - Удалить группу
	
usermod -aG group user - добавить пользователя в группу (сначала указываем группу потом пользователя)
	
