# Aprende un lenguaje de programación en un día (ejercicio voluntario para subir nota).

## Introducción

Cuando te sacaste el carnet de conducir, aprendiste las normas de circulación así como los fundamentos básicos para manejar un coche: volante, marchas, freno, acelerador, embrague, retrovisores... Seguramente, el coche que conduces ahora es diferente al que utilizaste para aprender a conducir, no obstante, lo puedes llevar sin problema. Cada coche tiene sus peculiaridades, pero quien sabe manejar un automóvil, puede adaptarse a las medidas, tacto y comportamiento de un vehículo en cuestión de horas.

Aprender a programar es como aprender a conducir. Si tienes una base sólida de programación y sabes manejar con soltura los tipos de datos, bucles, arrays, clases, métodos, etc. podrás pasar de un lenguaje a otro en un período relativamente corto, simplemente tendrás que adaptarte a la sintaxis y a las peculiaridades del nuevo lenguaje.

Con este ejercicio se pretende despertar el interés por otros lenguajes de programación distintos al que el alumno está estudiando como primer lenguaje.

Sigue los pasos que se indican a continuación.

## Creación del equipo
Grupo de tres alumnos:
  EasyCodeEasyLife

## Forkea forkea

El representante del grupo debe hacer un *fork* de este repositorio para utilizarlo como base.

## Añadiendo colaboradores

El encargado del grupo deberá añadir como colaboradores del repositorio *forkeado* a los otros dos miembros, para trabajar todos sobre los mismos archivos. Cuando alguien es colaborador en un repositorio, puede hacer *push* a él sin necesidad de pedir permiso o hacer *pull request*.

Para añadir colaboradores hay que hacer click en la pestaña *Settings* y seleccionar luego *Collaborators* en el menú.

## Miembros del grupo

Escribe aquí los miembros del grupo. El primero es el representante o encargado.

* Juan David Villena Gil -Lider-
* Alejandro Caralt Caralt 
* Jesus Vargas Galan 

## Lenguaje de programación

El profesor llevará una cajita llena de papelitos con los nombres de distintos lenguajes de programación. Los encargados de cada grupo meterán la mano en la caja y sacarán dos papelitos, de los cuales el grupo elegirá uno. Se permite hacer intercambio de papelitos entre grupos.

Escribe el lenguaje de programación elegido por el grupo.

* Mi lenguaje

AWK

## Información sobre el lenguaje

AWK es un lenguaje de programación diseñado para procesar datos basados en texto, ya sean ficheros o flujos de datos. El nombre de AWK deriva de las iniciales de los apellidos de sus autores : Alfred Aho, Peter Weinberger y Brian Kernighan.
Es un ejemplo de un lenguaje de programación que usa ampliamente el tipo de datos de listas asociativas y expresiones regulares. Fue una de las primeras herramientas en aparecer en Unix y ganó popularidad como una manera de añadir funcionalidad a las tuberías de UNIX, aunque se puede instalar implementaciones de AWK en casi todos los demás sistemas operativos.
Se creó en 1977 y se actualizó hasta el año 1985. Que cada una de estas actualizaciones crearon dos dialectos el old awk y el awk nawk.Este lenguaje de programación es dinámico, su código es bastante corto, normalmente este lenguaje se usa para escribir programas de una linea (sencillos).
Para editar el código de AWK necesitamos una herramienta simple y básica de UNIX que se llama VI.
Ciertamente, puede no ser tan potente como numerosas herramientas que se pueden usar con la misma finalidad. Pero tiene la enorme ventaja de que, en un tiempo realmente corto, permite escribir programas que, aunque tal vez sean de un solo uso, están totalmente adaptados a nuestras necesidades, que en muchas ocasiones son sumamente sencillas.
Awk es ideal para los propósitos con los que se diseño: leer ficheros línea por línea y procesar en base a los patterns y cadenas que encuentre en ellas.
Ficheros del sistema como el /etc/password y muchos otros, resultan sumamente fáciles de tratar mediante el awk, sin recurrir a nada más.
Y desde luego que awk no es el mejor. Hay varios lenguajes de scripting con capacidades mucho mayores. Pero awk sigue teniendo la ventaja de ser siempre accesible en cualquier instalación, por mínima que esta sea.
## Herramientas de desarrollo

Para usar este lenguaje de programación nesitas el editor de texto VI, Sublime, NANO.

## Poniendo en práctica el lenguaje

Pon en práctica el lenguaje de programación realizando los siguientes ejercicios. Para cada uno de los ejercicios, pega el código fuente de la solución y una captura de pantalla.

### 1. ¡Hola mundo!

```awk
BEGIN { print "Hola mundo!"; exit }
```

### 2. Pirámide

