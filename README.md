# sesion7-tarea-individual

Enunciado.
La empresa "Distanza SA" tiene sucursales en toda España. Su sede central, al igual que el almacén
de donde se surten todas las sucursales se encuentra en Madrid.
Cada sucursal consta de una zona de exposición y otra de gestión que no siempre tienen la misma
ubicación.
Cuando se hace un pedido al almacén de la central las sucursales reciben los artículos en el
departamento de exposición y el albarán y el pago se remiten al departamento de gestión.
Sabiendo que en cada pedido la información que tiene que haber, además de los datos de la
sucursal que realiza el pedido y sus direcciones para los envíos correspondientes, (en el caso de que
ambas coincidan solo aparece una), hay que reflejar los siguientes datos:
•••••Código del pedido, que está formado por una cadena de 8 caracteres de los cuales el
primero es una letra.
Nombre del trabajador que realiza el pedido.
Fecha del pedido.
Observaciones sobre el pedido, cuyos valores son, en caso de que exista el dato: urgente o
incompleto.
Plazo de revisión de los productos recibidos que será un intervalo de tiempo expresado en
días y dependerá del precio final del pedido.
Respecto a los artículos de los que se hace el pedido hay que guardar, para cada uno de ellos:
••••Código del artículo, formado por tres letras mayúsculas y tres dígitos separados por un
guión. Es la referencia que tiene que dar el ordenante a la sede en caso de devolución de
algún artículo.
Número de unidades pedidas.
Precio de cada unidad.
Observaciones del artículo.
Construir:
1. El vocabulario para el documento XML que utiliza esta empresa para gestionar los pedidos
utilizando un DTD externo.
2. Ese mismo vocabulario utilizando el lenguaje XMLSchema debidamente documentado con
fecha de creación, nombre del autor y utilidad del esquema.
3. Realizar un fichero XML que se corresponda con una instancia del vocabulario diseñado y
asociarle al DTD.
4. Modificar ese fichero XML para asociarle al esquema diseñado.
Criterios de puntuación. Total 10 puntos.
1. DTD: 3 puntos repartidos como sigue:
a. Definición de la estructura de elementos (1 punto).
b. Definición de los tipos de los elementos (1 punto).
c. Definición de atributos (1 punto).
2. XML Schema: 5 puntos repartidos como sigue:
a. Documentación del documento y de los elementos (1 punto).
b. Definición de la estructura de elementos (1 punto).
c. Definición de los tipos de los elementos (1 punto).
d. Definición de atributos (1 punto).
e. Utilización adecuada de facetas (1 punto).
3. Fichero XML: 1 punto.
4. Asociación con el DTD: 0.5 puntos.
5. Asociación con el esquema: 0.5 puntos.
Recursos necesarios para realizar la Tarea.
Es recomendable trabajar con un editor de XML que facilite la edición y validación de los ficheros.
Puede ser práctico utilizar uno con una licencia de prueba.
Consejos y recomendaciones.
Es recomendable generar el DTD y después de haber validado el documento XML, abordar la
creación del esquema.

