# Observaciones Laboratorio No. 3

## Preguntas :writing_hand:

1. ¿Cuáles son los mecanismos de interacción que tiene el __view.py__ con el usuario?
   * La forma en la que el __view.py__ interactua con el usuario es por medio de una interfaz en la cual el usuario puede digitar un número tal que corresponda con la opcion que desee ejecutar, ya sea cargar la información en el catálogo, consultar los Top x libros por promedio, consultar los libros de un autor y consultar los libros por género.

2. ¿Cómo se almacenan los datos de __GoodReads__ en el __model.py__?
    * Para realizar este proceso en primer lugar se define una función ```newCatalog()``` la cual se encarga de crear un catálogo de listas vacias en las cuales se almacenarán los libros, autores, tags y booktags. Por otro lado, se crean funciones las cuales añadiran informacion a las listas creadas anteriormente. Sin embargo, este proceso no ocurre directamente en __model.py__, sino que ocurre dentro del __controller.py__, especfícamente en las funciones ```loadBooks(catalog)```, ```loadTags(catalog)```, ```loadBooksTags(catalog)```. Dentro de cada una de estas funciones se llaman las funciones del modelo, las cuales se encargan de tomar los valores del archivo csv seleccionado y almacenarlos en las listas creadas.
    
3. ¿Cuáles son las funciones que comunican el __view.py__ y el __model.py__?
    * Las funciones que se encargan de comunicar el __view.py__ y el __model.py__ son las que se encuentran en el __controller.py__, más específicamente estas funciones son llamadas en el __view.py__ como ```initCatalog``` y ```loadData```. Estas funciones se encargan de crear el catalogo y almacenar la informacion de los archivos csv. Adicionalmente a estas funciones también se encuentran las funciones que realizan el conteo de libros ```countBooksByTag()``` y ```getBooksByAuthor``` que retorna los libros de un autor en específico.
    
4. ¿Cómo se crea una lista?
    * Las listas se crean usando la función ```newList()``` del ADT lista. Dentro de los parentesis pueden ir un gran rango de parámetros los cuales pueden ser usados para determinar el tipo de lista a implementar o el factor de comparacion entre elementos de la lista.

5. ¿Qué hace el parámetro ```cmpfunction=None``` en la función ```newList()```?
    * El parámetro ```cmpfunction=None``` en la función ```newList()``` es el que define el factor que será usado para comparar los elementos de la lista entre sí y determinar así un orden.

6. ¿Qué hace la función ```addLast()```?
    * La función ```addLast()``` agrega un elemento al final de la lista.

7. ¿Qué hace la función ```getElement()```?
    * La funcion ```getElement()``` se encarga de obtener un elemento de la lista de acuerdo con la posición dada por parámetro.
    
8. ¿Qué hace la función ```subList()```?
    * La función ```subList()``` se encarga de retornar una partición de la lista principal. Esta se obtiene por medio de las posiciones del índice que se deben ingresar como parámetros.

9. ¿Observó algún cambio en el comportamiento del programa al cambiar el parámetro ```"ARRAY_LIST"``` a ```"SINGLE_LINKED"```?
    * En nuestro caso, el cambio mas notorio es el tiempo que el programa tarda para realizar la carga de datos. En el caso del ```"ARRAY_LIST"``` se toma alrededor de 7 minutos. Por otro lado, en el caso de```"SINGLE_LINKED"``` se tardó 8 minutos. Con esto podemos concluir que en este caso un ```"ARRAY_LIST"``` tiene un mejor tiempo de carga.
