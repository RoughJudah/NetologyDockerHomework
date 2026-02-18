# NetologyDockerHomework
Задача 1:
https://hub.docker.com/waldenbranda/custom-nginx/general

Задача 2:
<img width="2051" height="1057" alt="изображение" src="https://github.com/user-attachments/assets/2b6b85d5-ebce-4817-9187-5707cbb9cc0a" />

Задача 3:
<img width="1303" height="123" alt="изображение" src="https://github.com/user-attachments/assets/a9a99aa6-1d26-44b4-ba2a-638bbf744d8a" />
Контейнер работает, пока работает его основной процесс. В образе nginx основной процесс - это nginx в foreground. Когда мы нажали Ctrl+C, сигнал SIGINT был отправлен основному процессу nginx. Он завершился -> Docker остановил контейнер

<img width="1332" height="102" alt="изображение" src="https://github.com/user-attachments/assets/56f59621-621f-45f2-b530-ea3d4f891e37" />
<img width="648" height="99" alt="изображение" src="https://github.com/user-attachments/assets/2ed173a7-2a13-472c-b898-b465f51a20ca" />
<img width="653" height="464" alt="изображение" src="https://github.com/user-attachments/assets/3bded98f-bfd8-44f1-851d-c34462b94a51" />

Контейнер был запущен с публикацией порта: 127.0.0.1:8080 -> 80 (внутри контейнера) Но мы изменили nginx так, что он теперь слушает 81, а не 80. Docker продолжает проксировать: host 8080 -> container 80 А внутри контейнера порт 80 больше не слушается. 
Поэтому: curl http://127.0.0.1:8080 не работает.

<img width="819" height="141" alt="изображение" src="https://github.com/user-attachments/assets/7d15a664-5658-4210-b71a-6016bfacea77" />

Задача 4:

<img width="928" height="1010" alt="изображение" src="https://github.com/user-attachments/assets/acfd09d2-eefa-43c6-846a-2b7b703d7edd" />
