Role Name
=========

barm0leykin.postgres_deploy  простая роль для установки PotgresSQL

Example Playbook
----------------

Пример плейбука:

```
- hosts: localhost
  remote_user: root
  vars:
    - postgresql:
        version: "11"
        db_name:
          - test_db
          - test_db2
        create_user: no
        db_user:
          - test_user
          - test_admin
        db_password: QWErty123
  roles:
    - postgres_deploy
```

Тут всё просто. Версия СУБД, создавать или нет базы, создавать или нет юзеров, пароль для юзера.

Пока что пароль одинаковый. И у всех юзеров полные права, может быть позже переделаю.

License
-------

BSD

Author Information
------------------

Андрей Кудряшов
https://github.com/barm0leykin