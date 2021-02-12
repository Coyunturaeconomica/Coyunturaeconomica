# Coyuntura Económica - Estructura interna del proyecto :bar_chart: :chart_with_upwards_trend: :chart_with_downwards_trend:
Es necesario, dentro de un proyecto colaborativo, que exista una estructura definida la cual todos los miembros sigan para homogeneizar el proceso de tal forma que los pasos elaborados de forma separada sean entendibles para los demás colaboradores.

## Organización de carpetas :open_file_folder:
La organización de carpetas (también conocida como estructura del directorio) consiste en hacer una separación de los archivos mediante una estructura de carpetas preestablecidas que nos permite tener una organización lógica de los archivos presentes en el proyecto.

La estructura de directorio escogida es la siguiente:

- _Inputs_: Insumos del proyecto tales como: datos, modelos, o cualquier archivo necesario para la elaboración de las tareas presentes en el plan trazado. 
- _Scripts_: Archivos de códigos ejecutables, preferiblemente escritos en módulos para evitar códigos extensos y mejorar su lectura.
- _Others_: Archivos o información adicional que no interviene de manera directa en la elaboración del proyecto.
- _Outputs_: Salidas del proyecto. En nuestro caso son los datos pre-procesados y listos para crear el tablero de PowerBI.
- _Reports_: Visualización y documentación del código.

Asimismo, abra un archivo llamado _requirements.txt_, en el caso de Python, que nos permitirá tener las mismas versiones de los paquetes usados durante el proyecto, instalándose con la sentencia `$ pip install -r requirements.txt`. Esto se debe a que los paquetes están en constante actualización cambiando, en algunos casos, los métodos que contienen, generando conflictos en la ejecución de los códigos. 
Respecto a los demás lenguajes, se diseñarán otros mecanismos con el mismo propósito de trabajar con las versiones correctas.

Ahora bien, es necesario moverse dentro de las carpetas usando el lenguaje de programación que se este usando. Para esto existen las rutas relativas o árbol de directorio que nos permitirá acceder a los diferentes archivos sin usar las rutas absolutas, generando cambios en el código. Estas rutas relativas se usan de la siguiente forma:


