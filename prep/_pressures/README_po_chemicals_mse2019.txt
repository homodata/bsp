po_chemicals: Chemical pollution 
Capa de datos: Contaminación química modelada dentro de la ZEE por tráfico de embarque comercial, transporte marítimo y puertos, uso de pesticidas terrestres (contaminación orgánica) y escorrentía urbana (contaminación inorgánica). 

1. Institución recolectora original (cuál institución hizo la recolección de los datos de su fuente).
- Centro Nacional para Análisis y Síntesis Ecológico (NCEAS). https://mazu.nceas.ucsb.edu/data/
	Mapas: 	https://knb.ecoinformatics.org/view/doi:10.5063/F19021PC 
		https://knb.ecoinformatics.org/view/doi:10.5063/F1DR2SDD

2. Institución que provee los datos a este Proyecto (si es distinta de la recolectora).
- Índice de Salud del Océano (OHI) http://ohi-science.org/
 
3. Citas detalladas de la fuente, si se trata de uno o más artículos científicos.
Halpern, B.S., Frazier, M., Potapenko, J., Casey, K.S., Koenig, K., Longo, C., Lowndes, J.S., Rockwood, R.C., Selig, E.R., Selkoe, K.A. & Walbridge, S. (2015). Spatial and temporal changes in cumulative human impacts on the world’s ocean. Nature Communications, 6, 7615. URL: https://knb.ecoinformatics.org/view/doi:10.5063/F1S180FS

4. Método de captura de los datos. Si fue un Estudio realizado para obtener esos datos, si se hizo utilizando algún instrumento de medición, cuál método se aplicó, si se utilizó una encuesta o formulario para recogerlos, etc.
1. Descarga y análisis de la información ráster global disponible enfocada en el área de estudio desde 2009 hasta 2013.
2. Determinación de los valores anuales promedio establecidos en la base de datos del IdSO y reescalamiento con el valor máximo anual conforme lo establecido en la metodología global.
3. Elaboración de los mapas temáticos.

5. Período de tiempo que cubren los datos (año desde y año hasta). O enumeración de años si no son consecutivos.
2009-2013
Años escenarios	Años de datos
2009			2009
2010			2010
2011			2011
2012			2012
2013			2013
2014			2013
2015			2013
2016			2013
2017			2013
2018			2013
2019			2013

6. Unidad en la cual vienen los valores.
Adimensional

7. Significado o explicación de qué significan los valores.
Datos modelados de la contaminación de origen orgánica, inorgánica y oceánica en cada región en comparación con la mayor concentración encontrada en cada región y año.

8. Observación o comentario sobre los datos.


9. Significado y explicación de las columnas que se incluyen en el archivo
Los datos de la primera columna indican el nombre de cada provincia, que en el caso de la evaluación del IdSO Manabí y Santa Elena, corresponde a las provincias respectivas.
La segunda columna son los años de datos representados por archivos raster.
La tercera columna presenta el promedio de los datos de contaminación química en la Zona Económica Exclusiva de cada provincia.
La cuarta columna contiene el valor máximo de contaminación química por región y año.
La quinta columna presenta el puntaje de presión correspondiente a cada región y año, el cual es el resultado de la reescalación de los promedios de cada provincia con el valor máximo registrado. 
La sexta columna es el valor de estado que corresponde a la operación numérica 1 menos presión.

Provincia	Año	Presión promedio 	Presión máxima		Presión		Estado
				A			B		C=A/B		1-C
Manabí		2009		0.15			0.93		0.16		0.84
		2010		0.15			1.00		0.15		0.85
		2011		0.15			1.00		0.15		0.85
		2012		0.15			1.00		0.15		0.85
		2013		0.39			1.00		0.39		0.61
Santa Elena	2009		0.28			1.00		0.28		0.72
		2010		0.32			1.00		0.32		0.68
		2011		0.30			1.00		0.30		0.70
		2012		0.28			1.00		0.28		0.72
		2013		0.37			1.00		0.37		0.37	
