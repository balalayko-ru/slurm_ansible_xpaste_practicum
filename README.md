# slurm_ansible_xpaste_practicum
### Создание директории для ssh ключей (из текущей папки):
```
mkdir files
cd files 
```
### Генерация ключа для проброса на сервера
```
ssh-keygen vagrant_test
```
### Запуск виртуальных серверов (из папки с Vargantfile)
```
vagrant up
```
### Соединяемя с сервером с ansible:
```
vagrant ssh controlnode
```
### Копируем файлы с world-write директорию в локальную:
```
mkdir ansible-internal
cp -R ansible/* ansible-internal
cd ansible-internal
```
### Установка необходимых collection и rolse через ansible galaxy:
```
ansible-galaxy collection install -r requirements.yml
ansible-galaxy role install -r requirements.yml
```
### Запуск playbook
```
ansible-playbook playbook.yml
```
### Проверяем результат
```
http://192.168.50.3/
```
