# ansible_mikrotik

# ВАЖНО получаем fatal error если в имени устройства >30 chars!!!!

## Start

### Получаем информацию с микротика

```bash
ansible-playbook data_get.yml
```

Правим данный playbook и пишем свою комманду

### Скачиваем бэкап с микротика

Playbook file_get.yml - создаёт бэкап на микротике, скачивает его в текущую директорию и удаляет файл с микротика.

```bash
ansible-playbook file_get.yml
```

## Info

 - Правим groups_vars/routers.yml, где указываем user и password, либо запускаем на выполнение playbook с аргументом **-k**, но указав user.
 - Если у Вас несколько разных логинов и паролей то необходимо создать папку `host_vars` и в неё поместить файл ex. `10.10.0.28.yml` и в нём определить необходимые ansible_user и ansible_password
