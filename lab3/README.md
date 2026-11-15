ЛР Redis Rocket Counter. От docker run к docker compose и масштабированию

Ручной запуск редиса:

![lab3/Photos3/Pasted image 20261115151912.png](Photos3/Pasted%20image%2020261115151912.png)

Проверим, что она запущен и работает:

![Pasted image 20261115152025.png](Photos3/Pasted%20image%2020261115152025.png)

Запустим приложение и свяжем его с контейнером с редисом:

![Pasted image 20261115152226.png](Photos3/Pasted%20image%2020261115152226.png)

Видим, что контейнер слушает 0.0.0.0:8085->5000/tcp:

![Pasted image 20261115152231.png](Photos3/Pasted%20image%2020261115152231.png)

Перешёл в GitBash
![Pasted image 20261115152238.png](Photos3/Pasted%20image%2020261115152238.png)

Переходим на [http://localhost:8085/](http://localhost:8085/) и запускаем ракеты))
![Pasted image 20261115152244.png](Photos3/Pasted%20image%2020261115152244.png)

![Pasted image 20261115152307.png](Photos3/Pasted%20image%2020261115152307.png)![Pasted image 20261115152310.png](Photos3/Pasted%20image%2020261115152310.png)![Pasted image 20261115152314.png](Photos3/Pasted%20image%2020261115152314.png)![Pasted image 20261115152318.png](Photos3/Pasted%20image%2020261115152318.png)
P.S Собрал все виды)))

Удаляем контейнеры:
![Pasted image 20261115152324.png](Photos3/Pasted%20image%2020261115152324.png)
Создали каталог и провалились в него:
![Pasted image 20261115152327.png](Photos3/Pasted%20image%2020261115152327.png)
Создаём `d`ocker-compose.yml:
![Pasted image 20261115152330.png](Photos3/Pasted%20image%2020261115152330.png)
Запускаем стек, проверяем, что оба контейнера запущены
![Pasted image 20261115152335.png](Photos3/Pasted%20image%2020261115152335.png)
Переходим на [http://localhost:8085/](http://localhost:8085/) и снова запускаем ракеты))
![Pasted image 20261115152342.png](Photos3/Pasted%20image%2020261115152342.png)
Масштабируем  
Теперь хост сам выбирает свободный порт
![Pasted image 20261115152352.png](Photos3/Pasted%20image%2020261115152352.png)
Применим изменения и поверим:
![Pasted image 20261115152357.png](Photos3/Pasted%20image%2020261115152357.png)
Хост-порты разные, а счётчик общий:
![Pasted image 20261115152402.png](Photos3/Pasted%20image%2020261115152402.png)
Уничтожаем стек:
![Pasted image 20261115152429.png](Photos3/Pasted%20image%2020261115152429.png)
Проверка, что всё удалилось(От редиса старые файлы 1.5-2 месячной давности):
![Pasted image 20261115152434.png](Photos3/Pasted%20image%2020261115152434.png)
