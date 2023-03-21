# Acceso a datos: Recuperación 1ª Ev

## Contenidos
1. Ficheros
    1. De texto
2. Bases de datos relacionales:
    1. Sentencias parametrizadas
    2. Transacciones


## Instrucciones

- Leer todo el contenido de este fichero detenidamente antes de empezar.
- Cada ejercicio puntúa diferente y está compuesto por una serie de apartados que van puntuando.
  Es altamente recomendable detectar qué ejercicios se pueden hacer de manera más sencilla y rápida para aprovechar el
  tiempo de la mejor manera posible.
- Todos los métodos tendrán que contemplar las excepciones necesarias.

>⚠️ Se recuerda que, para los ejercicios de bases de datos, es necesario instalar el driver de MySQL.

## Enunciados

### Ejercicio 1: ficheros (5 puntos)

El fichero `cotas.txt` en la carpeta "archivos" contiene un conjunto de cotas de nieve, cada una de ellas en una línea diferente.
Crear los siguientes métodos y llamarlos desde el main:

#### - leerCotas(File) [2pts]:
Método que recibe el fichero `cotas.txt` y **devuelve un ArrayList** con las cotas que contiene en su interior.

#### - aumentarCotas(ArrayList<Integer>, numero) [3pts]:
Método que recibe un ArrayList (el que devuelve el método anterior) y un número y crea un fichero llamado `nuevas_cotas.txt` con las cotas contenidas en el ArrayList, sumándoles el número recibido por parámetros.
Comprobar con el método leerCotas y el print si realmente el método funciona.


### Ejercicio 2: bases de datos (5 puntos)
Se va a utilizar un servidor de bases de datos en local, por lo que habrá que arrancar servidor MySQL del XAMPP.
Para crear dicha base de datos, se importará a mano el fichero `neptuno.sql` incluido en la carpeta de archivos, en el HeidiSQL o MySQLWorkBench.
>⚠️ Es importante incluir el driver de MySQL en este proyecto para poder testear y ejecutar dicha conexión correctamente.

#### - crearConexión [1pts]
Crear un método que permita crear una conexión con una base de datos cuyos datos se facilitan a continuación.
El método ha de retornar un objeto de tipo Connection, con la conexión a la base de datos.
**No es necesario** que reciba los parámetros de la conexión como argumentos.

- Host: localhost
- Puerto: el que indica el XAMPP
- Nombre base de datos: neptuno (crearla a mano con el Heidi / PHPMyAdmin)
- Usuario: root
- Contraseña: (vacío) / root


#### - consultaPreparada() [4pt]
Método que consulta la tabla productos. Ha de mostrar por pantalla aquellos productos cuyas `UnidadesEnExistencia` sean mayores que 5.
La consulta se tiene que realizar mediante una sentencia preparada