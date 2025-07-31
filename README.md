# MySQL Conf

개발용 맥에서 사용하는 mysql 설정.

## my.cnf 세팅

    $ cd /opt/homebrew/etc
    $ mv my.cnf my.cnf.org
    $ ln -s $HOME/project/mysql-conf-mac/my.cnf .

## 사이트 활성화

sites/enabled 디렉토리에 심볼릭 링크를 만들고/삭제하는 식으로 사이트를 켜고 끈다.

abc.conf 를 사용하는 사이트를 활성화 하려면.

    $ ln -s ../abc.conf sites/enabled

    $ nginx -s reload

## nginx 실행

nginx daemon 모드 끄고 실행.

    $ nginx -g "daemon off;"

nginx.conf 수정 후 테스트.

    $ nginx -t

nginx 데몬으로 돌고 있을 때, nginx.conf 리로딩.

    $ nginx -s reload 

## 기타

자세한 내용은 아래를 참고.

<https://github.com/drypot/web-memo>
