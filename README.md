# Coyuntura Económica - Estructura interna del proyecto :bar_chart: :chart_with_upwards_trend: :chart_with_downwards_trend:
Es necesario, dentro de un proyecto colaborativo, que exista una estructura definida la cual todos los miembros sigan para homogeneizar el proceso de tal forma que los pasos elaborados de forma separada sean entendibles para los demás colaboradores.

## Organización de carpetas :open_file_folder:
La organización de carpetas (también conocida como estructura del directorio) consiste en hacer una separación de los archivos mediante una estructura de carpetas preestablecidas que nos permite tener una organización lógica de los archivos presentes en el proyecto.

La estructura de directorio escogida es la siguiente:

- **Inputs**: Insumos del proyecto tales como: datos, modelos, o cualquier archivo necesario para la elaboración de las tareas presentes en el plan trazado. 
- **Scripts**: Archivos de códigos ejecutables, preferiblemente escritos en módulos para evitar códigos extensos y mejorar su lectura.
- **Others**: Archivos o información adicional que no interviene de manera directa en la elaboración del proyecto.
- **Outputs**: Salidas del proyecto. En nuestro caso son los datos pre-procesados y listos para crear el tablero de PowerBI.
- **Reports**: Visualización y documentación del código.

Asimismo, abra un archivo llamado _requirements.txt_, en el caso de Python, que nos permitirá tener las mismas versiones de los paquetes usados durante el proyecto, instalándose con la sentencia `$ pip install -r requirements.txt`. Esto se debe a que los paquetes están en constante actualización cambiando, en algunos casos, los métodos que contienen, generando conflictos en la ejecución de los códigos. 
Respecto a los demás lenguajes, se diseñarán otros mecanismos con el mismo propósito de trabajar con las versiones correctas.

Ahora bien, es necesario moverse dentro de las carpetas usando el lenguaje de programación que se este usando. Para esto existen las rutas relativas o árbol de directorio que nos permitirá acceder a los diferentes archivos sin usar las rutas absolutas, generando cambios en el código. Estas rutas relativas se usan de la siguiente forma:

![alt text][logo]

[logo]: https://github.com/Coyunturaeconomica/Coyunturaeconomica/blob/main/paths.PNG "Rutas"

**EJEMPLO**: 
El directorio de trabajo en nuestro caso será la carpeta “_Scripts_” donde se alojaran los códigos. Sin embargo, necesitamos acceder a la carpeta “_Inputs_” para importar los datos del recaudo del GNC mensual por tipo (_recaudo_mensual_tipo.xlsx_). 

Si tomamos dos rutas absolutas como ejemplo tendríamos:
<p align="center">
 C:\User\Camilo\OneDrive-EAFIT\Grupo de coyuntura\Tablero\Programming\Inputs\recaudo_mensual_tipo.xlsx
</p>
 
<p align="center">
 C:\User\Jesús Botero\Documents\Grupo de coyuntura\Tablero\Inputs\recaudo_mensual_tipo.xlsx
</p>

Así, si el usuario Jesús Botero desea ejecutar el código elaborado por Camilo tendría que cambiar las rutas del código. Este problema se puede evitar si usamos rutas relativas para generalizar el acceso a las carpetas: 

<p align="center">
 ..\Inputs\recaudo_mensual_tipo.xlsx
</p>

Adicionalmente, y como se menciona anteriormente, los códigos deben estar escritos en módulos para evitar códigos excesivamente extensos. 

**EJEMPLO**:
-	preprocessing.py (código principal).
-	functions.py (archivo de código que guarda las funciones).
-	web_scraping_api.py (archivo de código que nos permite descargar los datos usando web scraping o usando API’ s).
-	interface.py (archivo de código que crea una interfaz gráfica de usuario).

En forma de consideración final, antes de pasar a algunas recomendaciones, cuando los archivos que estén usando tengan nombres largos y poco entendibles, renombres los archivos evitando espacios o cualquier símbolo diferente a guion bajo.

