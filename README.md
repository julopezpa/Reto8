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
        
![image](https://user-images.githubusercontent.com/124606636/233543989-e1c3dd16-20c5-47f8-9273-ee18397d7aa8.png)

#4
Imprimir los números de 1 hasta un número natural n dado, cada uno con su respectivo factorial

    def factoriales(n=int):#definimos una funcion que calcule el factorial de un numero
        suma : int = 1
        for i in range(1, n+1):
            suma *= i
        return suma

    if __name__=="__main__":
        n = int(input("Ingrese numero final: "))#ingresamos el numero final 
        for i in range(1,n+1):#aclaramos el rango que va de 1 a n 
            factorial=factoriales(i)#llamamos la funcion y que se ejecute con la i en que vamos para ese momento
            print(str(i)+" y su factorial es "+ str(factorial))#imprimimos el numero y el factorial de ese numero 

![image](https://user-images.githubusercontent.com/124606636/233544310-20bd070c-ec5d-48a0-bb09-9b086cfeccba.png)

#5
Calcular el valor de 2 elevado a la potencia n usando ciclos for.

        n=int(input("ingrese un valor"))#ingresamos un valor
        lista=[n]#creamos una lista donde este el numero al que queremos elevar al cuadrado 
        for i in lista:#el ciclo para donde la i va a tomar los valores que se encuentren dentro de la lista
            resultado =2**i#elevamos 2 a el valor que lleve i 
            print(resultado)#imprimimos el valor de 2 elevado a i

![image](https://user-images.githubusercontent.com/124606636/233544359-773d3213-31b2-486e-863e-c5db4ce4f8bb.png)

#6
Leer un número natural n, leer otro dato de tipo real x y calcular x^n usando ciclos for.

        n=int(input("ingrese un valor"))#ingresamos el valor del exponente 
        x=float(input("ingrese un valor"))#ingresamos el valor de la base
        lista=[n]#creamos una lista que solo contenga n 
        for i in lista:#el ciclo
            y=x**i#elevamos la base escogida a el valor de i que este tomando en ese "turno"
            print(y)#imprimimos lo que nos da el calculo anterior
![image](https://user-images.githubusercontent.com/124606636/233544439-25244d35-c15d-4e6c-b089-099df863daae.png)


#7
Diseñe un programa que muestre las tablas de multiplicar del 1 al 9.

        for i in range(1,10):#primer ciclo para definir el primer factor  
            print("tabla de multiplicar de "+ str(i))
            for x in range(1,10):#segundo ciclo para definir el segundo factor 
                y=x*i#se multiplica el primer factor con todos los elementos del segundo ciclo 
                print( str(i) + "*" + str(x)+ "="+str(y))#imprimimos:D
![image](https://user-images.githubusercontent.com/124606636/233544515-526af915-9726-4f69-8a8b-b6d08d95180c.png)

#8
Diseñar una función que permita calcular una aproximación de la función exponencial alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. nota: use math para traer la función exponencial y mostrar la diferencia entre el valor real y la aproximación.

        import math #fmportamos de la libreria math
        def exponencial(x):#funcion para la exponencial 
            return math.exp(x)

        def factorial(n:int): #funcion para factorial
            i = 1
            for x in range(1, n+1):
                i*=x
            return i

        def seriemac(x,n):#funcion para la serie de maclaurin
            l=0
            for i in range (n+1): 
                 l+= (x**i)/factorial(i)#se pone la formula de hacer la serie de maclaurin
            return l

        if __name__ == "__main__":  
         a = float(input("Ingrese el valor de x:"))# se ingresa el valor de x
         b = int(input("Ingrese la cantidad de las series Maclaurin:"))# se ingresa la cantidad de serie maclaurin
         print(exponencial(a)) # se imprime el exponencial de x
         print(seriemac(a,b)) # se imprime la aproximacion con la serie maclaurin
         
![image](https://user-images.githubusercontent.com/124606636/233544581-7ce4c759-dc28-4fea-80ac-ecb2c56a28d0.png)


#9
Diseñar una función que permita calcular una aproximación de la función seno alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. nota: use math para traer la función seno y mostrar la diferencia entre el valor real y la aproximación.

        import math # importamos la libreria math
        def seno(x): # funcion para el seno
            return  math.sin(x) 

        def factorial(n : int ): # funcion para la factorial
            p = 1
            for i in range(1,n+1):
                p *= i
            return p

        def seriemc(x,n): # funcion para aproximacion con la serie de maclaurin 
            m=0
            for i in range(n+1):
                m += ((-1)**i)*(x**((2*i)+1))/(factorial((2*i)+1))
            return m

        if __name__ == "__main__": 
            a=float(input("ingrese el valor de x: ")) # Se pide el valor de x
            b=int(input("ingrese la cantidad de las serie de Maclaurin: ")) #Se pide la cantidad de la serie
            print(seno(a)) # Se imprime el valor "real"
            print(seriemc(a,b)) # Se imprime la aproximación
![image](https://user-images.githubusercontent.com/124606636/233545601-99a12e95-c800-4abb-9f6e-a520218a6e29.png)

#10
Diseñar una función que permita calcular una aproximación de la función arcotangente alrededor de 0 para cualquier valor x en el rango [-1, 1], utilizando los primeros n términos de la serie de Maclaurin. nota: use math para traer la función arctan y mostrar la diferencia entre el valor real y la aproximación.

        import math # importamos la libreria math
        def arcotan(x):# funcion para el arcotangente
            return math.atan(x)

        def seriemc(x,n): # Se hace con la serie Maclaurin la aproximación
            l=0
            for i in range(n+1):
                l += ((-1)**i)*(x**((2*i)+1))/((2*i)+1)
            return l

        if __name__ == "__main__":  
         a= float(input("ingresar x entre -1 y 1: ")) # Se pide el valor de x entre -1 y 1
         b=int(input("ingresar cantidad de las serie de Maclaurin : ")) #Se pide la cantidad de la serie
         print(arcotan(a)) # Se imprime el valor "real"
         print( seriemc(a,b))  # Se imprime la aproximación
         
![image](https://user-images.githubusercontent.com/124606636/233545164-552e0d96-69b9-4ad0-9051-a773f94e4c32.png)

# meme random
![image](https://user-images.githubusercontent.com/124606636/233545409-da2dac22-45ad-4373-b45c-762db9d7d3e9.png)



