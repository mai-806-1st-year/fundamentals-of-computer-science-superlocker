# Отчёт по лабораторной работе №3 по курсу “Фундаментальная информатика”

<b>Студент группы:</b> <ins>М80-108Б-22 Ибрагимов Далгат Магомедалиевич, № по списку 9</ins> 

<b>Контакты e-mail:</b> <ins>doly2004e@yandex.ru</ins>

<b>Работа выполнена:</b> <ins>«7» октября 2022</ins> г.

<b>Преподаватель:</b> <ins>асп. каф. 806 Сахарин Никита Александрович</ins>

<b>Входной контроль знаний с оценкой:</b> <ins>5 (отлично)</ins>

<b>Отчет сдан</b> <ins>«8» Октября 2022</ins> г., <b>итоговая оценка</b> <ins>5 (отлично)</ins>

<b>Подпись преподавателя:</b> ________________

## 1. Тема
Сети и телекоммуникации в ОС UNIX
## 2. Цель работы
Изучение и освоение удалённых команд UNIX и приобретение навыков, необходимых для выполнения курсовых и лабораторных работ в среде UNIX.
## 3. Задание (вариант № —)
Изучение удалённых команд
## 4. Оборудование
<b>Процессор:</b> AMD Ryzen 5 5600H (12) @ 3.600GHz<br/>
<b>ОП:</b> 32GiB 3200 MHz LPDDR4<br/>
<b>SSD:</b> 512 GiB<br/>
<b>Адрес:</b> <br/>
<b>Монитор:</b> 27-дюймовый (1920 х 1080)<br/>
<b>Графика:</b>AMD Radeon™ RX 6600M 2177 MHz 8GiB GDDR6<br/>
## 5. Программное обеспечение:
<b>Слой совместимости для запуска Linux-приложений в ОС Windows:</b> WSL2 5.10.102.1<br/>
<b>Операционная система семейства UNIX:</b> Ubuntu 20.04 LTS GNU/Linux 5.10.16.3-microsoft-standard-WSL2 x86_64<br/>
<b>Интерпретатор команд:</b> bash версия 5.1.16<br/>
<b>Система программирования:</b> не использовалась версия —<br/>
<b>Редактор текстов:</b> vim8 версия 8.0<br/>
<b>Утилиты операционной системы:</b> cd, pwd, ls, cp, mv, mkdir, rmdir, cat, man, ps, rm<br/>
<b>Прикладные системы и программы:</b> gnuplot<br/>
<b>Местонахождение и имена файлов программ и данных на домашнем компьютере:</b> /home/lockr<br/>
## 6. Идея, метод, алгоритм решения задачи (в формах: словесной, псевдокода, графической [блок-схема, диаграмма, рисунок, таблица] или формальные спецификации с пред- и постусловиями)
Изучить основы программного обеспечения ОС UNIX и работы с сетями в ней
Ввод команд:
- ls -l/-A/-lAF
- ssh
- service
- hostname
- tar


## 7. Сценарий выполнения работы [план работы, первоначальный текст программы в черновике (можно на отдельном листе) и тесты либо соображения по тестированию]. 
- Изучить литературу по OC UNIX
- Просмотреть демонстрационный материал в лабораторной аудитории
- Освоить удалённые команды OC UNIX
- Научиться удалённо манипулировать с файлами 
- Запротоколировать сеанс

