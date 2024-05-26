#Javascript para principiantes.

una variable se asigna con el operador "="

si ingresamos un nro, puede no tomarse como nro.
un numero escrito en comillas, es tomado como un "string de texto"("cadena")

## Number.parseInt("7130") esto devuelve 7130 como número propiamente dicho.

    Number.parseInt(42000$$) devuelve 42000.

    Number.parseInt("Num. 2345") devuelve NaN (not a number) por lo tanto no puede convertir.

## Number.parseFloat() 

devuelve un nro con coma flotante (decimal)

#Operadores de asignacion

|Operador | Descripción    |
|---------|----------------|
| +       |  Suma          |
| -       | Resta          |
| *       | Multiplicacion |
| **      | Exponenciación |
| /       | Division       |
| %       | Módulo:resto de dividir|
| ++      | Incremento     |
| --      | Decremento     |
____________________________


## Operadores de cadena y números.-

El operador + se puede utilizar también para concaternar cadenas.

ej:
    
        var texto1 = "Juan" ;
        var texto2 = "Pablo" ; 
        var textoJunto = texto1 + " " + texto2 ; 
         
> (se agrega + " " + para sumar un espacio vacío entre las 2 cadenas y que no quede "JuanPablo" sino "Juan Pablo")

ej2:

        var texto3 = "bienvenidos a ";
        var texto3 += "Javascript" ;



))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))

# Funciones ASYNC y promesas.

  En Javascript el código se realiza una linea a la vez, y si existe un problema, el código no termina de realizarse, esto implica que cuando nos queremos comunicar con un server externo, a través del código, esa respuesta puede demorar.
Para que el código no se detenga hasta obtener dicha respuesta, se utilizan las funciones ASINCRONAS (async) y el manejo de "promesas"-
Las "promesas" son primeras respuestas del servidor a donde nos comunicamos, indicándonos que "nos van a retornar algún tipo de dato.

hay 2 maneras de manejar este tipo de código: por ejemplo, si queremos traer datos desde una api, necesitamos ciertos datos de la misma para comunicarnos, como mínimo, la dirección web de donde nos van a enviar los datos(esto lo define CADA api en su propia documentación).

teniendo este dato, podemos solicitar nos envíen la información de la siguiente manera;

    fetch ('direccion web de la api')  //rdto devuelve una promesa, que tenemos que manejar con .then()//
    
    .then ('datos en formato json'.json())  //aqui normalmente tenemos la respuesta, pero la misma está en formato json, por lo que la convertimos al obtenerla, genenrando una funcion flecha, que a su vez, genera una nueva promesa
    
    .then (('varDatosEnObjeto') => {resto de codigo a ejecutar}) //aqui ya tenemos los datos del json en formato objeto, para poder manipularlos, y normalmente el manejo se hace en esta instancia, mediante funciones, etc porque los datos no se pueden sacar a no ser que se manejen con otra funcion asyncrona.

    .catch (error) {
    //codigo segun el error dado por la respuesta. //si el servidor da una respuesta de error, enviará un codigo del error que se puede ver en developers.mozilla.org.
}
        
))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))

# Manejo del DOM ---------------------------------------------------------------------------------------------------
Tipos de nodo:
    -Document: es el nodo raíz del cual se derivan el resto de nodos.

    -Element: son nodos definidos por etiquetas HTML ej: <div>, <p>, <span>, etc.

    -Text : el texto dentro de un nodo element se considera un nuevo nodo hijo del tipo "text"

    -Attribute: los atributos de las etiquetas definen nodos, pero en js lo vemos como información asociada al nodo.

    -Comment node: los nodos que definen comentarios.

##DOCUMENT - Metodos de seleccion de elementos:

    como son métodos, se aplican al nodo document.

obtener un nodo por id:
    
                document.getElementByID('id a seleccionar');

obtener nodos por nombre de etiqueta:

                document.getElementsByTagName('div'); //esto devuelve una coleccion HTML de elementos, donde se puede acceder a cada elemento por indice(como un array, pero sin ser un array)

obtener nodos por querySelector:

                document.querySelector('.clase'); // esto permite seleccionar el primer elemento mediante selectores de css, se puede definir #id, .clase, [atributo], etc.

obtener una lista de nodos por querySelectorAll:

                document.querySelectorAll('#id');


## setAttribute("atributo a cambiar", "nuevo valor de atributo") : permite definir atributos de los elementos html.
    
                const input = document.querySelector('.form__input');
                input.setAttribute("type","text")

## getAttribute("atributo") : permite obtener atributos de los elementos html.
    .getAttribute; //esto devuelve el valor del atributo "type";

## removeAttribute("atributo"): directamente esto elimina el atributo del elemento html.


ATRIBUTOS GLOBALES (TODOS LOS ELEMENTOS TIENEN ESTOS ATRIBUTOS)-----------------------------------------------------------------------

-contenteditable (booleano) : indica si el elemento puede ser modificable por el usuario.

-style:

-tabIndex: permite definir con qué orden se seleccionan las etiquetas con la tecla TAB

-title: atributo que define un titulo al elemento seleccionado.


ATRIBUTOS INPUTS----------------------------------------------------------------------------------------------------------------------






# Metodos del DOM para agregar elementos desde JS.



https://lenguajejs.com/javascript/dom/insertar-elementos-dom/


            