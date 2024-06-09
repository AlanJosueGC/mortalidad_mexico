# mortalidad_mexico
Este proyecto analiza los datos de defunción de la base de datos del 2020 obtenida de:
http://www.dgis.salud.gob.mx/descargas/datosabiertos/excesoMortalidad/Exceso_Mortalidad_MX_2020_Historico.zip?v=2022.11.04

la base de datos tiene varios comprimidos, usamos el que dice Exceso_Mortalidad_MX_2020_quincena001_SE41 y la tabla que contiene dentro

Creamos la tabla en MySQL cambiando el nombre de las columnas por las siguientes:

FECHA_ACTUALIZACION: fecha_actualizacion
ID_REGISTRO: id_registro
ENTIDAD_REG: estado
MUNICIPIO_REG: municipio
FECHA_DEFUNCION: fecha_defuncion
SEXO: sexo

El proyecto analiza las edades de defuncíon de manera simple, los clasifica por edad y estado. 
Cada numero de estado corresponde a un estado en orden alfábetico de acuerdo a la siguiente página:
https://www.agricultura.gob.mx/sites/default/files/sagarpa/document/2018/07/17/8/180717115914/entidades-federativas.pdf

Se hacen pequeñas consultas como valores minimos y maximos agrupandolos por estado y sexo, se calcula el promedio de edad de defunción y
finalmente se hace un histograma de las edades de defuncion para tener un idea de la probabilidad de tener una nueva defunción a cierta edad.
