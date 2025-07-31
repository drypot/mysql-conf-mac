# MySQL Conf

개발용 맥에서 사용하는 mysql 설정.

## my.cnf 연결

    $ cd /opt/homebrew/etc
    $ mv my.cnf my.cnf.org
    $ ln -s $HOME/project/mysql-conf-mac/my.cnf .

## 기초 명령들

mysqld 시작.

    $ mysqld

    ^\   <-- 중지하려면 ^C 대신 ^\

root 로 접속.

    $ mysql -u root

db 목록.

    mysql> show databases;

관리자 추가.

    $ mysql -u root
    
    CREATE USER 'drypot'@'%' IDENTIFIED BY '';
    GRANT ALL PRIVILEGES ON *.* TO 'drypot'@'%' WITH GRANT OPTION;
    FLUSH PRIVILEGES;
    quit

    $ mysql -u drypot

사용할 디비 선택.

    mysql> use {db name}
