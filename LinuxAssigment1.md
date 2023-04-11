Ejercicio de Clase (Fecha de entrega 10/04/2023 23:59)
Descripción: Se pide crear usuarios par aun profe y 5 estudiantes y tener dos grupos uno de practica y el otro de teoria, cumplir con lo siguiente: el estudiante 5 no tiene un home directory todos los estudiantes deben estar en ambos grupos y el profesor solo en practica a los home directory solo podra acceder el profesor con full permisos y no asi los otros estudiantes 
Nota: Deben entregar un documento, por chat interno que contenga las capturas de pantalla que verifiquen los usuarios creados, la asignacion de los grupos y los permisos.


Approach:

Se crean los grupos Class, Teacher, Practice, Theory
```bash
# sudo groupadd Class
# sudo groupadd Teacher
# sudo groupadd Practice
# sudo groupadd Theory
```

Se crean los usuario y se asignan a los estudiantes el grupo principal Class y al profesor el grupo principal Teacher
Para los grupos secundarios se asigna Practice y Theory a todos los estudiantes y para el profesor Class y Practice
```bash
#useradd -m -g Teacher -G Class,Practice Teacher
#useradd -m -g Class -G Practice,Theory Student1
#useradd -m -g Class -G Practice,Theory Student2
#useradd -m -g Class -G Practice,Theory Student3
#useradd -m -g Class -G Practice,Theory Student4
#useradd -g Class -G Practice,Theory Student5
```

Se modifican los permisos de los home directories 
```bash
#chmod 770 Student1
#chmod 770 Student2
#chmod 770 Student3
#chmod 770 Student4
#chmod 770 Teacher
```

Se modifican los groups de los home directories
```bash
#chgrp Teacher Student1
#chgrp Teacher Student2
#chgrp Teacher Student3
#chgrp Teacher Student4
```

Listamos los resultados:

```bash

# ls -l
total 20
drwxrwx--- 2 Student1 Teacher 4096 Apr 11 16:35 Student1
drwxrwx--- 2 Student2 Teacher 4096 Apr 11 16:35 Student2
drwxrwx--- 2 Student3 Teacher 4096 Apr 11 16:35 Student3
drwxrwx--- 2 Student4 Teacher 4096 Apr 11 16:35 Student4
drwxrwx--- 2 Teacher  Teacher 4096 Apr 11 16:34 Teacher
# groups Teacher
Teacher : Teacher Class Practice
# groups Student1
Student1 : Class Practice Theory
# groups Student2
Student2 : Class Practice Theory
# groups Student3
Student3 : Class Practice Theory
# groups Student4
Student4 : Class Practice Theory
# groups Student5 
Student5 : Class Practice Theory
# cat /etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/run/ircd:/usr/sbin/nologin
gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
_apt:x:100:65534::/nonexistent:/usr/sbin/nologin
Teacher:x:1000:1003::/home/Teacher:/bin/sh
Student1:x:1001:1000::/home/Student1:/bin/sh
Student2:x:1002:1000::/home/Student2:/bin/sh
Student3:x:1003:1000::/home/Student3:/bin/sh
Student4:x:1004:1000::/home/Student4:/bin/sh
Student5:x:1005:1000::/home/Student5:/bin/sh
# cat /etc/group
root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:
tty:x:5:
disk:x:6:
lp:x:7:
mail:x:8:
news:x:9:
uucp:x:10:
man:x:12:
proxy:x:13:
kmem:x:15:
dialout:x:20:
fax:x:21:
voice:x:22:
cdrom:x:24:
floppy:x:25:
tape:x:26:
sudo:x:27:
audio:x:29:
dip:x:30:
www-data:x:33:
backup:x:34:
operator:x:37:
list:x:38:
irc:x:39:
src:x:40:
gnats:x:41:
shadow:x:42:
utmp:x:43:
video:x:44:
sasl:x:45:
plugdev:x:46:
staff:x:50:
games:x:60:
users:x:100:
nogroup:x:65534:
Class:x:1000:Teacher
Practice:x:1001:Teacher,Student1,Student2,Student3,Student4,Student5
Theory:x:1002:Student1,Student2,Student3,Student4,Student5
Teacher:x:1003:
```
