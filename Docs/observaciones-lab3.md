# Observaciones Laboratorio No. 3

## Preguntas :writing_hand:

1. ¿Cuáles son los mecanismos de interacción que tiene el __view.py__ con el usuario?
   * La forma en la que el __view.py__ interactúa con el usuario es por medio de una interfaz en la cual el usuario puede ingresar un número como input tal que corresponda con la opción que desee ejecutar, ya sea cargar la información en el catálogo, consultar los Top x libros por promedio, consultar los libros de un autor, consultar los libros por género o salir del programa. Después de seleccionar la opción que desea ejecutar, el usuario puede ingresar como input el número de libros Top que desea consultar, el nombre del autor que desea consultar o el género (tag) de los libros que desea consultar. El __view.py__ retorna como output la información solicitada de acuerdo a los inputs ingresados por el usuario.

2. ¿Cómo se almacenan los datos de __GoodReads__ en el __model.py__?
    * Para realizar este proceso, en primer lugar, se define una función ```newCatalog()``` la cual se encarga de crear un catálogo de listas vacías en las cuales se almacenarán los libros, autores, tags y booktags. Por otro lado, se crean funciones las cuales añadirán información a las listas creadas anteriormente. Este proceso es mediado por el __controller.py__, específicamente por las funciones ```loadBooks()```, ```loadTags()``` y ```loadBooksTags()```. Dentro de cada una de estas funciones se llaman las funciones del modelo ```addBook()```, ```addTag()``` y ```addBookTag()``` respectivamente, las cuales se encargan de tomar los valores del archivo csv seleccionado y almacenarlos en las listas vacías creadas.
    
3. ¿Cuáles son las funciones que comunican el __view.py__ y el __model.py__?
    * Las funciones que se encargan de comunicar el __view.py__ y el __model.py__ son las que se encuentran en el __controller.py__, más específicamente las funciones llamadas en el __view.py__ como ```initCatalog()``` y ```loadData()```. Estas funciones se encargan de llamar la función de inicialización del catálogo del modelo y cargar la información de los archivos . Adicionalmente a estas funciones, también se encuentran las funciones de consulta ```countBooksByTag()```, ```getBestBooks()``` y ```getBooksByAuthor()``` que se encargan de llamar las funciones respectivas del modelo.
    
4. ¿Cómo se crea una lista?
    * Las listas se crean usando la función ```newList()``` del ADT lista. Los parámetros de la función pueden ser usados para determinar el tipo de lista a implementar, la función de comparacion entre los elementos de la lista, un identificador usado para comparar dos elementos de la lista con la función de comaparación dada, entre otros.

5. ¿Qué hace el parámetro ```cmpfunction=None``` en la función ```newList()```?
    * El parámetro ```cmpfunction``` en la función ```newList()``` es el que define el factor que será utilizado para comparar los elementos de la lista entre sí. En el caso de ```cmpfunction=None``` no se especifica una función de comparación, por lo que se utiliza la función por defecto que requiere de especificar un valor ```key```.

6. ¿Qué hace la función ```addLast()```?
    * La función ```addLast()``` agrega un elemento en la última posición de la lista.

7. ¿Qué hace la función ```getElement()```?
    * La función ```getElement()``` se encarga de retornar un elemento de la lista de acuerdo con la posición dada por parámetro.
    
8. ¿Qué hace la función ```subList()```?
    * La función ```subList()``` se encarga de retornar una sublista de la lista original. Esta retorna los elementos a partir de la
    posición dada por parámetro, con una longitud de elementos dada también por parámetro.

9. ¿Observó algún cambio en el comportamiento del programa al cambiar el parámetro ```"ARRAY_LIST"``` a ```"SINGLE_LINKED"```?
    * En nuestro caso, el cambio más notorio es el tiempo que el programa tarda para realizar la carga de datos. En el caso del ```"ARRAY_LIST"``` se toma alrededor de 7 minutos. Por otro lado, en el caso de```"SINGLE_LINKED"``` se tardó alrededor de 8 minutos. Con esto podemos concluir que en este caso un ```"ARRAY_LIST"``` tiene un mejor tiempo de carga.
