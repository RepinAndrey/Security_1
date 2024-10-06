# Домашнее задание к занятию "`Уязвимости и атаки на информационные системы`" - `Репин Андрей`


---

### Задание 1

>Скачайте и установите виртуальную машину Metasploitable: https://sourceforge.net/projects/metasploitable/.

>Это типовая ОС для экспериментов в области информационной безопасности, с которой следует начать при анализе уязвимостей.

>Просканируйте эту виртуальную машину, используя nmap.

>Попробуйте найти уязвимости, которым подвержена эта виртуальная машина.

>Сами уязвимости можно поискать на сайте https://www.exploit-db.com/.

>Для этого нужно в поиске ввести название сетевой службы, обнаруженной на атакуемой машине, и выбрать подходящие по версии уязвимости.

>Ответьте на следующие вопросы:

>Какие сетевые службы в ней разрешены?
>Какие уязвимости были вами обнаружены? (список со ссылками: достаточно трёх уязвимостей)
>Приведите ответ в свободной форме.

Разрешенные службы:

![скриншот ](https://github.com/RepinAndrey/Security_1/blob/main/img/1.png)

Примеры уязвимостей из базы уязвимостей:

![скриншот ](https://github.com/RepinAndrey/Security_1/blob/main/img/2.png)

![скриншот ](https://github.com/RepinAndrey/Security_1/blob/main/img/3.png)

![скриншот ](https://github.com/RepinAndrey/Security_1/blob/main/img/4.png)

### Задание 2

>Проведите сканирование Metasploitable в режимах SYN, FIN, Xmas, UDP.

>Запишите сеансы сканирования в Wireshark.

>Ответьте на следующие вопросы:

>Чем отличаются эти режимы сканирования с точки зрения сетевого трафика?
>Как отвечает сервер?
>Приведите ответ в свободной форме.

####Режим SYN

В этом режиме nmap отправляет пакеты SYN на целевой хост и анализирует ответы для определения открытых и закрытых портов.

![скриншот ](https://github.com/RepinAndrey/Security_1/blob/main/img/5.png)

####Режим FIN

FIN-сканирование использует флаг TCP FIN (завершение соединения) для определения состояния портов на целевом хосте.

Если порт закрыт, то целевой хост должен отправить ответ RST (сброс соединения). Если порт открыт, то целевой хост должен проигнорировать пакет FIN.

![скриншот ](https://github.com/RepinAndrey/Security_1/blob/main/img/6.png)

####Режим XMAS

XMAS-сканирование использует комбинацию флагов TCP FIN, URG и PSH для определения состояния портов на целевом хосте.

Если порт закрыт, то хост должен отправить ответ RST. Если порт открыт, то целевой хост должен проигнорировать XMAS.

![скриншот ](https://github.com/RepinAndrey/Security_1/blob/main/img/7.png)

####Режим UDP (-sU)

При сканировании портов по протоколу UDP, nmap отправляет UDP-пакеты на целевой порт и ожидает ответа.

Если порт открыт и слушает UDP-трафик, то целевой хост должен отправить ответ. Если порт закрыт, то целевой хост должен отправить ICMP-сообщение о недоступности порта или проигнорировать пакет.

![скриншот ](https://github.com/RepinAndrey/Security_1/blob/main/img/8.png)