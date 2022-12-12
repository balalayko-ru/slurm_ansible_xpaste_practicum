# slurm_ansible_xpaste_practicum
### �������� ���������� ��� ssh ������ (�� ������� �����):
```
mkdir files
cd files 
```
### ��������� ����� ��� �������� �� �������
```
ssh-keygen vagrant_test
```
### ������ ����������� �������� (�� ����� � Vargantfile)
```
vagrant up
```
### ���������� � �������� � ansible: 
```
vagrant ssh controlnode
```
### �������� ����� � world-write ���������� � ���������:
```
mkdir ansible-internal
cp -R ansible/* ansible-internal
cd ansible-internal
```
### ��������� ����������� collection � rolse ����� ansible galaxy:
```
ansible-galaxy collection install -r requirements.yml
ansible-galaxy role install -r requirements.yml
```
### ������ playbook
```
ansible-playbook playbook.yml
```
### ��������� ���������
```
http://192.168.50.3/
```