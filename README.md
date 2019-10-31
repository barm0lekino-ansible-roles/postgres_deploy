Role Name
=========

postgres_deploy  простая роль для установки PotgresSQL

Example Playbook
----------------

Пример плейбука:

- hosts: localhost
  remote_user: root
  vars:
    - postgresql:
        version: "11"
        create_db: yes
        db_name: test_db
        create_user: yes
        db_user: test_user
        db_password: QWErty123
  roles:
    - postgres_deploy

Тут всё просто. Версия СУБД, создавать или нет базу, создавать или нет юзера, пароль для этого юзера.

License
-------

BSD

Author Information
------------------

Андрей Кудряшов
https://github.com/barm0leykin