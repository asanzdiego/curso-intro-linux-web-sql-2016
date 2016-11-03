% Introducción JSON
% Adolfo Sanz De Diego
% Noviembre 2016




# Acerca de




## Autor

- **Adolfo Sanz De Diego**
    - Blog: [asanzdiego.blogspot.com.es](http://asanzdiego.blogspot.com.es/)
    - Correo: [asanzdiego@gmail.com](mailto:asanzdiego@gmail.com)
    - GitHub: [github.com/asanzdiego](http://github.com/asanzdiego)
    - Twitter: [twitter.com/asanzdiego](http://twitter.com/asanzdiego)
    - LinkedIn: [in/asanzdiego](http://www.linkedin.com/in/asanzdiego)
    - SlideShare: [slideshare.net/asanzdiego](http://www.slideshare.net/asanzdiego/)

## Licencia

- **Copyright:**
    - Antonio Sarasa Cabezuelo <[antoniosarasa@campusciff.net](mailto:antoniosarasa@campusciff.net)>

## Fuente

- Las slides y sus fuentes las podéis encontrar en:
    - <https://github.com/asanzdiego/curso-intro-linux-web-sql-2016>




# Introducción a JSON




## ¿Qué es?

- JSON (**JavaScript Object Notation**) es un
formato de datos que se caracteriza:
    - Está basado en JavaScript.
    - Es utilizado para el intercambio de datos.
    - Es utilizado por muchas APIs de sitios web tales como
Facebook, Twitter,... para devolver su contenido.
    - Es independiente del lenguaje
    - Los archivos tienen extensión .json

## Parejas clave=valor

- JSON representa objetos de manera textual
mediante **parejas clave=valor**,

<div style="text-align:center">![Ejemplo JSON](../img/05-introduccion-json/05-introduccion-json-01.png)</div>


## Sintaxis JSON

- Un objeto se representa como una secuencia de
parejas clave=valor encerradas entre llaves { y }.

- Las claves son cadenas de texto entre comillas " y ".

## Valores JSON

- Tipos básicos: **cadena, número, booleano, null**
- **Arrays** de valores: entre corchetes [ y ]
- Otros **objetos** JSON: entre llaves { y }

## Ejemplo JSON

- Considerar el siguiente ejemplo dónde se
quiere representar la ficha de un estudiante
con sus datos personales y asignaturas
matriculadas:
    - Nombre="Pepito Pérez"
    - DNI="517899R"
    - Edad="22"



- Asignaturas matriculadas:
    - Obligatorias: Sistemas Operativos, Compiladores,
y Bases de Datos.
    - Optativas: Bases de Datos NoSQL, Minería de
Datos, Programación Lógica.
    - Libre Elección: Ajedrez, Música Clásica



- La ficha de información se puede representar
en un documento JSON de la siguiente
manera:

<div style="text-align:center">![Ejemplo JSON](../img/05-introduccion-json/05-introduccion-json-02.png)</div>


## Ejemplo API

- <http://jsonplaceholder.typicode.com/posts>

- <http://jsonplaceholder.typicode.com/posts/1/comments>




# JSON desde Python




## Módulo JSON

- Para gestionar Documentos JSON
desde Python se usa el **modulo JSON** que permite la
traducción de datos JSON en valores de Python.

## Tipos permitidos

- JSON no puede almacenar cualquier tipo de
valor Python, únicamente **cadenas, enteros,
reales, booleanos, listas, diccionarios y el tipo
None**.

## Tipos no permitidos

- JSON no puede representar objetos
específicos de Python tales como **Ficheros,
expresiones regulares, ...**

## JSON desde cadena

- Para traducir una cadena que contiene datos
JSON en un valor de Python se utiliza el
**método json.loads()**.

<div style="text-align:center">![Cargar JSON](../img/05-introduccion-json/05-introduccion-json-03.png)</div>


## Diccionario

- La llamada al método loads() del módulo json
permite cargar una cadena de datos JSON en
valores de Python, retornando como **resultado
un diccionario**.

- Si se quiere acceder a los distintos elementos
del diccionario **se usan los índices**. La cadena
JSON utiliza dobles comillas para las claves.

## Sin orden

- Observar que **los valores en los diccionarios
no están ordenados**, por lo que los pares
clave-valor pueden aparecer en orden
diferente a como aparecían en la cadena
original.

## Escribir JSON

- Para escribir un valor de Python como una
cadena de datos JSON se usa el método
json.dumps().

<div style="text-align:center">![Escribir JSON](../img/05-introduccion-json/05-introduccion-json-05.png)</div>


## Ejemplos de procesamiento

- Para comprender la utilidad y aplicación de los
Documentos JSON se van a ver un par de
ejemplos de procesamiento de documentos
JSON desde el lenguaje de programación
Python.

## Enunciado Ejemplo 1

- Considerar un programa que permita:
    - Leer desde teclado una ciudad
    - Llamar a la API de geocodificación de Google
    - Extraer la información en formato JSON que nos
devuelve.

## Recoger JSON

- Mediante urllib se recupera el texto en JSON que la API de
geocodificación de Google devuelve.

<div style="text-align:center">![Ejemplo 1 - recoger JSON](../img/05-introduccion-json/05-introduccion-json-07.png)</div>


## Procesar JSON

- Una vez recuperados los datos JSON se
analizan y se muestran.

<div style="text-align:center">![Ejemplo 1 - procesar JSON](../img/05-introduccion-json/05-introduccion-json-08.png)</div>


## Ejemplos 1

<div style="text-align:center">![Ejemplo 1 - completo](../img/05-introduccion-json/05-introduccion-json-09.png)</div>


## Enunciado  Ejemplo 2

- Twitter tiene una disponible una API con
servicios para los usuarios. Para poder utilizar
dicha API es necesario el uso de firmas Oauth
(es una tecnología para firmar peticiones en
Internet) en cada solicitud.

## Crear cuenta

- Si no se dispone de cuenta en twitter, entonces
hay que crearse una cuenta en <https://twitter.com/>

## Aceder a apps

- A continuación se navega a la dirección
<https://apps.twitter.com/>, dónde habrá que
autenticarse. Esta página da acceso a la api de
twitter para desarrolladores.

## Autenticarse

- Nos autenticamos:

<div style="text-align:center">![Ejemplo 2 - autenticarse en twitter](../img/05-introduccion-json/05-introduccion-json-11.png)</div>


## Dentro de apps

- Una vez autenticados, se entra en la página principal:

<div style="text-align:center">![Ejemplo 2 - dentro de apps de twitter](../img/05-introduccion-json/05-introduccion-json-12.png)</div>


## Crear nueva app

- Se selecciona "Create New App", lo que abre un
formulario que hay que rellenar.

<div style="text-align:center">![Ejemplo 2 - dentro de apps de twitter](../img/05-introduccion-json/05-introduccion-json-13.png)</div>


## Información app

- Cuando se pulsa sobre "Create your Twitter
application" aparece una nueva página con la
información de la aplicación.

<div style="text-align:center">![Ejemplo 2 - información de apps de twitter](../img/05-introduccion-json/05-introduccion-json-14.png)</div>


## Crear access token

- Se pulsa sobre la solapa "Keys and Access content", y
en dicha página se busca la sección "Your access
token" dónde se pulsa sobre la opción "create my
access token".

<div style="text-align:center">![Ejemplo 2 - crear access token de twitter](../img/05-introduccion-json/05-introduccion-json-15.png)</div>


## Valores app

- Después de pulsar sobre la opción "create my access
token" se han generado un conjunto de valores en la página.

<div style="text-align:center">![Ejemplo 2 - valores app de twitter](../img/05-introduccion-json/05-introduccion-json-16.png)</div>


## Valores importantes

- Los valores que son necesarios utilizar para
acceder a los datos de twitter son:
    - api_key = "Valor de la api key"
    - api_secret = "Valor de la api secret"
    - access_token_key = "Valor de la access token"
    - access_token_secret = "Valor de la access token secret"

- Una vez que se disponen de estos valores, se crea
un programa en python para recuperar datos de
Twitter.

## Programa python

- Se van a necesitar 4 programas:
    - oauth.py
    - twurl.py
    - hidden.py
    - twitter.py

## oauth.py

- El programa oauth.py contiene una
implementación del protocolo de firmas
oauth.

## hidden.py

- El programa hidden.py contiene los
parámetros para acceder a la API de twitter
que se han debido copiar de la app creada en
la API en la sección de "Keys and Access
content".

<div style="text-align:center">![Ejemplo 2 - hidden.py](../img/05-introduccion-json/05-introduccion-json-17.png)</div>


## twurl.py

- El programa twurl.py es un programa auxiliar
necesario para realizar la conexión.

<div style="text-align:center">![Ejemplo 2 - twurl.py](../img/05-introduccion-json/05-introduccion-json-18.png)</div>


## twitter.py

- El programa twitter.py contiene el
procesamiento buscado.

- En este caso se recuperan los amigos de un
usuario en Twitter, se analiza el JSON devuelto
y se extrae parte de la información sobre esos
amigos.

## Otros datos

- También recupera información de las
cabeceras de respuesta HTTP.

- En particular de x-rate-limit-remaining que
informa sobre cuántas peticiones se pueden
hacer antes de que ser bloqueados por un
corto periodo de tiempo.

## Código twitter.py

<div style="text-align:center">![Ejemplo 2 - twitter.py](../img/05-introduccion-json/05-introduccion-json-19.png)</div>

