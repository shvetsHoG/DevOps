# Для развертывания приложения с помощью Docker:
<hr>

1. Склонировать репозиторий 
```
git clone https://github.com/shvetsHoG/PTStart-DevOps.git -b docker
```
```
cd PTStart-DevOps
```
2. Настроить .env
3. Создать все нужные образы
```
cd bot
```
```
docker build -t bot_image .
```
```
cd ../db
```
```
docker build -t db_image .
```
```
cd ../db_repl
```
```
docker build -t db_repl_image .
```
4. Сделать docker-compose
```
cd ../
```
```
docker compose up -d
```
# Для развертывания приложения с помощью Ansible:
<hr>

1. Склонировать репозиторий 
```
git clone https://github.com/shvetsHoG/PTStart-DevOps.git -b ansible
```
```
cd PTStart-DevOps
```
2. Запустить 2 виртуальные машины ubuntu - 1 для бд и приложения, 2 для реплики бд
3. Настроить hosts
4. Запустить приложение
```
ansible-playbook playbook.yml
```