Dada una altura introducida por el usuario, realiza un programa que pinte una pirámide a base de asteriscos con la altura indicada.
```awk
#!/usr/bin/awk -f
# Practicando AWK
BEGIN {
	print "La piramide se construira con distintas piedras dependiendo de su altura(<10='*' ;11-20='🂠'; >21='🀱')"
	print "Introduce la altura de la piramide: "
}
{
	ORS=" "
	altura=$0 
	base=1
	espacios=(altura -1)
	cielo = (altura/10)
	if ( cielo <= 1){simbolo_piramide="*"}
	else if(cielo <=2 ){ simbolo_piramide="🂠"}
	else{simbolo_piramide="🀱"}
}
{
	#Dibujo de Fondo
	c_fondo="\033[1;44;30m"
	c_piramide="\033[1;43;33m"
	c_tierra="\033[0;43;33m"
	c_blanco="\033[1;44;37m"	

	print c_fondo
	print c_blanco"☁☁☁☁" 
	print c_fondo"   "
	print c_blanco"--✈" 
	print c_fondo"    " 
	print c_blanco"☁☁☁☁☁" 
	print c_fondo"      "
	print "\033[1;44;33m☀" 
	for(i = 0; i < cielo; i++){
		print c_blanco"☁☁☁☁"
		print c_fondo"     " 
		print c_fondo"    "
		print c_blanco"☁☁☁☁" 
		print c_fondo"   "
		print c_blanco"☁☁"
		print c_fondo"  "
		print c_blanco"☁☁☁"
	}
	print c_fondo"    \n"

	print c_blanco"☁☁☁☁☁☁"
	print c_fondo"     "
	print c_blanco"☁☁☁☁"
	print c_fondo"  "
	print c_blanco"☁☁☁" 
	for(i = 0; i < cielo; i++){
		print c_blanco"☁☁☁☁"
		print c_fondo"     " 
		print c_blanco"♈" 
		print c_fondo"    " 
		print c_blanco"☁☁☁☁" 
		print c_fondo"   "
		print c_blanco"☁☁"
		print c_fondo"  "
		print c_blanco"☁☁☁"
	}
	print c_fondo"          \n"

	print c_blanco"☁☁☁☁"
	print c_fondo"     " 
	print c_blanco"♈" 
	print c_fondo"    " 
	print c_blanco"☁☁☁☁" 
	print c_fondo"   "
	print c_blanco"☁☁"
	print c_fondo"  "
	print c_blanco"☁☁☁"
	for(i = 0; i < cielo; i++){
		print c_blanco"☁☁"
	print c_fondo"    "
	print c_blanco"♈"
	print c_fondo"          "
	print c_blanco"☁☁☁☁☁☁☁☁☁"
	}
	print c_fondo"  \n"

	print c_blanco"☁☁"
	print c_fondo"    "
	print c_blanco"♈"
	print c_fondo"          "
	print c_blanco"☁☁☁☁☁☁☁☁☁"
	for(i = 0; i < cielo; i++){
		print c_blanco"☁☁☁☁"
		print c_fondo"     " 
		print c_blanco"♈" 
		print c_fondo"    " 
		print c_blanco"☁☁☁☁" 
		print c_fondo"   "
		print c_blanco"☁☁"
		print c_fondo"  "
		print c_blanco"☁☁☁"
	}
	print c_fondo"    \n"

	print "        "
	print c_blanco"♈"
	print c_fondo"           "
	print c_blanco"☁☁☁☁☁"
	for(i = 0; i < cielo; i++){
		print "        "
		print c_blanco"♈"
		print c_fondo"           "
		print c_blanco"☁☁☁☁☁"
	}
	print c_fondo"     \n"
}
{
	#Piramide
	for (i = 0; i < altura; i++){
		for (u = 0; u <= espacios; u++){
		print c_fondo" "
		}
		for (relleno = 1; relleno <= base; relleno++){
		print c_piramide simbolo_piramide
		}
		print c_fondo"\n"
		base+=2
		espacios-=1
	}
	exit
}
```


### 3. Arrays y números aleatorios

Realiza un programa que rellene un array (o una estructura similar) con 20 números enteros aleatorios entre 1 y 100 y que seguidamente los muestre por pantalla. A continuación, se deben pasar los números primos a las primeras posiciones del array y los no primos a las posiciones restantes. Muestra finalmente el array resultado.
```awk
BEGIN{
	ORS = " "
	array_original[20]
	array_primos[20]
	array_noprimos[20]
	contador_primos = 1
	contador_noprimos = 1
	primo = 0
	c_piramide="\033[1;43;37m"
	c_blanco="\033[1;44;37m"
	c_color="\033[1;40;37m"

	print "Array Original:   "
	for(i = 1; i < 20; i++){
		array_original[i] = int(rand() * 100 + 1)
		printf c_color"%4d",array_original[i]
		for(u = 2; u < array_original[i]; u++){
			if((array_original[i] % u) == 0){
				primo = 1
			}
		}
		if(primo == 0){
			array_primos[contador_primos] = array_original[i]
			contador_primos++
		}
		if(primo == 1){
			array_noprimos[contador_noprimos] = array_original[i]
			contador_noprimos++
		}
	primo = 0
	}
	print "\033[0;30;37m \nArray Modificado: "
	for(i = 1; i < contador_primos; i++){
		printf c_piramide"%4d",array_primos[i]
	}
	for(i = 1; i < contador_noprimos; i++){
		printf c_blanco"%4d",array_noprimos[i]
	}
print "\033[0;30;37m \n"
exit
}
```
	

## Presentación de resultados

En este trabajo hemos aprendido los conceptos básicos de la programación con AWK que es un lenguaje muy antiguo el cual se usa para el tratado de texto (filtro de texto), Haciendo una comparación con java vemos que hay alguna similitud en la estructura pero solo con el dialecto más reciente.
El tutorial que hemos seguido para aprender un concepto básico de AWK ha sido mediante videos de youtube y de una pagina que viene con muchos ejemplos y gran temario cuya dirección es: ftp://ftp.gnu.org/old-gnu/Manuals/gawk-3.0.3/html_chapter/gawk_toc.html

## Recompensa

* Todos los alumnos que realicen correctamente la actividad tendrán 0'25 puntos extra en la nota del trimestre.

* Los miembros del equipo más votado ganarán un premio.

:star: Si te ha gustado este ejercicio, dale una estrellita al [repositorio original](https://github.com/LuisJoseSanchez/aprende-un-lenguaje-en-un-dia).

