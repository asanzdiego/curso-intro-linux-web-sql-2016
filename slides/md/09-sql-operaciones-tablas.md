% SQL - Operaciones tablas
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





## Funciones de Agregación
- Las funciones de agregación son funciones
que permiten realizar operaciones sobre los
datos de una columna. Algunas funciones son
las siguientes:

## Funciones de Agregación
- En general, las funciones de agregación se
aplican a una columna, excepto COUNT que se
aplica a todas las columnas de las tablas
seleccionadas. Se indica como COUNT (*).

## Funciones de Agregación
- Sin embargo si se especifica COUNT(distinct
columna), entonces sólo contará los valores
que no nulos ni repetidos, y se especifica
COUNT (columna), sólo contaría los valores
que no son nulos.

## Funciones de agregación
- Por ejemplo si se quieren contar el número de
clientes de la tabla clientes cuya ciudad es
“Madrid”:
SELECT COUNT(*) AS numero_clie FROM
clientes WHERE ciudad = ‘Madrid’;

## Agrupación de filas
•

Al realizar una consulta, las filas se pueden agrupar de la siguiente
manera:
SELECT nombre_columnas_a seleccionar
FROM tabla_a_consultar [WHERE condiciones]
GROUP BY columnas_según_las_cuales_se_quiere_agrupar
[HAVING condiciones_por_grupos]
[ORDER BY columna_ordenación [DESC] [, columna [DESC]...]];

•
•

La cláusula GROUP BY permite agrupar las filas según las columnas
indicadas, excepto aquellas afectadas por funciones de agregación.
La cláusula HAVING especifica las condiciones para recuperar grupos de
filas.

## Agrupación de filas
- Por ejemplo si se quiere conocer el importe total de los proyectos
agrupados por clientes:
SELECT código_cliente, SUM(precio) AS importe FROM clientes
GROUP BY codigo_cliente;
- Y si solo queremos aquellos clientes con un importe facturado
mayor de 10000 euros
SELECT código_cliente FROM clientes
GROUP BY codigo_cliente
HAVING SUM(precio)>10000

## Vistas
- Una vista es una tabla ficticia que se construye a partir de
una consulta a una tabla real
CREATE VIEW nombre_vista [(lista_columnas)] AS
(consulta) [WITH CHECK OPTION];
- donde se indica el nombre de la vista, a continuación se
pueden especificar los nombres de las columnas de la vista,
se define la consulta que construirá la vista, y se puede
añadir la clausula “with check option” para evitar
inserciones o actualizaciones excepto en los registros en
que la cláusula WHERE de la consulta se evalúe como true.

## Vistas
- Para borrar una vista se utiliza la sentencia:
DROP VIEW nombre_vista (RESTRICT|CASCADE);

    - La opción RESTRICT indica que la vista no se
borrará si está referenciada,
    - La opción CASCADE indica que todo lo que
referencie a la vista se borrará con ésta.

## Vistas
- Para ilustrar las vistas, se van a
considerar las siguientes tablas:
    - Tabla clientes:

    - Tabla pedidos:

## Vistas
- Si se quiere crear una vista que indique
para cada cliente el número de pedidos
que tiene encargados el cliente, se
definiría la vista:
CREATE VIEW pedidos_por_cliente (codigo_cli, num_pedidos) AS
(SELECT c.codigo_cli, COUNT(*) FROM pedidos p, clientes c WHERE
p.codigo_cliente = c.codigo_cli GROUP BY c.codigo_cli);

Y se obtendría la vista:

##
