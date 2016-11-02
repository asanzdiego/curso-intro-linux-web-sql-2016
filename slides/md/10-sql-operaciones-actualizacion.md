% SQL - Operaciones actualización
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




## Inserción de filas en una tabla
- Para poder consultar los datos de una base de
datos hay que introducirlos con la sentencia
INSERT INTO VALUES:
INSERT INTO nombre_tabla [(columnas)]
{VALUES ({v1|DEFAULT|NULL}, ...,
{vn/DEFAULT/NULL})|<consulta>};

## Inserción de filas en una tabla
- Los valores v1, v2, ..., vn se deben corresponder
con las columnas de la tabla especificada y deben
estar en el mismo orden.
- También es posible especificar el nombre de las
columnas de la tabla. En este último caso, los
valores se deben disponer de forma coherente
con el nuevo orden.
- Si se quiere especificar que un valor por omisión
se usa la palabra reservada DEFAULT, y si se trata
de un valor nulo se usa la palabra reservada
NULL.

## Inserción de filas en una tabla
- Observar que para insertar más de una fila
con una sola sentencia, se deben obtener los
datos mediante una consulta a otras tablas.

## Inserción de filas en una tabla
- Por ejemplo si se quiere insertar en una tabla clientes
que tiene las columnas :nif, nombre_cli, codigo_cli,
telefono, direccion, ciudad, se podría hacer de dos
formas:
INSERT INTO clientes
VALUES (10, ‘Mercadona’, ‘122233444-C’, ‘Gran vida 8’,
‘Madrid’, DEFAULT);
INSERT INTO clientes(nif, nombre_cli, codigo_cli,
telefono, direccion, ciudad)
VALUES (‘122233444-C’, ‘Mercadona’, 10, DEFAULT,
‘Gran vida 8’, ‘Madrid’);

## Inserción de filas en una tabla
- Insertar un préstamo en la relación Préstamo
INSERT INTO Prestamo
VALUES (‘Navacerrada’, ‘Pepe Pérez’, 125.000)

- También es posible obtener
mediante una consulta SELECT
INSERT INTO Prestamo
SELECT * FROM Nuevos_Prestamos

los

datos

## Borrado de filas de una tabla
- Para borrar valores de algunas filas de una
tabla se usa la sentencia DELETE:
DELETE FROM nombre_tabla [WHERE
condiciones];

## Borrado de filas de una tabla
- Observar que si no se utiliza la clausula
WHERE se borran todas las filas de la tabla, en
cambio si se utiliza WHERE entonces solo se
borran aquellas filas que cumplen las
condiciones especificadas.

## Borrado de filas de una tabla.
- Por ejemplo si se quieren borrar todas las filas
de la tabla proyectos se usaría la sentencia:
DELETE FROM proyectos;

- Si solo se quieren borrar las filas de la tabla en
las que el valor de la columna cliente vale 12,
entonces se usaría la sentencia:
DELETE FROM proyectos WHERE codigo_cliente = 12;

## Borrado de filas de una tabla.
- La clausula WHERE admite consultas anidadas
como por ejemplo la consulta que quiere
borrar todos los clientes que tengan un
préstamo no registrado en la relación
Préstamo.
DELETE
FROM Clientes
WHERE Clientes.NumPrestamo NOT IN
(SELECT NumPrestamo FROM Prestamo)

## Modificación de filas de una tabla
- Para modificar los valores de algunas filas de
una tabla se usa la sentencia UPDATE:
UPDATE nombre_tabla
SET columna = {expresión|DEFAULT|NULL}
[, columna = {expresión|DEFAULT|NULL} ...]
WHERE condiciones;

## Modificación de filas de una tabla
- La cláusula SET indica qué columna modificar
y los valores que puede recibir, y la cláusula
WHERE
especifica
qué
filas
deben
actualizarse.
- La parte WHERE es opcional y, si no se
especifica, se actualizarán todas las tuplas de
la tabla.

## Modificación de filas de una tabla.
- Por ejemplo si se quiere inicializar el sueldo de
todos los empleados del proyecto 2 en 500
euros:
UPDATE empleados SET sueldo = 500
WHERE num_proyec = 2;

## Modificación de Datos
- La clausula WHERE admite consultas anidadas como
por ejemplo la siguiente consulta que quiere modificar
todos los prestamos cuya sucursal hay sido cerrada a la
sucursal ‘Centro’.
UPDATE Prestamo
SET sucursal= ‘Centro’
WHERE sucursal IN
(SELECT sucursal
FROM Sucursales_Cerradas)

##
