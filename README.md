# MovieLens#
## Aprendizaje NO Supervisado
### Marcelo LEON
### Cohorte OMEGA
#### DiploDatos 2019 - FAMAF

### Notebook
* MovieLens.ipynb 

### Carpetas
* ./data/    ::Contiene los dataset que se utilizaron en el análisis (MovieLens 20M Dataset).
    -movies.csv, lista de películas
    -ratings.csv, películas vistas por usuarios y calificación asignada
* Descargados de https://grouplens.org/datasets/movielens/.

## Resumen

**1. Conatmos con un dataset de más de 27mil películas, estrenadas entre 1891 y 2015 perteneciente a diversos géneros predominando el DRAMA y en menor medida la COMEDIA.
2. Tenemos, además, 20 milloes de calificaciones de usuarios que vieron estas películas. Son algo menos de 140mil usuarios, viendo en promedio 144 pelis cada uno.
3. La calificación media por Peli es 3.1.
4. Por una cuestión de performance vamos a considerar SOLO películas que hayan obtenido un Rating promedio de 4 en adelante. Quedan algo mas de 1700 películas películas con 3 millones de calificaciones. 
4. Vamos a aplicar el algoritmo APRIORI para identificar reglas en este subconjunto de visualizaciones, considerando:
* Nuestros TICKET será cada USUARIO y los ITEMS las películas que rankeó
* Tenemos de 135mil usuarios/ticket de donde extraeremos asociaciones entre películas con los siguientes criterios:

* Ambas películas deben haber sido vistas, en conjunto, por al menos en el 0.01% de los usuarios (1300 aprox), podría ser menos pero implica mucho tiempo de proceso. (Soporte)
    
    **La peli recomendada debe haber sido vista por el 50% de los usuarios que vieron la otra peli, al menos. (Confianza)

