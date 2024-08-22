# Mapa de Vientos

Esta herramienta permite la visualización de datos de viento utilizando archivos en formato **NetCDF** del Servicio Meteorológico Nacional y la biblioteca **geemap**.

Su desarrollo se realizó en el entorno de Google Colab con lenguaje Python junto con la función **add_velocity()** para lograr la representación de las direcciones y magnitudes del viento



                                           --- INSTRUCCIONES --- 
El cuaderno a Colab se encuentra en el siguiente enlace:   [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1462-vdp6vLfGCKYWRKQBipQ701CkS5AW?usp=sharing)

                                           
**0. Instalación de librerías**

**1. Acceso a los datos del Servicio Meteorológico (SMN)**:
El primer paso es obtener el archivo .nc del SMN el cual puede obtener por dos vías
* Directamente de la página del SMN:

  > [**Enlace al acceso de datos del SMN**](https://odp-aws-smn.github.io/documentation_wrf_det/Acceso_a_los_datos/)
  
* Descargando el archivo de ejemplo:
  
  > [**Enlace al archivo de ejemplo**](https://github.com/etengler/MapaVientos/tree/c96c82e8ef1f511c082e9008502a0bc08f9f0187/Archivos)
  
**2. Interpolación a retícula regular**
Conversión de Dirección y Magnitud a Componentes Zonales y Meridionales
Ajuste de Dimensiones para la Visualización
Visualización del Viento en un Mapa Interactivo


                                            --- EJEMPLO ---                                           
<p align="center">
  <img src="mapaVientos.gif" alt="Gif" width="600" height="400">
</p>



> [**Enlace al repositorio en Google Earth Engine**]()
