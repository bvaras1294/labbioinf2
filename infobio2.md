##Laboratorio 02- Alineamiento de secuencias 

#Parte 1: colectar genes homólogos#

*GEN SRY BASE DE DATOS NCBI*

**¿Que función cumple el gen SRY**

El gen SRY es un gen sin intrones que codifica un factor de transcripción que es miembro de la familia de proteínas de unión a ADN del grupo de alta movilidad (HMG). Esta proteína es el factor determinante de los testículos (TDF), que inicia la determinación del sexo masculino.

**¿Cuantos genes ortólogos están anotados en esa base de datos?**

28 genes ortólogos encontrados en NCI para el gen SRY de humanos (29 genes si se incluye al gen SRY de humanos) 

#Parte 2: Alineamiento múltiple#

**¿Qué es el EMBL-EBI?**

El instituto Europeo de Bioinformática (EMBL-EBI)  proporciona servicios de bioinformática y datos de libre acceso a la comunidad científica.
Desarrollan bases de datos, herramientas y software que hacen posible alinear, verificar y visualizar los diversos datos producidos gracias a la investigación y hacer que la información esté disponible libremente para todos.
 
**¿Cuál es el programa que ellos ofrecen que funciona mejor para secuencias de proteínas?**

El mejor programa para secuencias de Proteinas otorgado por EMBL-EBI es MUSCLE

**¿Qué otros tipos de herramientas ofrece EMBL-EBI?**

Comparación de ontología, alineación de secuencia múltiple, alineación de secuencia por pares, alineación local y global, generación de bibliografía, detección de características de proteínas, DNA back-translation, reconocimiento de motivos de secuencia, búsqueda de similitud de secuencias, análisis de función de proteína, leer mapeo, enriquecimiento de similitud química, formateo, búsqueda en la base de datos, formateo de secuencia, cálculo de propiedades de las proteínas, cálculo de hidropatía proteica, traducción de ADN, predicción de la región codificante, identificación de islas CpG y detección de isochore, Mapeo ID. 

*Utilizar MAFFT*

**¿cuál es el costo de abrir un gap?**

En los valores predeterminados por MAFFT el costo de abrir un gap es de 1.53

**¿Cuál es el costo de extender un gap?**

El costo de extender un gap es de 0.123 como valor predeterminado por MAFFT


**¿Cuál es la longitud total del alineamiento?**

La longitud total es de 1934

**¿Cuál es la especie cuyo gen SRY está más relacionado con el gen SRY de humanos?**

Piliocolobus tephrosceles

![](https://github.com/bvaras1294/labbioinf2/blob/master/infbio2/Captura3.PNG?raw=true)

**¿Cuál es el más lejano?**

las especies Bos indicus, Bison bison ya que entre ellas y humanos hay 12 nodos indicando distintos ancestros, por ende una mayor lejanía.

![](https://github.com/bvaras1294/labbioinf2/blob/master/infbio2/Captura2.PNG?raw=true)

**¿Cuál es la especie cuyo gen SRY es más cercana a la del burro?**

Equus przewalskii

**¿Cómo esperas que sea el alineamiento si el costo de abrir un gap aumenta? ¿Y si disminuye?**

si el costo de abrir un gap aumenta el programa intentara no abrir tantos gaps ya que el costo es muy alto por tanto preferirá otra opción con menos costo, si el costo de abrir gap es menor, el programa intentara abrir gaps por cada mismatch ya que el costo es mínimo y preferirá esta opción ante otras como por ejemplo extender gaps.

**¿Cómo esperas que sea el alineamiento si el costo de extender un gap aumenta? ¿Y si disminuye?**

Si el costo de extender gaps aumenta el programa no va a preferir extender los gaps debido al costo por tanto preferirá abrir gaps en cada mismatch antes de extender el gap. Si el costo de extender gaps es mínimo el programa va a preferir extender el gap antes de abrir gaps por separados.

***Prueba aumentando el costo de abrir gaps cambiando el valor de 1.53 a 2.0***
**¿Cuál fue el efecto de aumentar el costo de abrir un gap en la longitud total del alineamiento?**

 De 1934 disminuye la longitud a 1895 ya que el programa debido a costo de abrir un gap es muy grande preferirá no abrir gaps disminuyendo así el largo del alineamiento. 

**prueba lo mismo pero esta vez disminuyendo al mínimo el costo de extender un gap. Describe cómo cambia el alineamiento**

El alineamiento aumenta a 1953 ya que el costo de extender gaps es mínimo por tanto el programa preferiría extender un gap por cada mismatch que encuentre y en el alineamiento se verán los indels como una extensión del gap, alargando por consecuente la longitud del alineamiento. 

#Parte 3: Diseño de partidores#

*Secuencia codificante (CDS) del gen SRY de humanos 

**Agrega a tu informe una lista de los "LEFT PRIMER" y "RIGHT PRIMER" que obtuviste usando Primer3.**

*RESULTADOS LEFT PRIMER*

LEFT PRIMER  AGAGTGAAGCGACCCATGAA
LEFT PRIMER  TTACAGGCCATGCACAGAGA
LEFT PRIMER  GGATAGAGTGAAGCGACCCA
LEFT PRIMER  AGATGCTGCCGAAGAATTGC
LEFT PRIMER  CGAAGATGCTGCCGAAGAAT

*RESULTADOS RIGHT PRIMER*

RIGHT PRIMER   TCTCTGTGCATGGCCTGTAA
RIGHT PRIMER   CTTGAGTGTGTGGCTTTCGT
RIGHT PRIMER   TTTCTCTCTGTGCATGGCCT
RIGHT PRIMER   GCTTTGTCCAGTGGCTGTAG
RIGHT PRIMER   CTACAGCTTTGTCCAGTGGC

![](https://github.com/bvaras1294/labbioinf2/blob/master/infbio2/Captura4.PNG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/infbio2/Captura%205.PNG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/infbio2/Captura6.PNG?raw=true)

**Indica los partidores forward y reverse que escogiste y explica por qué son la mejor opción para amplificar el gen SRY de humano.**

La mejor opción para hacer el aplicòn del gen SRY de humanos son los partidores Forward primer: Pr0001 y Reverse primer: Pr0002 ya que ambos fueron arrojados por el programa primer 3 como los mejores partidores posibles para el gen SRY de humanos y en los detalles dado por AmplifX de cada partidos todos son buenos tienen los mismos valores para TM y porcentaje de GC, hacemos el valor ara dímeros es 12 y 16 los cuales son unos buenos valores y tienen también el mismo valor para la estabilidad de 3`. en comparación a los otros primers que tenían diferencia en los valores algunas características eran malas en ciertos partidores. 

![](https://github.com/bvaras1294/labbioinf2/blob/master/infbio2/Captura7.PNG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/infbio2/Captura%208.PNG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/infbio2/Captura9.PNG?raw=true)

**¿Cuál es el largo del amplicón? ¿Y la temperatura de annealing sugerida?**

El largo del amplicon es de 191 nucleótidos y la temperatura es de 54ºC
