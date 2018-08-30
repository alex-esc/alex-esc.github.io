# Notas digitales




---


## Notas simples y flexibles

![](https://i.imgur.com/reoV9VD.png)


---



La pregunta numero uno que me hacen mis compañeros es ¿como haces que tus notas se vean así? la respuesta corta es _Markdown_. 


---


hay 3 partes principales de mi sistema de notas: El texto original, Documento en PDF y un respaldo en mi pagina web. Esta guía te enseñara como duplicar mi estilo de notas.

---


Una parte importante de tomar todos tus apuntes digitales es la **eliminación de distracciones**.

---

Por eso en mi método no usaremos word o pages o drive en particular, este método te permite trabajar en cualquier editor de texto sin tener que pelear con menús, solo tu y tu teclado.

---




## Como usar Markdown

Como mencione al principio usaremos Markdown (o "md" por su extensión), este no es un nuevo programa por aprender, markdown es solo sintaxis. La meta de md es simple: ser fácil de leer en cualquier dispositivo y en cualquier programa.

---



	# Integrales y derivadas

	La derivadas son una relación de diferencia de cambio de una curva.

	Las integrales son la reversa de integrales, una buena forma de visualizar integrales es pensando en el área debajo de la curva.

	![Curva en rojo y área en gris](https://matplotlib.org/1.4.2/_images/integral_demo.png)

	**Formulas de derivadas**

	_basica:_

---

	

	# Esto es un titulo

	## Esto es un sub-titulo

	### subtitulo nivel 3

	#### subtitulo nivel 4

	##### subtitulo nivel 5

	###### subtitulo nivel 6

	####### subtitulo nivel 7

	######## solo puedes hacer 8 sub niveles de titulo


---


	
	Esto es texto normal, pero **esto esta en negritas** y _esto en itálicas.

	Deja una linea entre renglones para iniciar un nuevo párrafo.


---


	
	[Esto es un link y te lleva a wikipedia](https://www.wikipedia.org/)

	y abajo hay un link a una foto, agragar un '!' antes del link te mostrara la foto. (como la gráfica de integrales en el primer ejemplo)

	![Esto son notas de la foto, pueden estar vacías.](https://upload.wikimedia.org/wikipedia/commons/d/de/Wikipedia_Logo_1.0.png)

	La foto de arriba es el logo de wikipedia.


---


	
	* Esto es una lista de puntos
		* sub punto
		* otro
	* otro punto principal
		* sub punto
			*sub-sub punto
			
	1. Esto es una lista enumerada
	1. Numero dos
	1. Numero tres
	1. No es nesesario poner el numero correcto, al transformarlo a word o pdf se enumeraran solos

---


Entonces para usar markdown solo abre un editor de texto, el que tu quieras y escribe siguiendo estas reglas, no olvides guardar tu documento con la terminación '.md' para guardarlo como archivo markdown. Archivo -> Guardar como -> escribe el nombre del documento y agrega '.md' al final.

---


## Grandes ventajas de markdown

---


**Markdown te permite hacer PDFs, documentos de word y paginas web en cualquier dispositivo**


---

Como un extra, también puedes transformar tus documentos de markdown a una presentación de Powerpoint 


---


Cuando termines tus notas y quieras convertirlas a PDF, word o pagina web solo abre la carpeta con tus notas y usaras un programa llamado **pandoc** para hacer la trasformación.

---


## Como transformar tus documentos usando Pandoc

usaras la linea de comandos...

---



No te preocupes,  _solo necesitas saber copiar y pegar._

---


### Paso uno, instala Pandoc

Guía de instalación de pandoc en [PC](http://www.texts.io/support/0004/), [Mac](http://www.texts.io/support/0003/) y [linux](https://pandoc.org/installing.html#linux)

Si tienes problemas la pagina oficial de Pandoc esta [aquí](https://pandoc.org/installing.html)

---


### Paso dos, localiza tu documento a transformar

Abre la carpeta donde guardas tu documento, recuerda que termina en '.md', luego abre la terminal en esa carpeta:

* En Windows has click derecho en el espacio en blanco y preciosa la tecla shift al mismo tiempo y selecciona a abrir Powershell aquí. ([mas info](https://www.addictivetips.com/windows-tips/open-powershell-in-a-specific-location/))

* En Mac ve a preferencias , teclado, atajos, servicios y activa New Terminal at Folder, luego de esto podrás hacer click derecho en cualquier folder y en servicios habrá una opción para abrir nueva terminal aquí. ([mas info](https://lifehacker.com/launch-an-os-x-terminal-window-from-a-specific-folder-1466745514))

* En linux (Ubuntu) preciona Ctrl + Alt + T y pega este texto "sudo apt-get install nautilus-open-terminal" (sin comillas), esto instalara el menú de abrir en terminal, reinicia tu computadora y has click derecho en cualquier archivo y selecciona abrir en terminal. ([mas info](https://www.howtogeek.com/192865/how-to-open-terminal-to-a-specific-folder-in-ubuntus-file-browser/))

---



### Ultimo paso, transforma tu documento


---


#### Transformar a PDF

Si quieres convertir de Markdown a PDF copia y pega lo siguiente en la terminal.

	pandoc EL_NOMBRE_DE_TU_ARCHIVO.md -f markdown -o EL_NUEVO_NOMBRE_DE_TU_ARCHIVO.pdf
	
Recuerda cambiar "EL_NOMBRE_DE_TU_ARCHIVO" por el nombre de tu archivo y "EL_NUEVO_NOMBRE_DE_TU_ARCHIVO" por el nombre del PDF que vas a producir.


---



#### Transformar a una pagina web

Si quieres convertir de Markdown a HTML (el formato de las paginas web) copia y pega lo siguiente en la terminal.

	pandoc EL_NOMBRE_DE_TU_ARCHIVO.md -f markdown -o EL_NUEVO_NOMBRE_DE_TU_ARCHIVO.html
	
Recuerda cambiar "EL_NOMBRE_DE_TU_ARCHIVO" por el nombre de tu archivo y "EL_NUEVO_NOMBRE_DE_TU_ARCHIVO" por el nombre del archivo HTML que vas a producir. Para publicar este acrhivo en internet necesitas una pagina web que te permita subir los archivos que quieras como [neocities](https://neocities.org/) y [github pages](https://pages.github.com/), para agregar estilo a tu pagina lee [esta guía](https://jblevins.org/log/custom-css).


---



#### Transformar a un documento de word

Si quieres convertir de Markdown a docx copia y pega lo siguiente en la terminal.

	pandoc EL_NOMBRE_DE_TU_ARCHIVO.md -f markdown -o EL_NUEVO_NOMBRE_DE_TU_ARCHIVO.docx
	
Recuerda cambiar "EL_NOMBRE_DE_TU_ARCHIVO" por el nombre de tu archivo y "EL_NUEVO_NOMBRE_DE_TU_ARCHIVO" por el nombre del archivo de word que vas a producir.

Veremos como transformar a Powerpoint mas adelante...

---



## Markdown avanzado

---


### Comentarios


	### Comentarios

	<!-- Recuerda corregir ortografía -->

	Para escribir un comentario, primero escribe '<!--' luego tu comentario, cuando termines tu comentario escribe '-->'. Un comentario es texto que no se mostrara cunado el archivo markdown sea transformado a word, PDF o cualquier otro formato.


---


#### Escribir ejemplos de código


Esto es código como texto:

public class HelloWorld
{
	public static void main(String[] args) {
		System.out.println("Hello World!");
	}
}

Esto es código tabulado:

	public class HelloWorld
	{
		public static void main(String[] args) {
			System.out.println("Hello World!");
		}
	}

---


#### Citas


Cita como texto:

Life is like riding a bicycle. To keep your balance, you must keep moving.

- Albert Einstein


Cita con '>':

> Life is like riding a bicycle. To keep your balance, you must keep moving.
>
>  Albert Einstein

---


#### Como escribir símbolos especiales


	$\pi$ y $\Delta$

---


#### Escribir ecuaciones y modo matemáticas

$Math Mode$


---


##### Matemáticas entre texto

> Escribir esto:

	La famosa formula de Einstein es $E = MC^2$ , Parte de la teoría de la relatividad, conocida como Equivalencia entre masa y energía.

> Produce esto:

La famosa formula de Einstein es $E = MC^2$ , Parte de la teoría de la relatividad, conocida como Equivalencia entre masa y energía.

---


##### Matemáticas por si solas


Para escribir una ecuación por si sola tienes que usar dos $ arriba y abajo de la ecuación, ejemplo:

> Escribir esto:

	Esta es la famosa formula de Einstein

	$$
	E = MC^2
	$$ 
	
	Forma parte de la teoría de la relatividad, conocida como Equivalencia entre masa y energía.

> Produce esto:

Esta es la famosa formula de Einstein

$$
E = MC^2
$$ 

Forma parte de la teoría de la relatividad, conocida como Equivalencia entre masa y energía.


---


##### Múltiples ecuaciones alineadas 


	$$
	\begin{align*}
	y(x) &= x\\
	y(x) &= x^2\\
	y(x) &= e^x\\
	y(x) &= sen(x)
	\end{align*}
	$$


$$
\begin{align*}
y(x) &= x\\
y(x) &= x^2\\
y(x) &= e^x\\
y(x) &= sen(x)
\end{align*}
$$

##### Formato de matemáticas de LaTeX

Todas las matemáticas en md se escribes en LaTeX, todas las ecuaciones siguen este formato:
---



###### Números, sumas, restas y multiplicaciones


	$$
	2 + 2 = 5 - 1 * 1
	$$

> Produce esto:
	
$$
2 + 2 = 5 - 1 * 1
$$

---


###### Divisiones


	$$
	\frac{1}{2}
	$$

> Produce esto
	
$$
\frac{1}{2}
$$

---

	
###### Exponentes y subindices


	$$
	x^{2 \alpha} - z^w = y_{ij} + y_{ij} - z_w
	$$

> Produce esto:
	
$$
x^{2 \alpha} - z^w = y_{ij} + y_{ij} - z_w
$$

---


###### Mas información de formato LaTeX

Guías de matemáticas en LaTeX (Links)

* [Subscripts and superscripts](https://www.sharelatex.com/learn/Subscripts_and_superscripts)

* [Brackets and Parentheses](https://www.sharelatex.com/learn/Brackets_and_Parentheses)

* [Fractions and Binomials](https://www.sharelatex.com/learn/Fractions_and_Binomials)

* [Aligning Equations](https://www.sharelatex.com/learn/Aligning%20equations%20with%20amsmath)

* [Operators](https://www.sharelatex.com/learn/Operators)

* [Spacing in math mode](https://www.sharelatex.com/learn/Spacing_in_math_mode)

* [Integrals, sums and limits](https://www.sharelatex.com/learn/Integrals,_sums_and_limits)

* [Display style in math mode](https://www.sharelatex.com/learn/Display_style_in_math_mode)

* [List of Greek letters and math symbols](https://www.sharelatex.com/learn/List_of_Greek_letters_and_math_symbols)

---


###### Mas información de Markdown

[Info aqui](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), incluye como hacer tablas, mini resumen de tablas:

	| Tables        | Are           | Cool  |
	| ------------- |:-------------:| -----:|
	| col 3 is      | right-aligned | $1600 |
	| col 2 is      | centered      |   $12 |
	| zebra stripes | are neat      |    $1 |

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Mas detalles en el link de arriba.

---


### Transformar tus notas a una presentación

Para hacer presentaciones necesitas agregar separaciones entre diapositivas, para hacer esto agrega '---' para iniciar la siguiente diapositiva.



	# Tiulo de mi presentación

	---

	Esto es mi presentacion

	---

	blah blah blah

	---

	fin

---



> Esto genera:

![](https://i.imgur.com/03PEcSh.png)

---



---


Si quieres convertir de Markdown a PPTX(el formato de Powerpoint) copia y pega lo siguiente en la terminal.

	pandoc EL_NOMBRE_DE_TU_ARCHIVO.md -f markdown -o EL_NUEVO_NOMBRE_DE_TU_ARCHIVO.pptx
	
Recuerda cambiar "EL_NOMBRE_DE_TU_ARCHIVO" por el nombre de tu archivo y "EL_NUEVO_NOMBRE_DE_TU_ARCHIVO" por el nombre de la presentación que vas a producir.

---


## Pandoc avanzado


---


### Especificar formatos

usa -f, que significa 'from' y -t que significa 'to'

	pandoc -f markdown -t DocumentName.docx
	
Esto se puede interpretar como: "Pandoc, transforma de markdown a DocumentName.docx" 

---


### Transformar sin especificar formatos

	pandoc -o hello.tex hello.txt
	
-o es 'output', se interpreta como "pandoc, produce hello.tex usando hello.txt" pandoc intentara adivinar que formato es y que formato quieres.

---


### Portadas automáticas

Para usar portadas, escribe esto al principio de tu documento:

	---
	title:  'This is the title: it contains a colon'
	author:
	- Author One
	- Author Two
	keywords: [nothing, nothingness]
	abstract: |
	  This is the abstract.

	  It consists of two paragraphs.
	...

---

	
También puedes usar el siguiente formato (por que es mas simple)

	% title
	% author(s) (separated by semicolons)
	% date

---

	
### Presentacion estilo LaTeX / Beamer

LaTeX también puede hacer presentaciones, para esto usa beamer:

	pandoc -t beamer habits.txt -o habits.pdf
	
Las diapositivas también se separan con '---'.

---


### Presentaciones Reveal.js


	pandoc -t revealjs -s habits.txt -o habits.html

Las diapositivas también se separan con '---'. Las presentaciones revealjs se pueden importar y editar en [slides.com](https://slides.com/).

---


### Mas información de Pandoc

* [Manual](http://pandoc.org/MANUAL.html)
* [Foro de ayuda](https://stackoverflow.com/search?q=pandoc)
* [Foro de ayuda con LaTeX](https://tex.stackexchange.com/)
* [Ejemplos](http://pandoc.org/demos.html)


