Paso 1:

Se verifica que está inicializada la base de datos.

![alt text](images/image-1.png)

Se corre pytest y se verifica que hay errores que deben de corregirse.

![alt text](images/image.png)

Se tuvo que añadir "with app.app_context():" a los métodos setup_database(),  setup_method(), teardown_method(), test_create_an_account() y est_create_all_accounts() para que ya no hayan errores. Se corre el pytest y se verifica que funciona.

![alt text](images/image-2.png)

Se cargan los datos json en el siguiente método:

![alt text](images/image-3.png)

![alt text](images/image-4.png)

Se verifica que no hay errores al correr pytest

![alt text](images/image-5.png)

## Paso 3

Se tiene un test para la creación de una cuenta

![alt text](images/image-6.png)

Se corre pytest y se comprueba que no hay errores
![alt text](images/image-7.png)

## Paso 4

Nuevamente se revisa si la implementación del test para todas las cuentas es correcta y se corre pytest.

![alt text](images/image-8.png)

![alt text](images/image-9.png)

## Paso 5

Se añade db.session.remove() a setup_database(), además de que se comprueba que se tengan las funciones teardown_method() y setup_method()

![alt text](images/image-10.png)

Se corre pytest

![alt text](images/image-11.png)
