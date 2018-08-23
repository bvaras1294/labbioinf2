##Laboratorio 03- Ensamblaje de genomas y predicción de genes

#parte 1: El artículo genoma#

*Comencemos por ir a Genomes On Line Database (GOLD) . GOLD es una base de datos de proyectos de secuenciación de genomas y metagenomas.*

**¿Cuántos Sequencing Projects y Analysis Projects hay depositados en GOLD? ¿Cuál es la diferencia entre ambos?**

Hay 215.214 para sequencing Projects y 174.546 analysis projects depositados en GOLD.
Se diferencian entre si ya que Sequencing projects es una plataforma para subir proyectos de secuencia de una muestra o organismo individual, a partir de una única muestra se pueden realizar múltiples proyectos de secuenciación.
En cambio Analysis projects es el procesamiento informático de un proyecto de secuenciación. Describe como se realizó el proyecto de secuenciación.

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura23.PNG?raw=true)

**¿Cuál es el dominio más representado en la base de datos, archea, bacteria, eukaryote, o virus?**

El dominio más representado en la base de datos es bacteria  con un total de 111.074 representaciones al 2018. 

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura24.PNG?raw=true)

**¿Cuáles son los phyla más representados entre los proyectos de genomas bacterianos en la base de datos?**

De los proyectos de genomas bacterianos la distribución filogenéticas más representada son proteobacteria con un 37,3% de proyectos, después siguen todos las demás filogenias con un 29,2% de proyectos, sobre las filogenias firmicutes y actinobacteria que tienen un 23,6% y un 9,9% respectivamente de proyectos.

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura25.PNG?raw=true)
 
**¿A qué tipo de proyectos pertenece la mayor cantidad de genomas bacterianos depositados en GOLD? (tipo de proyecto, se refiere al tópico de la investigación, por ejemplo, salud humana, ambiental, etc.)**

La mayor cantidad de genomas bacterianos depositados en GOLD son para proyectos de tipo médicos. con un 58,9% ( equivalente a 41.708 genomas) sobre los otros tipos de proyectos. 

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura26.PNG?raw=true)

*A continuación, vamos a trabajar con el genoma del Bonobo (Pan paniscus)*

**¿Cuál es el artículo original del genoma? (en el cual se reporta la secuenciación y ensamble del genoma)**
The bonobo genome compared with the chimpanzee and human genomes. Prüfer K, et al. Nature 2012 Jun 28

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura.JPG?raw=true)

[https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3498939/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3498939/)

**Explica, qué es el N50, L50, y NG50.**

Son estadísticas de longitudes que se pueden usar en bioinformática. Se usa ampliamente en el ensamblaje de genomas para medir contig de las secuencias. 
Para evaluar la calidad del ensamblaje se utiliza N50 que es la mediana, los coting se deben ordenar y y dividir por la mitad la distribución de las bases totales, el contig que este justo en la mitad tendrá una longitud y donde esto ocurre es N50.
L50 es la cantidad de contigs que sumados hacen N50. 
Ya que N50 se calcula poniendo en contexto el tamaño del conjunto en vez del tamaño del genoma. NG50 es igual a N50 con la excepción de que el 50% del tamaño del genomas es conocido o estimado debe ser de la longitud de NG50.

**¿Cuál es el propósito de calcular estas estadísticas?**

Tener referencia de longitudes de contig dentro de un ensamblaje, sirve para medir la calidad del ensamblaje. 

**¿Cuántos contigs conforman el genoma del Bonobo? ¿Cuál es el N50 y L50 del genoma? (responde basado en los contigs)**

El genoma del Bonobo esta formado por 121,356 contigs. Basado en contigs N50 es 66,676 y L50 es 11,048 del genoma. 

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura28.PNG?raw=true)

**¿Cuál es el largo total y porcentaje de GC del genoma del Bonobo? ¿Qué quieren decir o qué indican éstos valores?**

El largo total del genomas es de 3286,64 Mb. y con un porcentaje de GC de 42.3185
El valor del largo total del genoma indica que la secuencia total del genoma tiene 3286,64 millones de bases. y el porcentaje de GC indica la cantidad de guanina y citosina los enlaces GC se unen por tres enlaces de hidrogeno y es más resistente por ejemplo a la desnaturalización y se debe tener en cuenta esta característica en el genoma, se representa como porcentaje porque es la cantidad de GC en el genoma que está siendo investigado.

**¿Qué tipo de tecnología se usó para secuenciar el genoma del Bonobo? ¿Qué método (programa o algorítmo bioinformático) se usó para ensamblar el genoma?**

