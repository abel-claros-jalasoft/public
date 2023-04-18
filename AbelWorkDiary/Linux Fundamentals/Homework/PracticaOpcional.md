## Preguntas 1, 2 y 3
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417181935.png)
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
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417181821.png)

```bash
abel@UbuntuLab:/home$ su paco
$ cd /home/paco/
$ touch topsecret.txt
$ chmod 700 topsecret.txt
```
## Pregunta 5
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417182407.png)

```bash
$ touch ventas_trimestre.txt
$ chmod g=rwx ventas_trimestre.txt
$ su pablo
$ vim /home/paco/ventas_trimestre.txt
```
## Pregunta 6
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417182825.png)

```bash
$ su alba
$ touch empleados.txt
$ chmod g=rwx,o=r empleados.txt
```

## Pregunta 7
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417183052.png)

```bash
$ su abel
abel@UbuntuLab:/home$ sudo addgroup alumno
abel@UbuntuLab:/home$ sudo useradd -m -g alumno -G alumno alumno
abel@UbuntuLab:/home$ sudo passwd alumno
abel@UbuntuLab:/home$ sudo cp /home/alba/empleados.txt /home/alumno
abel@UbuntuLab:/home$ sudo chown alumno:alumno /home/alumno/empleados.txt
```
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417191621.png)

## Pregunta 8
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417191442.png)

![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417191451.png)

```bash
abel@UbuntuLab:/home$ su pablo
$ cp /usr/bin/xclock /home/pablo/reloj
$ xhost reloj
```
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417193808.png)

## Pregunta 9
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417193858.png)

```bash
abel@UbuntuLab:/home$ sudo chmod u+x,go-x /home/pablo/reloj
```
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417200129.png)

## Pregunta 10
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417200154.png)

```bash
abel@UbuntuLab:/home$ sudo useradd -m -g oficina2 -G oficina2 modesto
abel@UbuntuLab:/home$ sudo passwd modesto
abel@UbuntuLab:/home$ sudo mkdir /home/modesto/compartido_con_todos
abel@UbuntuLab:/home$ sudo chown modesto:oficina2 /home/modesto/compartido_con_todos
```
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417201410.png)

## Pregunta 11
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417201444.png)

![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417201757.png)

![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417203532.png)


## Pregunta 12
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417203625.png)

```bash
abel@UbuntuLab:/home$ sudo chmod -R a+r /home/modesto/compartido_con_todos
```
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417205302.png)

## Pregunta 13
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417203708.png)

```bash
abel@UbuntuLab:/home$ sudo chmod ug+r,o-r /home/modesto/compartido_con_todos/telefono_contactos.ods
```
## Pregunta 14
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417203734.png)

```bash
abel@UbuntuLab:/home$ sudo chmod 740 /home/modesto/compartido_con_todos/gastos_marzo.ods
```
## Pregunta 15
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417203751.png)

```bash
abel@UbuntuLab:/home$ sudo chmod 700 /home/modesto/compartido_con_todos/sueldos.ods
```
## Pregunta 16
![alt text](https://github.com/abel-claros-jalasoft/public/blob/main/AbelWorkDiary/Pasted%20image%2020230417203841.png)
![[Pasted image 20230417203841.png]]
