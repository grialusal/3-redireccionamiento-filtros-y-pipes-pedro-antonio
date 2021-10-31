# Sesión III - Redireccionamiento, filtros y pipes

Herramientas computacionales para bioinformática: UNIX, expresiones regulares y shell script

Edita esta plantilla en formato markdown [Guía aquí](https://guides.github.com/features/mastering-markdown/) como se pide en el guión. 
Cuando hayas acabado, haz un commit de tus cambios y súbelos al repositorio antes de la fecha de entrega señalada. 

======================================


## Ejercicio 1
`sort -R` (random) desordena las líneas de un fichero. Prueba a desordenar el fichero `gene-2.bed` y crea un nuevo fichero llamado `gene-2-desordenado.bed`.

Trata ahora de ordenar este fichero de acuerdo a los siguientes criterios: 
1. Sin cortar los elementos
2. En orden descendente
3. Usando a la vez la tercera y la segunda columna (en este orden de prioridad). Consulta el manual para ver la opción -k. 

### Respuesta ejercicio 1
En primer lugar se crea un fichero llamado "gene-2-desordenado.bed" a partir del comando sort -R ejecutado sobre el fichero `gene-2.bed`. Se ha empleado el comando: 
`sort -R gene-2.bed > gene-2-desordenado.bed`
Tras esto empleamos cat para ver el contenido del fichero `gene-2.bed` y del fichero desordenado que se ha creado en nuestra carpeta `gene-2-desordenado.bed`
![sortR](images/sortR.png)

Para ordenar el fichero creado `gene-2-desordenado.bed` siguiendo los pasos del ejercicio. Dado que no hay que cortar elementos, no emplearemos el comando `cut`. 
En segundo lugar para ordenar números en orden descendente emplearemos el comando:
`sort -nr gene-2-desordenado.bed`
Y para ordenar usando la tercera y segunda columna según el orden de prioridad emplearemos el comando: 
`sort -k3,4 gene-2-desordenado.bed `
Antes de esto hemos consultado el manual para ver como se emplearia la opción -k de sort: 
`man sort`

![manShortK1](images/manShortK1.png)
![manShortK2](images/smanShortK2.png)

Empleando los dos comandos a la vez nos quedaría así:
`sort -nr -k3,2 gene-2-desordenado.bed`
Con esto nos ordenará el fichero en orden descendente usándo la tercera columna para ordenar valores y después emplea la segunda columna.
 
![sortNRK](images/sortNRK.PNG)




## Ejercicio 2

Cuáles son y cuántos tipos distintos de "features" hay en `Drosophila_melanogaster.BDGP6.28.102.gtf` y en `Homo_sapiens.GRCh38.102.gtf.gz`? Nota: para trabajar con ficheros .gunzip sin descomprimir puedes usar `zcat`.

### Respuesta ejercicio 2


## Ejercicio 3

Recuerdas `covid-samples.fasta`? Localízalo en tu HOME, y extrae, usando un pipeline, los nombres de las secuencias contenidas en este fichero. Luego saca la primera palabra de cada una, ordénalas y guárdalas en un fichero `covid-seq-names.txt`.

### Respuesta ejercicio 3


## Ejercicio 4

Encuentra, usando una sola línea, el número de usuarias diferentes que tienen al menos una carpeta a su nombre en el '/home' de CPG3.

### Respuesta ejercicio 4





