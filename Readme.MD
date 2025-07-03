 ## Procesamiento de Datos de SECOP y MEN

Este proyecto tiene como objetivo procesar y analizar dos datasets provenientes de datos abiertos de Colombia: el dataset de SECOP y el dataset de MEN.

## Datasets

1. **SECOP**: Sistema Electrónico para la Contratación Pública
   - URL: [https://www.datos.gov.co/resource/rpmr-utcd.csv](https://www.datos.gov.co/resource/rpmr-utcd.csv)

2. **MEN**: Ministerio de Educación Nacional
   - URL: [https://www.datos.gov.co/resource/nudc-7mev.csv](https://www.datos.gov.co/resource/nudc-7mev.csv

## Requisitos

Para ejecutar el procesamiento de datos, asegúrate de tener instalados los siguientes paquetes:

- `pandas`
- `numpy`
- `requests`
- `databricks`

## Estructura del Proyecto

El proyecto está organizado de la siguiente manera:


## Descarga de Datos

Para descargar los datos, ejecuta el script `descargar_datos.py` que se encuentra en la carpeta `scripts`. Este script descargará los archivos CSV desde las URLs proporcionadas y los guardará en la carpeta `data`.

python import requests

url_secop = "https://www.datos.gov.co/resource/rpmr-utcd.csv" url_men = "https://www.datos.gov.co/resource/nudc-7mev.csv"

def descargar_datos(url, nombre_archivo): response = requests.get(url) with open(nombre_archivo, 'wb') as file: file.write(response.content)

descargar_datos(url_secop, 'data/secop.csv') descargar_datos(url_men, 'data/men.csv')

## Procesamiento de Datos

Los notebooks `procesamiento_secop.ipynb` y `procesamiento_men.ipynb` contienen el código para procesar los datos de cada dataset. Asegúrate de ejecutar estos notebooks en un entorno de Databricks para aprovechar las capacidades de procesamiento distribuido.

### Ejemplo de Procesamiento

A continuación se muestra un ejemplo de cómo cargar y mostrar los datos utilizando PySpark en Databricks:

## Contribuciones

Si deseas contribuir a este proyecto, por favor sigue los siguientes pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -am 'Añadir nueva funcionalidad'`).
4. Haz push a la rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un Pull Request.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

