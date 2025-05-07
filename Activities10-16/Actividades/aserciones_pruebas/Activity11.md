## Paso 1

La instalación de las herramientas necesarias fue hecha al momento de correr make install

## Paso 2

Luego de haber revisado los métodos de la clase Stack, se hace el pytest y se verifica que todos los tests pasan.

![](images/1.png)

Además, se pueden correr tests en orden aleatorio usando un plugin llamado pytest-randomly.

## Paso 3

Se verifica el método test_is_empty() y se añade otro llamado test_pop2()

![alt text](images/image.png)

## Paso 4

Se corre el pytest para verificar que funciona correctamente

![alt text](images/image-1.png)

## Paso 5

Se cambia el método para testear la operación peek()

![alt text](images/image-2.png)

## Paso 6

Se usa el método test_pop() para verificar que la operación pop funciona correctamente

![alt text](images/image-3.png)

## Paso 7 

Se reemplaza el método test_push() para haberlo verificado de dos maneras distintas

![alt text](images/image-4.png)

## Paso 8
Se comprueba que con los nuevos métodos el pytest pasa

![alt text](images/image-5.png)

## Paso 9 

Se corre el comando pytest usando pytest-cov para verificar cobertura

![alt text](images/image-6.png)