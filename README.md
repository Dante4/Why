# Why
Web-exploits.

Использован python3, Flask

Для запуска стоит использовать команду:

source venv/bin/activate

При установленном python3 в системе.

Версия с эксплоитами

Missing function access control: К страничке http://IP:5000/explore имеют доступ все, а не только зарегистрированные пользователи

SQL injection: При регистрации отсутствует проверка на возможную SQL команду, 
Первоначальный логин пользователя: test1
Первоначальный пароль: test2
После регистрации пользователя с ником: ';update user SET password_hash='md5$f2BXPySx$2c5d5e305058f6f8c787e3075b3be337' where username='test1'; --
Пароль меняется на: test1

XSS: При заходе на страничку http://IP:5000/explore срабатывает JS-скрипт ALERT()
