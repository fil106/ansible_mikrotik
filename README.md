# ansible_mikrotik

## Start

### Получаем информацию с микротика

```bash
ansible-playbook data_get.yml
```

Правим данный playbook и пишем свою комманду

### Скачиваем бэкап с микротика

```bash
ansible-playbook file_get.yml -e "date=<текущая дата>"
```
p.s.

 - обязательно необходимо указать extra_vars. Пока не придумал как лучше получать текущую дату )

## Info

Правим groups_vars/routers.yml, где указываем user и password, либо запускаем на выполнение playbook с аргументом **-k**, но указав user.
