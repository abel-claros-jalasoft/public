## Preguntas 1, 2 y 3
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417181935.png)
![[Pasted image 20230417181935.png]]
```bash
abel@UbuntuLab:/home$ sudo addgroup oficina1
abel@UbuntuLab:/home$ sudo addgroup oficina2
```

```bash
abel@UbuntuLab:/home$ sudo useradd -m -g oficina1 -G oficina1 paco
abel@UbuntuLab:/home$ sudo useradd -m -g oficina1 -G oficina1 pablo
abel@UbuntuLab:/home$ sudo passwd paco
abel@UbuntuLab:/home$ sudo passwd pablo
```


```bash
abel@UbuntuLab:/home$ sudo useradd -m -g oficina2 -G oficina2 alba
abel@UbuntuLab:/home$ sudo useradd  -m -g oficina2 -G oficina2 nerea
abel@UbuntuLab:/home$ sudo passwd alba
abel@UbuntuLab:/home$ sudo passwd nerea
```

## Pregunta 4
![[Pasted image 20230417181821.png]]
```bash
abel@UbuntuLab:/home$ su paco
$ cd /home/paco/
$ touch topsecret.txt
$ chmod 700 topsecret.txt
```
## Pregunta 5
![[Pasted image 20230417182407.png]]
```bash
$ touch ventas_trimestre.txt
$ chmod g=rwx ventas_trimestre.txt
$ su pablo
$ vim /home/paco/ventas_trimestre.txt
```
## Pregunta 6
![[Pasted image 20230417182825.png]]
```bash
$ su alba
$ touch empleados.txt
$ chmod g=rwx,o=r empleados.txt
```

## Pregunta 7
![[Pasted image 20230417183052.png]]
```bash
$ su abel
abel@UbuntuLab:/home$ sudo addgroup alumno
abel@UbuntuLab:/home$ sudo useradd -m -g alumno -G alumno alumno
abel@UbuntuLab:/home$ sudo passwd alumno
abel@UbuntuLab:/home$ sudo cp /home/alba/empleados.txt /home/alumno
abel@UbuntuLab:/home$ sudo chown alumno:alumno /home/alumno/empleados.txt
```
![[Pasted image 20230417191621.png]]
## Pregunta 8
![[Pasted image 20230417191442.png]]
![[Pasted image 20230417191451.png]]
```bash
abel@UbuntuLab:/home$ su pablo
$ cp /usr/bin/xclock /home/pablo/reloj
$ xhost reloj
```
![[Pasted image 20230417193808.png]]
## Pregunta 9
![[Pasted image 20230417193858.png]]
```bash
abel@UbuntuLab:/home$ sudo chmod u+x,go-x /home/pablo/reloj
```
![[Pasted image 20230417200129.png]]
## Pregunta 10
![[Pasted image 20230417200154.png]]
```bash
abel@UbuntuLab:/home$ sudo useradd -m -g oficina2 -G oficina2 modesto
abel@UbuntuLab:/home$ sudo passwd modesto
abel@UbuntuLab:/home$ sudo mkdir /home/modesto/compartido_con_todos
abel@UbuntuLab:/home$ sudo chown modesto:oficina2 /home/modesto/compartido_con_todos
```
![[Pasted image 20230417201410.png]]
## Pregunta 11
![[Pasted image 20230417201444.png]]
![[Pasted image 20230417201757.png]]
![[Pasted image 20230417203532.png]]
## Pregunta 12
![[Pasted image 20230417203625.png]]
```bash
abel@UbuntuLab:/home$ sudo chmod -R a+r /home/modesto/compartido_con_todos
```
![[Pasted image 20230417205302.png]]
## Pregunta 13
![[Pasted image 20230417203708.png]]
```bash
abel@UbuntuLab:/home$ sudo chmod ug+r,o-r /home/modesto/compartido_con_todos/telefono_contactos.ods
```
## Pregunta 14
![[Pasted image 20230417203734.png]]
```bash
abel@UbuntuLab:/home$ sudo chmod 740 /home/modesto/compartido_con_todos/gastos_marzo.ods
```
## Pregunta 15
![[Pasted image 20230417203751.png]]
```bash
abel@UbuntuLab:/home$ sudo chmod 700 /home/modesto/compartido_con_todos/sueldos.ods
```
## Pregunta 16
![[Pasted image 20230417203841.png]]