Пункты 1-7 отчета составляются сторого до начала лабораторной работы.
Допущен к выполнению работы.  
Подпись преподавателя _____________________
## 8. Распечатка протокола 
```
PS C:\Users\lock_R> ssh -p 2222 lockr@172.17.105.181
Last login: Sat Oct  8 10:31:47 2022
lockr@lockR:~$ ls
0        Documents  Pictures   Videos  ubuntu-wsl2-systemd-script
6        Downloads  Public     lab1
Desktop  Music      Templates  lab2
lockr@lockR:~$ echo "hello world" > file_ssh.txt
lockr@lockR:~$ ls
0        Documents  Pictures   Videos        lab2
6        Downloads  Public     file_ssh.txt  ubuntu-wsl2-systemd-script
Desktop  Music      Templates  lab1
lockr@lockR:~$ cat file_ssh.txt
hello world
lockr@lockR:~$ mkdir konkur
lockr@lockR:~$ cd konkur
lockr@lockR:~/konkur$ touch ff.sh
lockr@lockR:~/konkur$ ls
ff.sh
lockr@lockR:~/konkur$ cd ./..
lockr@lockR:~$ gnuplot

        G N U P L O T
        Version 5.2 patchlevel 8    last modified 2019-12-01

        Copyright (C) 1986-1993, 1998, 2004, 2007-2019
        Thomas Williams, Colin Kelley and many others

        gnuplot home:     http://www.gnuplot.info
        faq, bugs, etc:   type "help FAQ"
        immediate help:   type "help"  (plot window: hit 'h')

Terminal type is now 'qt'
gnuplot> exit
lockr@lockR:~$ tar -zcf archive1.tar konkur/ff.sh
lockr@lockR:~$ ls
0          Downloads  Templates     konkur
6          Music      Videos        lab1
Desktop    Pictures   archive1.tar  lab2
Documents  Public     file_ssh.txt  ubuntu-wsl2-systemd-script
lockr@lockR:~$ tar -xvf archive1.tar
konkur/ff.sh
lockr@lockR:~$ rm -rf konkur
lockr@lockR:~$ ls
0        Documents  Pictures   Videos        lab1
6        Downloads  Public     archive1.tar  lab2
Desktop  Music      Templates  file_ssh.txt  ubuntu-wsl2-systemd-script
lockr@lockR:~$ tar -xvf archive1.tar
konkur/ff.sh
lockr@lockR:~$ ls
0          Downloads  Templates     konkur
6          Music      Videos        lab1
Desktop    Pictures   archive1.tar  lab2
Documents  Public     file_ssh.txt  ubuntu-wsl2-systemd-script
lockr@lockR:~$ cd konkur
lockr@lockR:~/konkur$ ls
ff.sh
lockr@lockR:~/konkur$exit
logout
Connection to 172.17.105.181 closed.
PS C:\Users\lock_R> mkdir for_ssh


    Каталог: C:\Users\lock_R


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        08.10.2022     10:47                for_ssh

PS C:\Users\lock_R> cd for_ssh
PS C:\Users\lock_R\for_ssh> New-Item -ItemType "file" -Path "C:\Users\lock_R\for_ssh\test.txt"


    Каталог: C:\Users\lock_R\for_ssh


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        08.10.2022     10:50              0 test.txt

PS C:\Users\lock_R> scp -P 2222 -r "C:\Users\lock_R\for_ssh" lockr@172.17.105.181:/home/lockr/
test.txt                                 100%    0     0.0KB/s   00:00
PS C:\Users\lock_R> ssh -p 2222 lockr@172.17.105.181
Last login: Sat Oct  8 10:36:15 2022 from 172.17.96.1
lockr@lockR:~$ ls
0          Downloads  Templates     for_ssh  ubuntu-wsl2-systemd-script
6          Music      Videos        konkur
Desktop    Pictures   archive1.tar  lab1
Documents  Public     file_ssh.txt  lab2
lockr@lockR:~$ cd for_ssh
lockr@lockR:~/for_ssh$ ls
test.txt
lockr@lockR:~/for_ssh$exit
logout
Connection to 172.17.105.181 closed.

```
## 9. Дневник отладки должен содержать дату и время сеансов отладки и основные события (ошибки в сценарии и программе, нестандартные ситуации) и краткие комментарии к ним. В дневнике отладки приводятся сведения об использовании других ЭВМ, существенном участии преподавателя и других лиц в написании и отладке программы.

| № |  Лаб. или дом. | Дата | Время | Событие | Действие по исправлению | Примечание |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 1 | дом. | 07.10.22 | 19:00 | Выполнение лабораторной работы | - | - |
## 10. Замечания автора по существу работы — Написание команд для отработки навыков работы в ОС UNIX.
Протокол:
```
lockr_vb2@sshtest2:~$ vi
lockr_vb2@sshtest2:~$ cat fffff 
sdffdfdfdf������������
lockr_vb2@sshtest2:~$ enca -L russian fffff 
MS-Windows code page 1251
  LF line terminators
lockr_vb2@sshtest2:~$ od fffff -t x1
0000000 73 64 66 66 64 66 64 66 64 66 e2 e0 e2 e0 e2 e0
0000020 e2 e0 e2 cc c0 c8 0a
0000027
lockr_vb2@sshtest2:~$ touch 2.txt
lockr_vb2@sshtest2:~$ touch 3.txt
lockr_vb2@sshtest2:~$ ls
2.txt  Desktop    Downloads  Music     Public  Templates
3.txt  Documents  fffff      Pictures  snap    Videos
lockr_vb2@sshtest2:~$ tar -cf new.tar 2.txt 3.txt fffff
lockr_vb2@sshtest2:~$ ls
2.txt  Desktop    Downloads  Music    Pictures  snap       Videos
3.txt  Documents  fffff      new.tar  Public    Templates
lockr_vb2@sshtest2:~$ scp new.tar lockr_vb@192.168.56.101:/home/lockr_vb/for_SSH/
lockr_vb@192.168.56.101's password: 
new.tar                                      100%   10KB   7.2MB/s   00:00    
lockr_vb2@sshtest2:~$ ssh lockr_vb@192.168.56.101
lockr_vb@192.168.56.101's password: 
Welcome to Ubuntu 22.04.1 LTS (GNU/Linux 5.15.0-50-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

0 updates can be applied immediately.

Last login: Tue Oct 18 22:19:50 2022 from 192.168.56.102
lockr_vb@sshtest:~/for_SSH$ tar -xf new.tar
lockr_vb@sshtest:~/for_SSH$ iconv -f CP1251 -t UTF-16 fffff -o outfile.txt
lockr_vb@sshtest:~/for_SSH$ ls
2.txt  3.txt  fffff  new.tar  outfile.txt
lockr_vb@sshtest:~/for_SSH$ file -i outfile.txt 
outfile.txt: text/plain; charset=utf-16le
lockr_vb@sshtest:~/for_SSH$ od -A n -t x1 outfile.txt 
 ff fe 73 00 64 00 66 00 66 00 64 00 66 00 64 00
 66 00 64 00 66 00 32 04 30 04 32 04 30 04 32 04
 30 04 32 04 30 04 32 04 1c 04 10 04 18 04 0a 00

```
## 11. Выводы
В ходе выполнения данной лабораторной работы были приобретены навыки работы с возможностью удаленного подключения, освоены команды, необходимые для установления соединения и удаленных манипуляций с файлами, а также приобретены навыки работы, которые помогут выполнять другие лабораторные работы

Недочёты при выполнении задания могут быть устранены следующим образом: —

Подпись студента _________________


