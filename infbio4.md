##Laboratorio 04- Filogenética Molecular 

#Plataforma Phylogeny.fr y preparación de datos#

**¿Qué ofrece o para qué sirve el portal Phylogeny.fr?**

Phylogeny.fr es un servicio web dedicado a la reconstrucción y análisis de relaciones filogenéticas entre distintas secuencias moleculares. Utiliza varios programas bioinformáticos para reconstruir un árbol filogenético a partir de un conjunto de secuencias.

**Nombra y explica brevemente los 3 modos en los que se puede ejecutar el pipeline de Phylogeny.fr.**

los tres modos que existen son One click, modo avanzado y a la carta.

El *modo One Click* está enfocado a usuarios que no se ocupan en la selección de programas y/o parámetros. Es decir, vienen valores por defecto, este modo ya está configurado para ejecutar y utilizar programas según su precisión y velocidad para reconstruir un árbol filogenético robusto a partir de un conjunto de secuencias.

En el *Modo avanzado*, es una la sucesión de los diferentes programas que ofrece el servidor, pero aqui los usuarios pueden elegir los pasos a realizar y las opciones de cada programa.

El *modo a la carta* permite ejecutar y probar más programas de alineación y filogenia, como MUSCLE , ClustalW , T-Coffee , PhyML , BioNJ , TNT , entre otros...

**Menciona qué tipos de análisis se pueden realizar en el portal de acuerdo a la documentación. (Online Programs)**

De acuerdo con la documentación los programas on line utilizan análisis de Filogenia utilizando máxima verosimilitud, Filogenia usando parsimonia, Filogenia bayesiana, Filogenia usando distancias

**Incluye en tu informe una captura de pantalla de las dos filogenias que inferiste. Recuerda que tu nombre completo debe aparecer en la imagen de cada filogenia (Name of the analysis).**

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf4/Captura%202.PNG?raw=true)
![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf4/Captura1.PNG?raw=true)

**¿A qué se refiere el paso de Alignment curation y para qué sirve?**

Se refiere a curación de la alineación, debido a que las  filogenias son una inferencia, se ocupa la curación como una forma de refinar las alineaciones de esta forma se  Eliminan posiciones mal alineadas y se disminuye el ruido de la alineación. 

**¿Cuál es la diferencia entre BioNJ y Neighbor?**

Ambos son para reconstruir filogenias utilizando distancia, la diferencia es que el número de taxa para la matriz de distancia en neighbor es de 500 y en BioNJ es de 5000.

*Corre nuevamente ambas filogenias, pero esta vez sin seleccionar Alignment curation*

**Incluye en tu informe una captura de pantalla de las dos filogenias que inferiste (sin Alignment curation). Recuerda que tu nombre completo debe aparecer en la imagen de cada filogenia (Name of the analysis).**

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf4/Captura%203.PNG?raw=true)

![](https://github.com/bvaras1294/labbioinf2/blob/master/bioinf4/Captura%204.PNG?raw=true)

**¿Cuál es el efecto de no hacer la curación del alineamiento en las filogenias?**

Son alineaciones no revisadas por consecuente en las filogenias quedan posiciones mal alineadas y un mayor ruido dentro de estas.  

**Describe las diferencias entre las filogenias que has estimado (4 en total): cantidad de grupos monofiléticos, relaciones que potencialmente cambiaron, etc**

en la filogenia estimada con probcons y que se le realizó una curación en la alineación, la relación entre *puma concolor* y *vulpes vulpes* pertenecen al mismo ancestro en cambio en a alineación no curada estas pierden el ancestro común se pierde el grupo monofilético. se ve un aumento de distancia evolutiva en la alineación curada. Además, se puede ver un cambio en la relación de *pteropus alecto* el cual en la filogenia no curada pierde el ancestro común que tenía con el grupo al cual pertenecia en la filogenia si curada. se observa un cambio en la relación entre *chlorocebus sabaeus*, *macaca mulatta* y *piliocolobus tephrosceles* ya que en la filogenia curada se encuentran todos en el mismo grupo, pertenecientes a un ancestro y en la filogenia no curada se separan. 

Para la filogenia realizada con clustalW se observan mayores cambios, ya que en su gran mayoría en la filogenia de culstalw no curada se separan y desordenan la mayoría de los grupos relaciones en la filogenia curada como por ejemplo *Equus przewalskii* con *Equus asinus* en la filogenia no curada quedan pertenecientes a un ancestro diferente que en la filogenia curada. otro ejemplo es *rhnopithecus roxelana* con *rhin t* en que se encuentran en un mismo grupo monofilético en la filogenia curada y en a filogenia no curada se encuentra separados.

