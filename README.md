# Занятие 1: Введение в Ansible

## 1. 

Значение `some_fact` имеет значение 12.

![01](src/01.png)

## 2.

Файл `group_vars/all/examp.yml`

![02](src/02.png)

## 3,4

```
ok: [centos7] => {
"msg": "el"
}
ok: [ubuntu] => {
"msg": "deb"
}
```

![03](src/03.png)

## 5,6

В файлах `group_vars/deb/examp.yml` и `group_vars/el/exampl.yml`.

![04](src/04.png)

## 7

```
ansible-vault encrypt group_vars/deb/examp.yml    
```

```
ansible-vault encrypt group_vars/el/examp.yml
```

## 8.

```
ansible-playbook site.yml -i inventory/prod.yml --ask-vault-pass
```

![05](src/05.png)

## 9.

Команда `ansible-doc -t connection -l` выводит список плагинов для подключения к локальной ноде.

## 10.

```
  local:
    hosts:
      localhost:
        ansible_connection: local
```

![06](src/06.png)
![07](src/07.png)

