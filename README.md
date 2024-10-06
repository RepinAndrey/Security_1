# Домашнее задание к занятию "`Система мониторинга Zabbix-2`" - `Репин Андрей`


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

![скриншот ](https://github.com/RepinAndrey/zabbix/blob/main/img/1.png)

### Задание 2
Добавьте в Zabbix два хоста и задайте им имена <фамилия и инициалы-1> и <фамилия и инициалы-2>. 
 Результат данного задания сдавайте вместе с заданием 3

### Задание 3
Привяжите созданный шаблон к двум хостам. Также привяжите к обоим хостам шаблон Linux by Zabbix Agent.

Процесс выполнения
Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
Зайдите в настройки каждого хоста и в разделе Templates прикрепите к этому хосту ваш шаблон
Так же к каждому хосту привяжите шаблон Linux by Zabbix Agent
Проверьте что в раздел Latest Data начали поступать необходимые данные из вашего шаблона
![скриншот ](https://github.com/RepinAndrey/zabbix/blob/main/img/3_1.png)
![скриншот ](https://github.com/RepinAndrey/zabbix/blob/main/img/3_2.png)

### Задание 4
Создайте свой кастомный дашборд.

![скриншот ](https://github.com/RepinAndrey/zabbix/blob/main/img/4.png)