para secuenciar el genoma del bonobo se realizó en la plataforma de secuenciación 454. El genoma se ensamblo utilizando el software de ensamblaje Celera Assembler. y además se secuencio 19 individuos de bonobo en la plataforma Illumina GAIIx. 

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura29.PNG?raw=true)

#Parte 2: Predicción de genes#

*En esta parte vamos a utilizar un programa clásico para predecir los genes ORFfinder.*
*Predecir qué gen (es) está (n) codificado (s) en la secuencia a continuación.*

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura30.PNG?raw=true)

**Describe los resultados obtenidos. ¿Cuántos ORFs o genes encontraron ORFfinder? ¿En qué hebra están codificados? ¿De qué largo son los ORFs predichos? ¿Algunos de ellos se sobreponen (fíjate en la posición de inicio [ inicio ] y término [ stop ])?**

Se encuentran 7 ORF o genes, para la secuencia puesta en ORFfinder.
ORF1,ORF3,ORF2 se encuentran en la hebra **+**
ORF4,ORF5,ORF7,ORF6 se encuentran en la hebra **-**
ORF1 tiene un largo de 909 nucleótidos, ORF2 tiene un largo de 78 nucleótidos, ORF3 tiene un largo de 99 nucleótidos, ORF4 tiene un largo de 441 nucleótidos, ORF5 tiene un largo de 405 nucleótidos, ORF6 tiene un largo de 84 nucleótidos, ORF7 tiene un largo de 144 nucleótidos. 
ORF 7 se encuentra sobrepuesto en ORF1, ORF 6 Y ORF2 està sobrepuesto en ORF4 y ORF3 se sobreponen a ORF5.

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura31.PNG?raw=true)

**¿Qué tipo de programa es OR Finder, Ab initio o por homología**

ORFfinder es un programa tipo AB initio ya que a partir de una secuencia de ADN, busca señales de presencia de un gen o regiones de interés. En cambio, los programas de homología realiza una búsqueda en bases de datos curadas. 

*Finalmente, vamos a usar BLAST para hacer una búsqueda de la secuencia completa y de cada uno de los ORFs predichos por ORFfinder.* *Primero, usa blastn ( Nucleótido BLAST ) para consultar la secuencia completa. Segundo, usa blastx ( nucleótido traducido> proteína ) para consultar cada uno de los ORFs predichos.*

 **¿A qué organismo pertenece la secuencia en cuestión?**

Pertenece a Heamophilus influenzae con un 100% de identidad según BLAST.

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Capturasada%C3%B1sldka.JPG?raw=true)

**¿Qué gen (s) está (n) codificados en la secuencia?**

En la secuencia se codifican 3 dominios conservados un FdHE superfamily, un NAT_SF superfamily y DNA_III_psi superfamily. Se ven 3 genes para esta secuencia 2 en la hebra **-** y uno en la hebra **+**. 

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura6.JPG?raw=true)

**Tomando en cuenta la evidencia que acumula usando ORFfinder y BLAST. ¿Cuál es el origen de los ORFs predichos por ORFfinder dirías tú que son o es el correcto (s)?** 
Los ORF correctos predichos por ORFfinder son ORF1, 0RF4 Y ORF5.
ya que para la secuencia analizada en blast se tienen 3 dominios conservados FdHE superfamily RF +1 por tanto está en la hebra **+** ubicado entre 1 a 900  de la hebra **+**, NAT_SF superfamily ubicado sobre los 900 hasta 1380  y DNA_III_psi superfamily ubicado en 1390 a 1700. 
Y en evidencia otorgada por blast al analizar cada ORF se tiene que ORF1 corresponde a FdhE superfamily y en segun ORFfinder la secuencia inicia en 1 y termina en 909 de la hebra **+** y coincide en un 100% de identidad con formate dehydrogenase perteneciente a Heamophilus influenzae. ORF4 corresponde a NAT_SF superfamily y según ORFfinder la secuencia inicia en 1388 y termina en 948 de la hebra **-** y coincide en un 100% con péptido N-Acetiltransferasa perteneciente a Heamophilus Influenzae. ORF5 corresponde a  DNA_III_psi superfamily segun ORFinder la secuencia inicia en 1795 y termina en 1391 de la hebra **-** y coincide en un 100% con DNA polymerase III perteneciente a Heamophilus influenzae. Es por esto que estos tres ORF son considerados correctos para la secuencia, ya que además toman todo el largo de la secuencia en conjunto. 

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Capturadfg.JPG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura%2010.JPG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura11.JPG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura%2017.JPG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura33.PNG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura%2034.PNG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Capturadfsgsf.JPG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura13.JPG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf3/Captura14.JPG?raw=true)



