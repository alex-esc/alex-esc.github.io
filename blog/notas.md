# Notas digitales

En esta guía te enseñara como tomar notas digitales con texto, formato, links, imágenes o gráficas, bloques de código, tablas y ecuaciones de manera efectiva, como transformar tus notas a Word, PDF , publicar tus notas o tareas en una pagina web y en como transformar tus notas a una presentación estilo PowerPoint automáticamente. Todo esto desde cualquier dispositivo, sea laptop, Smartphone, tablet, PC, Mac o Linux.

> Este método es gratis, **necesitas una computadora (PC, Mac, Linux) como mínimo, puedes hacer tus documentos en tu teléfono pero no transformarlos a PDF, docx etc hasta pasarlos a tu computadora**, las transformaciones solo se pueden hacer en una computadora por que un programa llamado pandoc solo corre en pc's, Termux podría funcionar para android pero no esta oficialmente soportado.

Recomiendo esta guía a estudiantes principalmente.

## Notas simples y flexibles

Así se ve el respaldo de mis notas en mi pagina web:

![](https://i.imgur.com/reoV9VD.png)

La pregunta numero uno que me hacen mis compañeros es ¿como haces que tus notas se vean así? la respuesta corta es _Markdown_. La respuesta larga es... un poco mas complicada, hay 3 partes principales de mi sistema de notas: El texto original, Documento en PDF y un respaldo en mi pagina web. Esta guía te enseñara como duplicar mi estilo de notas.

Una parte importante de tomar todos tus apuntes digitales es la eliminación de distracciones y no no solo me refiero a dejar atrás tu teléfono, me refiero a distracciones dentro del método de tomar notas, por ejemplo:

En procesadores de texto como word, google drive o pages cada acción esta escondida debajo de un menu o sub-menu, pasaras una gran cantidad de tiempo haciendo click derecho aqui, arrastrando imágenes y objetos por allá, en lugar de escribiendo el contenido. Por eso en mi método no usaremos word o pages o drive en particular, este método te permite trabajar en cualquier editor de texto sin tener que pelear con menús, solo tu y tu teclado.

## Como usar Markdown

Como mencione al principio usaremos Markdown (o "md" por su extensión), este no es un nuevo programa por aprender, markdown es solo sintaxis. La meta de md es simple: ser fácil de leer en cualquier dispositivo y en cualquier programa.

Un archivo de markdown se ve asi:

	# Integrales y derivadas

	La derivadas son una relación de diferencia de cambio de una curva.

	Las integrales son la reversa de integrales, una buena forma de visualizar integrales es pensando en el área debajo de la curva.

	![Curva en rojo y área en gris](https://matplotlib.org/1.4.2/_images/integral_demo.png)

	**Formulas de derivadas**

	_basica:_
	
No es nada especial, solo es texto con símbolos extra, como puedes ver este texto es una parte de la imagen de arriba. Poner un '#' antes de cualquier texto lo convierte en el titulo, poner dos '*' alrededor de una o mas palabras las convierte en negritas y poner un '_' alrededor de otras palabras las convierte en itálicas.

Mas adelante veremos como escribir ecuaciones en markdown, pero por ahora aquí un ejemplo de las funciones funciones de markdown

	# Esto es un titulo

	## Esto es un sub-titulo

	### subtitulo nivel 3

	#### subtitulo nivel 4

	##### subtitulo nivel 5

	###### subtitulo nivel 6

	####### subtitulo nivel 7

	######## solo puedes hacer 8 sub niveles de titulo

	Esto es texto normal, pero **esto esta en negritas** y _esto en itálicas_.

	Deja una linea entre renglones para iniciar un nuevo párrafo.

	[Esto es un link y te lleva a wikipedia](https://www.wikipedia.org/)

	y abajo hay un link a una foto, agragar un '!' antes del link te mostrara la foto. (como la gráfica de integrales en el primer ejemplo)

	![Esto son notas de la foto, pueden estar vacías.](https://upload.wikimedia.org/wikipedia/commons/d/de/Wikipedia_Logo_1.0.png)

	La foto de arriba es el logo de wikipedia.
	
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

Entonces para usar markdown solo abre un editor de texto, el que tu quieras y escribe siguiendo estas reglas, no olvides guardar tu documento con la terminación '.md' para guardarlo como archivo markdown. Archivo -> Guardar como -> escribe el nombre del documento y agrega '.md' al final.

## Grandes ventajas de markdown

![](https://i.imgur.com/sDO7Pp9.png)

Bueno ahora escribes tus notas con hastags, asteriscos y brackets por doquier ¿pero esto de que me sirve? bueno si te as fijado que aun no hay imágenes ni negritas aun es por que markdown tiene que convertirse de texto a algo mas, algo como un PDF o documento de word, si no lo transformas no sera mas que texto simple, pero esto el la primera gran ventaja de md: como solo es texto, lo puedes editar con cualquier programa en cualquier aparato: Puedes usar block de notas en tu PC y continuar tomando notas en tu celular y fácilmente agregar las nuevas notas que tomaste en tu teléfono a tu computadora.

En otras palabras _Markdown te permite hacer PDFs, documentos de word y paginas web en cualquier dispositivo_, puedes usar dropbox, drive o icloud para sincronizar las notas de tu smartphone y tu computadora. Como un extra, también puedes transformar tus documentos de markdown a una presentación de Powerpoint, esto te ahorrara mucho tiempo cuando tengas que hacer un escrito sobre un tema visto en clase y una presentación ya que el escrito sera una versión extendida de tus notas, el Powerpoint se generara de tus notas, mas adelante veremos este tema, por ahora lo básico.

Cuando termines tus notas y quieras convertirlas a PDF, word o pagina web solo abre la carpeta con tus notas, usaras un programa llamado **pandoc** para hacer la trasformación.

## Como transformar tus documentos usando Pandoc

Pandoc es una simple herramienta que transforma documentos, una ves que este instalado en tu computadora tendrás que usar la terminal o linea de comandos para hacer la transformación. **Woah woah woah!** ¿dijiste linea de comandos? ¡detente ahí no soy experto en computadoras! 

No te preocupes, yo tampoco soy un experto, _solo necesitas saber copiar y pegar, eso es todo._

### Paso uno, instala Pandoc

Guía de instalación de pandoc en [PC](http://www.texts.io/support/0004/), [Mac](http://www.texts.io/support/0003/) y [linux](https://pandoc.org/installing.html#linux)

Si tienes problemas la pagina oficial de Pandoc esta [aquí](https://pandoc.org/installing.html)

### Paso dos, localiza tu documento a transformar

Abre la carpeta donde guardas tu documento, recuerda que termina en '.md', luego abre la terminal en esa carpeta:

* En Windows has click derecho en el espacio en blanco y preciosa la tecla shift al mismo tiempo, luego selecciona a abrir Powershell aquí. ([mas info](https://www.addictivetips.com/windows-tips/open-powershell-in-a-specific-location/))

* En Mac ve a preferencias , teclado, atajos, servicios y activa New Terminal at Folder, luego de esto podrás hacer click derecho en cualquier folder y en servicios habrá una opción para abrir nueva terminal aquí. ([mas info](https://lifehacker.com/launch-an-os-x-terminal-window-from-a-specific-folder-1466745514))

* En linux (Ubuntu) preciona Ctrl + Alt + T y pega este texto "sudo apt-get install nautilus-open-terminal" (sin comillas), esto instalara el menú de abrir en terminal, reinicia tu computadora y has click derecho en cualquier archivo y selecciona abrir en terminal. ([mas info](https://www.howtogeek.com/192865/how-to-open-terminal-to-a-specific-folder-in-ubuntus-file-browser/))

Obviamente solo tendrás que hacer las configuraciones necesarias la primera ves, luego sigue lo mas fácil, si tienes problemas no olvides que el internet es tu amigo!

### Ultimo paso, transforma tu documento

Ahora debes estar en la terminal, el texto debe indicar que estas en la misma carpeta que tu archivo, luego tenemos que decidir a que formato queremos convertir:

En esta guía veremos como transformar markdown a PDF, word y una pagina web, si quieres transformar a otros formatos [aquí](https://pandoc.org/MANUAL.html) esta el manual de pandoc.

#### Transformar a PDF

Si quieres convertir de Markdown a PDF copia y pega lo siguiente en la terminal.

	pandoc EL_NOMBRE_DE_TU_ARCHIVO.md -f markdown -o EL_NUEVO_NOMBRE_DE_TU_ARCHIVO.pdf
	
Recuerda cambiar "EL_NOMBRE_DE_TU_ARCHIVO" por el nombre de tu archivo y "EL_NUEVO_NOMBRE_DE_TU_ARCHIVO" por el nombre del PDF que vas a producir.

#### Transformar a una pagina web

Si quieres convertir de Markdown a HTML (el formato de las paginas web) copia y pega lo siguiente en la terminal.

	pandoc EL_NOMBRE_DE_TU_ARCHIVO.md -f markdown -o EL_NUEVO_NOMBRE_DE_TU_ARCHIVO.html
	
Recuerda cambiar "EL_NOMBRE_DE_TU_ARCHIVO" por el nombre de tu archivo y "EL_NUEVO_NOMBRE_DE_TU_ARCHIVO" por el nombre del archivo HTML que vas a producir. Para publicar este acrhivo en internet necesitas una pagina web que te permita subir los archivos que quieras como [neocities](https://neocities.org/) y [github pages](https://pages.github.com/), para agregar estilo a tu pagina lee [esta guía](https://jblevins.org/log/custom-css).

cambia '-f markdown' por '-s --katex' si necesitas usar matemáticas, también puedes usar --mathjax pero yo prefiero katex.

	pandoc math.text -s --katex   -o mathKaTeX.html

#### Transformar a un documento de word

Si quieres convertir de Markdown a docx copia y pega lo siguiente en la terminal.

	pandoc EL_NOMBRE_DE_TU_ARCHIVO.md -f markdown -o EL_NUEVO_NOMBRE_DE_TU_ARCHIVO.docx
	
Recuerda cambiar "EL_NOMBRE_DE_TU_ARCHIVO" por el nombre de tu archivo y "EL_NUEVO_NOMBRE_DE_TU_ARCHIVO" por el nombre del archivo de word que vas a producir.

Veremos como transformar a Powerpoint mas adelante...



## Markdown avanzado

### Comentarios

<!-- Recuerda corregir ortografía -->

Para escribir un comentario, primero escribe '\<\!\-\-' luego tu comentario, cuando termines tu comentario escribe '\-\-\>'. Un comentario es texto que no se mostrara cunado el archivo markdown sea transformado a word, PDF o cualquier otro formato.

	### Comentarios

	<!-- Recuerda corregir ortografía -->

	Para escribir un comentario, primero escribe '<!--' luego tu comentario, cuando termines tu comentario escribe '-->'. Un comentario es texto que no se mostrara cunado el archivo markdown sea transformado a word, PDF o cualquier otro formato.

Por ejemplo, este comentario para recordarme corregir ortografía es invisible, yo recomiendo que copies el código que usaras para transformar el documento con pandoc en un comentario, para recordarte como hacer la transformación.

#### Escribir ejemplos de código

Si necesitas escribir ejemplos de código en tus notas solo tienes que seleccionar el texto del código y presionar tab o tabulador (Es la tecla arriba de bloq mayus)

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

#### Citas

Para sobresalir un texto de por ejemplo una cita textual solo agregamos '>' al principio de un párrafo:

Cita como texto:

Life is like riding a bicycle. To keep your balance, you must keep moving.

- Albert Einstein


Cita con '>':

> Life is like riding a bicycle. To keep your balance, you must keep moving.
>
>  Albert Einstein

#### Hacer un PDF con tabla de contenidos

escribe '\\tableofcontents' al principio de tu documento

#### Forzar PDF a saltar a siguiente pagina

Agrega '\\pagebreak' entre párrafos para asegurarte que se salte una pagina después de un párrafo.

#### Agregar espacio en blanco entre párrafos

usa el ambiente '\\vspace{}' para agregar espacio vertical entre párrafos, por ejemplo '\\vspace{5cm}' se salta 5 centímetros, esto es util para hacer paginas de portada simples.


#### Como escribir símbolos especiales

¿Que tal si quieres escribir un símbolo que se usa para cambiar el formato? solo tienes que agregar '\\' al principio. Si quieres escribir caracteres especiales como delta o pi, tienes que buscar como escribirlos en _LaTeX_, LaTeX es otro formato como markdown, pero LaTeX es mas complicado por eso solo lo usaremos muy poco.

Lo único que tienes que saber de LaTeX es:

* Como escribir símbolos o caracteres especiales
* Sintaxis de matemáticas
* Modo de ecuaciones alineadas

Veremos cada punto en esta guía, primero caracteres especiales: Por ejemplo para escribir _el numero pi_ usaremos \\pi, para delta usaremos '\\Delta' etc, solo busca en Internet como escribir el símbolo que deseas en LaTeX.

Así se escriben los símbolos $\pi$ y $\Delta$ en _LaTeX_.

	Así se escriben los símbolos $\pi$ y $\Delta$ en _LaTeX_.

#### Escribir ecuaciones y modo matemáticas

Para escribir matemáticas primero debemos entrar en 'math mode' , esto es simple, para activar este modo usaremos '$' , por eso el ejemplo de arriba tiene símbolos de dolar alrededor de pi y Delta, todos los símbolos escritos en LaTeX necesitan estar en mathmode, hay dos opciones para mathmode: matemáticas entre texto y matemáticas por si solas. Si quieres insertar ecuaciones entre texto escribe tu ecuación entre símbolos de dolar: 

##### Matemáticas entre texto

> Escribir esto:

	La famosa formula de Einstein es $E = MC^2$ , Parte de la teoría de la relatividad, conocida como Equivalencia entre masa y energía.

> Produce esto:

La famosa formula de Einstein es $E = MC^2$ , Parte de la teoría de la relatividad, conocida como Equivalencia entre masa y energía.

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

##### Formato de matemáticas de LaTeX

Todas las matemáticas en md se escribes en LaTeX, todas las ecuaciones siguen este formato:

###### Números, sumas, restas y multiplicaciones

para escribir números, sumas ,restas y multiplicaciones solo escribelos normalmente, recuerda entrar en modo mate:

	$$
	2 + 2 = 5 - 1 * 1
	$$

> Produce esto:
	
$$
2 + 2 = 5 - 1 * 1
$$

###### Divisiones

Usa el código frac, luego entre llaves escribe el numerador y en otras llaves el denominador:

	$$
	\frac{1}{2}
	$$

> Produce esto
	
$$
\frac{1}{2}
$$
	
###### Exponentes y subindices

Usa el símbolo '^' para elevar solo un numero, usa llaves para elevar varios números, usa el símbolo '_' para hacer subindices

	$$
	x^{2 \alpha} - z^w = y_{ij} + y_{ij} - z_w
	$$

> Produce esto:
	
$$
x^{2 \alpha} - z^w = y_{ij} + y_{ij} - z_w
$$

Recuerda que puedes incluir caracteres especiales con LaTeX, por eso el ejemplo usa '\\alpha'.

###### Múltiples ecuaciones alineadas 

Para escribir procesos matemáticos necesitas usar el código de align de LaTeX, primero inicias el modo align, luego escribes tu ecuación usando LaTeX, escribe un '&' donde quieres alinear tus ecuaciones, escribir dos '\\' oprimir enter y escribir cuantas ecuaciones necesites, la ultima ecuación no debe tener '\\\\' finalmente debes terminar el modo align, Por ejemplo:

	$$
	\begin{align*}
	y(x) &= x\\
	y(x) &= x^2\\
	y(x) &= e^x\\
	y(x) &= sen(x)
	\end{align*}
	$$


	
> Produce esto:

$$
\begin{align*}
y(x) &= x\\
y(x) &= x^2\\
y(x) &= e^x\\
y(x) &= sen(x)
\end{align*}
$$

Recuerda que tienes que entrar a modo matemáticas con símbolos de dolar. En el ejemplo usamos el modo 'align\*' porque el modo 'align' también numera las ecuaciones, mientras que el modo 'align\*' no las enumera.

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

### Transformar tus notas a una presentación

Para hacer presentaciones necesitas agregar separaciones entre diapositivas, para hacer esto agrega '\-\-\-' para iniciar la siguiente diapositiva.

> Esto genera:

	# Tiulo de mi presentación

	---

	Esto es mi presentacion

	---

	blah blah blah

	---

	fin


> Esto genera:

![](https://i.imgur.com/03PEcSh.png)

Como puedes hacer presentaciones de esta forma, yo recomiendo que si tienes que presentar algún tema del que tienes apuntes y ademas debes entregar un reporte entonces dupliques tus notas, en la copia elimina todo menos el tema de tus notas, agrega '\-\-\-' para separar los temas, luego elimina parte del texto para que halla poca información por diapositiva, finalmente duplica otra ves tus notas y redacta un poco mas para hacer el reporte, esto te ahorra re-escribir las mismas ideas 3 veces, solo tienes que expandir el texto en el reporte y recortar información en la presentación.

Si quieres convertir de Markdown a PPTX(el formato de Powerpoint) copia y pega lo siguiente en la terminal.

	pandoc EL_NOMBRE_DE_TU_ARCHIVO.md -f markdown -o EL_NUEVO_NOMBRE_DE_TU_ARCHIVO.pptx
	
Recuerda cambiar "EL_NOMBRE_DE_TU_ARCHIVO" por el nombre de tu archivo y "EL_NUEVO_NOMBRE_DE_TU_ARCHIVO" por el nombre de la presentación que vas a producir.

## Pandoc avanzado

Ahora que puedes tomar notas con Markdown y transformarlas a PDF, presentacion de Powerpoint, documento de Word y pagina de internet de manera simple con pandoc te preguntaras ¿Como puedo hacer que mis documentos transformados se vean mejor?

La respuesta esta en pandoc, el manual completo de pandoc esta [aqui](http://pandoc.org/MANUAL.html), abajo un resumen de los mas importante en mi opinión:

### Especificar formatos

usa -f, que significa 'from' y -t que significa 'to' en ingles.

	pandoc -f markdown -t DocumentName.docx
	
Esto se puede interpretar como: "Pandoc, transforma de markdown a DocumentName.docx" 

### Transformar sin especificar formatos

	pandoc -o hello.tex hello.txt
	
-o es 'output', se interpreta como "pandoc, produce hello.tex usando hello.txt" pandoc intentara adivinar que formato es y que formato quieres.

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
	
También puedes usar el siguiente formato (por que es mas simple)

	% title
	% author(s) (separated by semicolons)
	% date
	
### Presentacion estilo LaTeX / Beamer

LaTeX también puede hacer presentaciones, para esto usa beamer:

	pandoc -t beamer habits.txt -o habits.pdf
	
Las diapositivas también se separan con '\-\-\-'.

### Presentaciones Reveal.js

Reveal.js es mi metodo favorito de hacer presentaciones, es el mas profecional y el mas sencillo de automatisar el estilo, colores y tipo de letras, para transformar a reveal.js usa:

	pandoc -t revealjs -s habits.txt -o habits.html

Las diapositivas también se separan con '\-\-\-'. Las presentaciones revealjs se pueden importar y editar en [slides.com](https://slides.com/).

### Mas información de Pandoc

* [Manual](http://pandoc.org/MANUAL.html)
* [Foro de ayuda](https://stackoverflow.com/search?q=pandoc)
* [Foro de ayuda con LaTeX](https://tex.stackexchange.com/)
* [Ejemplos](http://pandoc.org/demos.html)


## Ejemplo

Esta es una fracción de mis notas de matemáticas:


	% **Libreta - Matemáticas**
	% Semestre Agosto - Diciembre 2018
	% Alejandro Escalante

	# Integrales y derivadas

	La derivadas son una relación de diferencia de cambio de una curva.

	$$
	pendiente = \frac{\Delta y}{\Delta x}
	$$

	Las integrales son la reversa de integrales, una buena forma de visualizar integrales es pensando en el área debajo de la curva.

	![Curva en rojo y área en gris](https://matplotlib.org/1.4.2/_images/integral_demo.png)

	\pagebreak

	**Formulas de derivadas**

	_basica:_


	$$
	x^n = nx^{n-1}
	$$

	_Casos comunes:_

	|  |  |  |
	|--|--|--|
	| $\frac{d}{dx}(c) = 0$ | $\frac{d}{dx}(x^n) = nx^{n-1}$ | $\frac{d}{dx}(e^x) = e^x$ |
	| $(cf)' = cf'$ | $(f + g)' = f' + g'$ | $(f - g)' = f' - g'$ |
	| $(fg)' = fg' + gf'$ | $\left( \frac{f}{g} \right) ' = \frac{gf'+fg'}{g^2}$ |  |

	_funciones trigonométricas:_

	|  |  |  |
	|--|--|--|
	| $\frac{d}{dx}(sen x) = cos x$ | $\frac{d}{dx}(cos x) = -sen x$ | $\frac{d}{dx}(tan x) = sec^2 x$ |
	| $\frac{d}{dx}(csc x) = -csc x cot x$ | $\frac{d}{dx}(sec x) = sec x tan x$ | $\frac{d}{dx}(cot x) = -csc^2x$ |	

	
Si lo transformo a HTML con pandoc usando kaktex con el comando:

	pandoc Notas_Matemáticas.md -s --katex   -o mate-notas-web.html
	
Pandoc genera el siguiente documento html:

	<!DOCTYPE html>
	<html xmlns="http://www.w3.org/1999/xhtml" lang="" xml:lang="">
	<head>
	  <meta charset="utf-8" />
	  <meta name="generator" content="pandoc" />
	  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes" />
	  <meta name="author" content="Semestre Agosto - Diciembre 2018" />
	  <title>Libreta - Matemáticas</title>
	  <style type="text/css">
		  code{white-space: pre-wrap;}
		  span.smallcaps{font-variant: small-caps;}
		  span.underline{text-decoration: underline;}
		  div.column{display: inline-block; vertical-align: top; width: 50%;}
	  </style>
	  <script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.8.3/katex.min.js"></script><script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.8.3/contrib/auto-render.min.js"></script><script>document.addEventListener("DOMContentLoaded", function() {
		renderMathInElement(document.body);
	  });</script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.8.3/katex.min.css" />
	  <!--[if lt IE 9]>
		<script src="//cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv-printshiv.min.js"></script>
	  <![endif]-->
	</head>
	<body>
	<header>
	<h1 class="title"><strong>Libreta - Matemáticas</strong></h1>
	<p class="author">Semestre Agosto - Diciembre 2018</p>
	<p class="date">Alejandro Escalante</p>
	</header>
	<h1 id="integrales-y-derivadas">Integrales y derivadas</h1>
	<p>La derivadas son una relación de diferencia de cambio de una curva.</p>
	<p><span class="math display">\[
	pendiente = \frac{\Delta y}{\Delta x}
	\]</span></p>
	<p>Las integrales son la reversa de integrales, una buena forma de visualizar integrales es pensando en el área debajo de la curva.</p>
	<figure>
	<img src="https://matplotlib.org/1.4.2/_images/integral_demo.png" alt="Curva en rojo y área en gris" /><figcaption>Curva en rojo y área en gris</figcaption>
	</figure>

	<p><strong>Formulas de derivadas</strong></p>
	<p><em>basica:</em></p>
	<p><span class="math display">\[
	x^n = nx^{n-1}
	\]</span></p>
	<p><em>Casos comunes:</em></p>
	<table>
	<tbody>
	<tr class="odd">
	<td><span class="math inline">\(\frac{d}{dx}(c) = 0\)</span></td>
	<td><span class="math inline">\(\frac{d}{dx}(x^n) = nx^{n-1}\)</span></td>
	<td><span class="math inline">\(\frac{d}{dx}(e^x) = e^x\)</span></td>
	</tr>
	<tr class="even">
	<td><span class="math inline">\((cf)&#39; = cf&#39;\)</span></td>
	<td><span class="math inline">\((f + g)&#39; = f&#39; + g&#39;\)</span></td>
	<td><span class="math inline">\((f - g)&#39; = f&#39; - g&#39;\)</span></td>
	</tr>
	<tr class="odd">
	<td><span class="math inline">\((fg)&#39; = fg&#39; + gf&#39;\)</span></td>
	<td><span class="math inline">\(\left( \frac{f}{g} \right) &#39; = \frac{gf&#39;+fg&#39;}{g^2}\)</span></td>
	<td></td>
	</tr>
	</tbody>
	</table>
	<p><em>funciones trigonométricas:</em></p>
	<table>
	<colgroup>
	<col style="width: 33%" />
	<col style="width: 33%" />
	<col style="width: 33%" />
	</colgroup>
	<tbody>
	<tr class="odd">
	<td><span class="math inline">\(\frac{d}{dx}(sen x) = cos x\)</span></td>
	<td><span class="math inline">\(\frac{d}{dx}(cos x) = -sen x\)</span></td>
	<td><span class="math inline">\(\frac{d}{dx}(tan x) = sec^2 x\)</span></td>
	</tr>
	<tr class="even">
	<td><span class="math inline">\(\frac{d}{dx}(csc x) = -csc x cot x\)</span></td>
	<td><span class="math inline">\(\frac{d}{dx}(sec x) = sec x tan x\)</span></td>
	<td><span class="math inline">\(\frac{d}{dx}(cot x) = -csc^2x\)</span></td>
	</tr>
	</tbody>
	</table>
	</body>
	</html>

Aunque no tengo la menor idea de como leer html lo subiré a [mi pagina](alex-esc.neocities.org) y agrego el link a mi css de estilo markdown y me produce:

![](https://i.imgur.com/reoV9VD.png)

Esto me genera un respaldo en linea de mis notas, pero si quiero el archivo en pdf entonces uso estas instrucciones en pandoc:

	pandoc Notas_Matemáticas.md -f markdown -o mate-notas.pdf

El siguiente PDF es generado:

![](https://i.imgur.com/scVPZrD.png)

> \*Screenshot de mis notas completas, el pdf real de esta conversión seria ligeramente diferente

## En resumen

un documento en markdown como:

	% titulo
	% autor
	% fecha

	# Este es mi documento en markdown

	Este es el **contenido** con matemáticas $x=1$

pasa por pandoc 2 veses, primero con las opciones:

	pandoc midocumento.md -f markdown -s --katex -o midocumento.html

y produce:

		<!DOCTYPE html>
	<html xmlns="http://www.w3.org/1999/xhtml" lang="" xml:lang=""><head><meta charset="utf-8" /><meta name="generator" content="pandoc" /><meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes" /><meta name="author" content="autor" />
	  <title>titulo</title>
	  <style type="text/css">code{white-space: pre-wrap;}span.smallcaps{font-variant: small-caps;}span.underline{text-decoration: underline;}div.column{display: inline-block; vertical-align: top; width: 50%;}</style><script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.8.3/katex.min.js"></script><script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.8.3/contrib/auto-render.min.js"></script><script>document.addEventListener("DOMContentLoaded", function() {renderMathInElement(document.body);});</script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.8.3/katex.min.css" /><!--[if lt IE 9]><script src="//cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv-printshiv.min.js"></script><![endif]-->
	</head>
	<body>
	<header>
	<h1 class="title">titulo</h1>
	<p class="author">autor</p>
	<p class="date">fecha</p>
	</header>
	<h1 id="este-es-mi-documento-en-markdown">Este es mi documento en markdown</h1>
	<p>Este es el <strong>contenido</strong> con matemáticas <span class="math inline">\(x=1\)</span></p>
	</body>
	</html>

	
Agrego mi css después de <meta charset="utf-8" />

  <link rel="stylesheet" href="css/modest.css">

Genera esta pagina:

![](https://i.imgur.com/iB4gthN.png)

