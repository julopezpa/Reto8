# Reto8
#1
Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.

    range(1,101)
    for i in range(1,101):#definimos el rango de los numero que va de 1 a 100
        z=i**2#elevamos al cuadrado el numero que va en ese "turno"
        print(i, " y su cuadrados es ", z)#se imprime el numero y su cuadrado
        
![image](https://user-images.githubusercontent.com/124606636/233543747-177fae62-1a4d-4903-aaa2-b4678a0009ed.png)

#2
Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.

    for i in range(1 ,1000,2):#se define el rango de 1 a 999 y se aumenta en dos para que todos los numeros sean impares
        print(i)
    for z in range(2,1001,2):#se define el rango de 2 a 1000 y se aumenta en dos para que todos los numeros sean pares
        print(z)

![image](https://user-images.githubusercontent.com/124606636/233543835-b38333ee-ff1b-4451-86f7-2d305a35a0c2.png)

#3
Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado

    n=int(input("ingrese un numero"))#ingresamos el numeor escogido
    if n%2!=0:#miramos si es un numero par o impar
        n-=1#si llega a ser impar le disminuimos una unidad para poder empezar con los numero pares menores a n 
    for i in range(n,1,-2):#definimos el rango que va de n hasta 1 y va restando 2 unidades
        print(i)#se imprime los numero pares de n hasta 2 de menor a mayor 