Recomendaciones a la hora de trabajar con organización de carpetas:
-	Omita guardar archivos en el escritorio.
-	Omita guardar archivos en descargas.
-	Cuando descargue un archivo asegurase de moverlo a su carpeta correspondiente.
-	Constantemente este revisando la organización de los archivos.
-	Si consideran necesario usar más carpetas, traten de no excederse.

Finalmente, todo el contenido descrito anteriormente (mover archivos, renómbralos, acceder a ellos estando en otra carpeta, etc.) se puede hacer de manera automática desde el software en el cual estén trabajando.

## Código :computer:
-	**SharePoint**: Herramienta de almacenamiento.
-	**Descarga automática de los datos**: Web Scraping o API’s.
-	**Organización de archivos**: Modificaciones mencionadas en la sección de organización de carpetas.
-	**Preprocesamiento**: Asignado a cada miembro los datos que deben pre-procesar.
-	**Exportar datos**: Exportar los datos pre-procesados y listos para montar en el tablero.

## Herramientas :wrench: :hammer:
1. **SharePoint**: Alojamiento de los datos, imagenes, logos, códigos, etc.
2. **Lenguaje de programación**: Archivos de códigos ejecutables de cada software (py, R, m, do…).
3. **Notebooks (opcional)**: Elaboración de los reportes. En otras palabras, documentación de código donde muestre como funciona y los pasos que sigue.
4. **GitHub**: Sistema de control de versiones que nos permite tener registro de los pasos elaborados en el proyecto. Además, nos permite gestionar la compatibilidad de las distintas partes que se están trabajando.
5. **Guías de estilos**: Las guías de estilos son normas estandarizadas para la escritura de códigos de programación. En otras palabras, nos dan convenciones de codificación para aplicar a nuestros códigos. De esta forma conseguimos que todos comprenda de la mejor forma los códigos escritos por sus compañeros. A continuación algunas guías de estilos:

Lenguaje | Guia de estilos |
--- | --- | 
Python| [Pep8](https://www.python.org/dev/peps/pep-0008/) | 
R | [Hadley Wickham - Tidyverse](https://style.tidyverse.org/)<br>[Hadley Wickham - Style guide](http://adv-r.had.co.nz/Style.html)| 
MatLab | [Richard Johnson - MathWorks](http://www.datatool.com/downloads/MatlabStyle2%20book.pdf) |

**Hasta aquí podemos resumir la estructura de la siguiente forma:**

![alt text][estructura]

[estructura]: https://github.com/Coyunturaeconomica/Estructura/blob/main/Estructura-PowerBI-GC.jpg "Estructura"


## Almacenamiento (SharePoint)
Usaremos el SharePoint del grupo como herramienta de almacenamiento desde los insumos del código hasta los componentes del PowerBI. Cualquier resultado, modelo, código, etc., deberá estar alojado en la cuenta del grupo.

La estructura inicial serán dos carpetas las cuales serán:
- **Programming**: Elementos relacionados con la programación como sccripts, datos, resultados, etc.
- **PowerBI**: Elementos relacionados con el tablero como logos, template, imagenes, archivo con comentarios de expertos, etc. 

![alt text][arbol]

[arbol]: https://github.com/Coyunturaeconomica/Estructura/blob/main/Arbol-PowerBI-CG.jpg "Arbol"

## GitHub
Recomendaciones a la hora de crear un repositorio.
- No escribir el nombre de corrido, usar separadores. Ejemplo: *repositorio_de_prueba* o *repositorio-de-prueba*.
- Añadir un pequeña descripción.
- Poner el repositorio público.
- Añadir el README y la licencia (preferiblemente MIT License).

Para saber saber sobre el funcionamiento revise [Manual de GitHub – Coyuntura económica](https://github.com/Coyunturaeconomica/Manual-GitHub/blob/main/README.md).
