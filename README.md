# Mapa de Vientos

Esta herramienta permite la visualización de datos de viento utilizando archivos en formato **NetCDF** del Servicio Meteorológico Nacional y la biblioteca **geemap**.

Su desarrollo se realizó en el entorno de Google Colab con lenguaje Python junto con la función **add_velocity()** para lograr la representación de las direcciones y magnitudes del viento



                                           --- INSTRUCCIONES --- 
El cuaderno a Colab se encuentra en el siguiente enlace:   [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1462-vdp6vLfGCKYWRKQBipQ701CkS5AW?usp=sharing)

                                           
**0. Instalación de librerías**


**1. Acceso a los datos del Servicio Meteorológico (SMN):**
El primer paso es obtener el archivo .nc del SMN el cual puede obtener por dos vías
* Directamente de la página del SMN:

  > [**Enlace al acceso de datos del SMN**](https://odp-aws-smn.github.io/documentation_wrf_det/Acceso_a_los_datos/)
  
* Descargando el archivo de ejemplo:
  
  > [**Enlace al archivo de ejemplo**](https://github.com/etengler/MapaVientos/tree/c96c82e8ef1f511c082e9008502a0bc08f9f0187/Archivos)

A continuación, debe agregar el archivo .nc al entorno y modificar la siguiente línea con el nombre del archivo si descarga uno diferentre al del ejemplo. 

![image](https://github.com/user-attachments/assets/841c3288-d8c3-4f77-aee0-476c8188c113)

&nbsp;

**2. Interpolación a retícula regular:**

El archivo .nc del SMN contiene los datos en una proyección Lambert Conformal. Es necesario transformar estos datos a una retícula regular de latitud-longitud.
En esta solapa ya se encuentran todos los pasos necesarios para este pasaje por lo que solo debe ejecutarla. 

  > [**Enlace a la documentacíon de Interpolación a retícula regular del SMN**](https://odp-aws-smn.github.io/documentation_wrf_det/Regrid/)

&nbsp;

**3. Conversión de Dirección y Magnitud a Componentes Zonales y Meridionales:**

Otro paso importante, es convertir la dirección y magnitud del viento en componentes zonales y meridionales a través de fórmulas trigonométricas.
Tampoco será necesario modificar nada en esta solapa, solo ejecutarla.

&nbsp;

**4. Ajuste de Dimensiones para la Visualización:**

Otro ajuste que se debe realizar es renombrar las dimensiones x e y a lon y lat, respectivamente, para poder usarlas como parámetros en la función de geemap:
 Sólo se debe ejecutar la celda en este caso.

&nbsp;

**5. Conexión a Google Earth Engine (GEE):**

En este paso, se debe hacer una conexión a GEE. De no tener una cuenta crearse una. 
 > [**Enlace a GEE**](https://earthengine.google.com/)

Lo importante es el nombre del proyecto personal de GEE, que se encuentra en el borde superior derecho de la pantalla (como indica la flecha roja).

![image](https://github.com/user-attachments/assets/bf8e9322-af6e-4c8f-948f-38db7e6672f6)

&nbsp;

**6. Visualización del Viento en un Mapa Interactivo:**
Al ejecutar esta celda se podrá visualizar el mapa de vientos con sus direcciones y magnitudes gracias a la función add_velocity() de geemap. 

 
                                           --- VISTA PREVIA ---                                                                                     
<p align="center">
  <img src="mapaVientos.gif" alt="Gif" width="600" height="400">
</p>

