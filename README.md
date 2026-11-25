# Observatorio de Extorsiones en Guayaquil

Plataforma web que muestra cómo se distribuyen las extorsiones en Guayaquil entre 2021 y 2024, por distrito, por momento del día y por tipo de delito, y que estima la probabilidad de cada tipo de incidente en cada subcircuito policial.

Proyecto académico de la carrera de Ingeniería en Estadística (ESPOL), Facultad de Ciencias Naturales y Matemáticas, en colaboración con el Centro de Estudios e Investigaciones Estadísticas.

![Portada del observatorio](img/imagen-portada.png)

## Qué se puede consultar

| Módulo | Qué muestra | Técnica |
| --- | --- | --- |
| Análisis univariante | Tasa de extorsiones por distrito, por año (2021 a 2024) y acumulada | Tasas por distrito |
| Análisis temporal | Casos por mes, por día de la semana y por rango horario | Series de tiempo descriptivas |
| Análisis multivariante | Relación entre distrito, tipo de delito, peligrosidad y amenaza de muerte | Análisis de correspondencias múltiples (ACM) |
| Análisis geográfico | Intensidad de casos sobre el mapa de la ciudad, año por año | Mapa de calor |
| Predicciones geográficas | Probabilidad de cada tipo de incidente al buscar un subcircuito | Modelo bayesiano |

## Datos

- Fuente: Ecuador en Cifras.
- Período: 2021 a 2024.
- Unidad territorial: distritos, circuitos y subcircuitos de Guayaquil.

## Mi aporte

Diseñé y programé el sitio web: la plantilla común en PHP, una página por cada análisis, los gráficos con Highcharts y los mapas con Leaflet. El sitio lee desde archivos JSON los resultados que el equipo obtuvo en los análisis y en el modelo, de modo que se pueden actualizar sin tocar el código.

## Tecnologías

- Sitio web: PHP, Bootstrap 5, Highcharts y Leaflet con mapas de OpenStreetMap.
- Los resultados de los análisis y del modelo están en `json/`. El código con el que el equipo los calculó no forma parte de este repositorio.

## Estructura

```
analisis/   páginas de los análisis univariante, temporal, multivariante y geográfico
mod/        página del modelo de predicción por subcircuito
json/       resultados de los análisis y del modelo (tasas, series, ACM, mapa)
comp/       encabezado, pie y plantilla comunes
css/, img/  estilos e imágenes
```

## Cómo verlo en tu computadora

Necesitas PHP 8 o superior.

```bash
git clone https://github.com/Jennovill/Extorsiones.git
cd Extorsiones
php -S localhost:8000
```

Luego abre http://localhost:8000 en el navegador.

## Equipo

Franklin López, Jenny Ochoa, Leonardo Pesantes y Doménica Rocha. Estudiantes de Ingeniería en Estadística, ESPOL.
