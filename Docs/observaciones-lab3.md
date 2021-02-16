# Observaciones Laboratorio No. 3

## Preguntas :writing_hand:

1. ¿Cuáles son los mecanismos de interacción que tiene el __view.py__ con el usuario?
   *La forma en la que el __view.py__ se interactua con el usuario es por medio de una interfaz interactiva en la cual el usuario puede digitar un numero tal que 
   corresponda con la opcion que desee, ya sea cargar la información del catalogo, consultar el top x de libros por promedio, consultar libros de un autor y consultar
   libros por género.

2. ¿Cómo se almacenan los datos de __GoodReads__ en el __model.py__?
    *Para realizar este proceso en primer lugar se define una función __newCatalog()__ la cual se encarga de crear un catalogo de listas vacias en las cuales se almace-
    naran los libros, autores, rating, etc. Por otro lado se crean funciones las cuales añadiran informacion a las listas creadas anteriormente. Sin embargo el proceso
    no ocurre directamente en __model.py__ este proceso ocurre dentro de __controller.py__, especificamente en las funciones __load_Books__, __load_Tags__, __load_TagsBooks__
    dentro de cada una de estas funciones se llaman funciones del modelo las cuales se encargan de tomar los valores del archivo csv seleccionado y almacenarlos en las listas
    creadas.
    
3. ¿Cuáles son las funciones que comunican el __view.py__ y el __model.py__?
    *Las funciones que se encargan de comunicar el __view.py__ y el __model.py__ son las que se encuentran en el controlador, para ser mas especifico estas son llamadas en la 
    vista como __initCatalog__ y __loadData__. Se encargan de crear el catalogo y almacenar la informacion de los archivos csv. Aparte de estas tambien se encuentran las funcio-
    nes que realizan el conteo de libros countBooksByTag y getBooksByAuthor que retorna los libros de un autor en especifico
    
4. ¿Cómo se crea una lista?
    *Las listas se crean usando lt.newList() dentro de una variable. Dentro de los parentesis puede ir un gran rango de comandos los cuales pueden ser usados para decidir el
    tipo de arreglo o el factor de comparacion entre elementos.

5. ¿Qué hace el parámetro ```cmpfunction=None``` en la función ```newList()```?
    *El parámetro cmpfunction=None en la función newList() es el que define el factor que será usado para comparar los elementos de la lista entre si y determinar asi un orden

6. ¿Qué hace la función ```addLast()```?
    *La función ```addLast()``` agrega el elemento al final de la lista. Similar al append usado en las listas TAD

7. ¿Qué hace la función ```getElement()```?
    *La funcion ```getElement()``` se encarga de obtener el elemento especificado en esta.
8. ¿Qué hace la función ```subList()```?
    *La función ```subList()``` se encarga de retornar una particion de la lista principal. Esta se obtiene por medio de las pocisiones del index, estas se deben ingresar como
    parametros

9. ¿Observó algún cambio en el comportamiento del programa al cambiar el parámetro ```"ARRAY_LIST"``` a ```"SINGLE_LINKED"```?
    *En nuestro caso, el cambio mas notorío es el tiempo que el programa se toma para realizar la carga de datos. En el caso del ```"ARRAY_LIST"``` se toma alrededor de 7            minutos, por otro lado ```"SINGLE_LINKED"``` se tardo 8 minutos. Con esto podemos concluir que en este caso un ```"ARRAY_LIST"``` tiene un mejor tiempo de carga.
