# Why
Web-exploits.

Использован python3.5, Flask

Для запуска стоит использовать команду:

source venv/bin/activate

flask run --host=0.0.0.0

При установленном python3 в системе.

Версия с эксплоитами

Missing function access control: К страничке http://IP:5000/explore имеют доступ все, а не только зарегистрированные пользователи

SQL injection: При изменении имени пользователя отсутствует проверка на возможную SQL команду, 
Выполнить в поле username http://192.168.1.50:5000/edit_profile
test3', password_hash = 'md5$xJVQFOoN$3f3ea77f1cfbb0d18d4201393b205c50' where username = 'test3'--
Поменяет пароль пользователя test3 на 123

XSS: При заходе на страничку http://IP:5000/explore срабатывает JS-скрипт ALERT()
