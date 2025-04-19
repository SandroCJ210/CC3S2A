# Actividad 5

### Fusión fast forward
![Fusión ff](images/fusionff.png)

### Fusión  no fast forward
![Fusión noff](images/fusionnoff.png)

### Fusión squash
![Fusión squash](images/fusionsquash.png)

## Ejercicios
Estos ejercicios fueron hechos al hacer las fusiones, la prueba está arriba.

1. **¿En qué situaciones recomendarías evitar el uso de git merge --ff?**  
    La desventaja más obvia de una fusión fast forward es que, al mantener lineal el historial de commits, se pierde la visibilidad de las ramas, por lo que si se quiere tener bien en claro qué ramas se han usado en el proyecto, no es una buena opción.

2. **2.	¿Cuáles son las principales ventajas de utilizar git merge --no-ff en un proyecto en equipo? ¿Qué problemas podrían surgir al depender excesivamente de commits de fusión?**  
    La principal ventaja es la visualización de las diferentes ramas junto con su convergencia. El problema más común que surge al usar estos commits continuamente son los merge conflicts.

3. **¿Cuándo es recomendable utilizar una fusión squash? ¿Qué ventajas ofrece para proyectos grandes en comparación con fusiones estándar?**  
    Es recomendable cuando se quiere tener un historial limpio de commits para una fácil lectura de estos. En proyectos grandes la ventaja sería cuando una rama o feature tiene que revertirse por cualquier razón, solo se revierte un commit y no varios de estos.

## Resolver conflictos con fusión no fast forward

![Merge conflict fusion no ff](images/mc1.png)

![Merge conflict fusion no ff 2](images/mc2.png)

Se revisa el log del repositorio

![Merge conflict fusion no ff 3](images/mc3.png)

## Preguntas

### ¿Qué pasos adicionales tuviste que tomar para resolver el conflicto?

Tuve que abrir el archivo en vscode, elegir si aceptar la nueva versión de este o la actual y por último hacer un commit más que sería el commit de fusión.

### ¿Qué estrategias podrías emplear para evitar conflictos en futuros desarrollos colaborativos?

La comunicación entre miembros del equipo es bastante importante, así que no formar silos es algo que puede evitar conflictos de fusión. Por otro lado, el uso de pull request es algo que ayuda a que alguien más revise el código y pueda evitar los conflictos en su rama.

## Comparar los historiales con git log después de diferentes fusiones

### Fusion fast forward

![Git log ff](images/logff.png)

### Fusion no fast forward

![Git log noff](images/lognoff.png)

### Fusion squash

![Git log squash](images/logsquash.png)

## Preguntas

### ¿Cómo se ve el historial en cada tipo de fusión?
En la fusión fast forward no se observan diferentes ramas, ya que esta hace una fusión que mantiene el flujo lineal.

Por otro lado, en la fusión no fast forward se nota una divergencia de ramas en el commit 2a2ae69, que termina convergiendo en el commit 6ed3dc7, esto deja en claro que se han usado dos ramas y el comienzo y fin de una de estas.

Finalmente en la fusión squash no se ve una unión de la rama master con la de feature-3, esto es porque al hacer un merge squash no se mantienen en la rama principal todos los commits que se hicieron en la otra rama, por esto se observa solamente un commit en la rama master que indica el merge de estas dos.

### ¿Qué método prefieres en diferentes escenarios y por qué?

Bueno, en el caso del fast forward, lo usaría para proyectos pequeños en el que no se necesite un historial más claro de las ramas y commits, debido a que este hace que se tenga un flujo lineal.

La fusión no fast forward la usaría en proyectos más grandes en el que sea más necesario tener un historial claro de todas las ramas, esto debido a que este merge crea un nuevo commit y mantiene el historial de cada rama creada.

La fusión squash la usaría también en proyectos grandes para ramas que cumplan cierta funcionalidad específica pero que sea pequeña, como alguna corrección a un bug, o alguna prueba o cosas por el estilo, ya que esto hace que todos los cambios de la rama que se va a fusionar se guarden en un solo commit.

## Fusión remota en un repositorio colaborativo

![Pull request](images/PR.png)

## Preguntas
### ¿Cómo cambia la estrategia de fusión cuando colaboras con otras personas en un repositorio remoto?

Pues al colaborar con otras personas se tiene que ser más cuidadoso con las fusiones, en estos casos hay que coordinar y revisar los cambios que hace cada uno en el equipo. Justamente por eso se usan los pull request, para que estos cambios puedan ser revisados y depurados.

### ¿Qué problemas comunes pueden surgir al integrar ramas remotas?

Puede que dos personas hayan hecho cambios en un mismo archivo a cierta funcionalidad en específico, esto hace que haya un conflicto en el merge y que se tenga que decidir con qué parte quedarse, o cómo fusionar ambas modificaciones, estos conflictos pueden evitarse coordinando y comunicándose.
