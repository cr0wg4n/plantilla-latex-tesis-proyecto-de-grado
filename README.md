# Plantilla LaTeX para Tesis o Proyecto de Grado (incluye Normas APA)

**"No te preocupes por el formato o la estética de tu documento, preocúpate por crear, experimentar y documentar tu proyecto/tesis debidamente"**

![](https://github.com/cr0wg4n/plantilla-latex-proyecto-de-grado/blob/master/img/preview.png)

Características:
* Carátula parametrizada
* Autogeneración de índice principal, tablas e imágenes
* Márgenes con dimensiones pre-establecidas y configurables
* Autonumeración de imágenes y tablas
* Enlaces rápidos a secciones, imágenes, tablas, código y otros
* Gestión y referenciación automática en formato APA
* Autonumerado de páginas 
* Código con highlighting y formateado automático 
* PDF bookmarks
* Diagramas de flujo
* Ejemplos de uso

> Si no se ajusta a tus necesidades es facilmente ajustable

## 🔗 Enlaces relacionados
* [Diapositivas y guia "Taller de LaTeX 2022"](https://slides.com/cr0wg4n/taller-de-latex/edit), una guia útil para los comandos y sintaxis básicas de LaTeX.
* [Artículo web sobre este repositorio](https://cr0wg4n.medium.com/documenta-tu-proyecto-de-grado-con-latex-sin-morir-en-el-intento-ft-normas-apa-15bf50a2ee01), aprende a configurar tu entorno LaTeX.

## ☑️ Requisitos
> ⚠️ Es muy importante tener instalados todos los requisitos, si usas [MiKTeX](https://miktex.org/) no olvides actualizarlo.

* Prepara tu entorno siguiendo este [articulo web para WINDOWS](https://cr0wg4n.medium.com/latex-y-visual-studio-code-gu%C3%ADa-de-instalaci%C3%B3n-ca8bef3935e3) o checa este video de [YouTube](https://www.youtube.com/watch?v=KZbciURUYb4).
* No importa si usas Linux o Windows necesitaras Python 3 o mayor instalado, una vez configurado, instala el paquete [Pygments](https://pypi.org/project/Pygments/): `pip install Pygments`.
* Si usas LINUX el camino es muy similar, necesitaras instalar Perl (`sudo apt install perl`), [MiKTeX](https://miktex.org/) dependiendo tu distro y [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) para [VSCode](https://code.visualstudio.com/).

## 🔀 Estructura de archivos

- ```configs```, directorio de configuraciones de la plantilla. En el archivo ```dockstyle.sty``` se introduce tus datos personales asi podrás personalizar la plantilla.
- ```capitulos```, directorio contenedor de los capítulos del documento, es recomendable crear sub-directorios para cada capítulo.
- ```anexos```, directorio contenedor de los anexos del documento.
- ```img```, directorio contenedor de las imagenes del documento, es recomendable crear sub-directorios para cada capítulo.
- ```codigo```, directorio para adjuntar archivos de código en texto plano (el código puede ser embebido en el mismo documento `.tex` o usado, referenciado y embebido como archivo).

## 🪛 Uso 

```main.tex``` es el archivo principal y puede ejecutarse en cualquier editor
de LaTeX (preferentemente usa MiKTeX).

El archivo ```.latexmkrc``` introduce un flag o argumento ```--shell-escape``` que permite externalizar la composición tipográfica, en este caso permite trabajar a los paquetes `tikz`, `minted2` entre otros, que comúnmente se usan para la generación de graficos o inclusión de archivos generados dinámicamente.

La compilación se realiza a través de ```pdflatex``` (la mayoria de los editores lo tienen por defecto).

> Esta plantilla fue elaborada en [Visual Studio Code](https://code.visualstudio.com/) con la extensión [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), otra muy buena alternativa es [Texmaker](https://www.xm1math.net/texmaker/).

## 🚀 Demo

El documento ```.pdf``` final se [main.pdf](https://github.com/cr0wg4n/plantilla-latex-proyecto-de-grado/blob/master/build/main.pdf) y se encuentra en el directorio `./build` (si configuraste bien tu entorno).

## 🤔 ¿Deseas reducir el tamaño de tu PDF?

En muchas ocasiones el PDF final alcanza un peso demasiado alto, eso dependerá de cuantas imágenes estas empleando en el documento y en que calidad se encuentren, para ello puedes correr el siguiente comando para disminuir la calidad de las imágenes en tu PDF, pero antes necesitas instalar [ghostscript](https://www.ghostscript.com/), te aconsejo correr el comando en una terminal con bash:

```bash
# Comando válido para windows
gswin64c -sDEVICE=pdfwrite -dDownsampleColorImages=true -dDownsampleGrayImages=true -dDownsampleMonoImages=true -dColorImageResolution=300 -dGrayImageResolution=300 -dMonoImageResolution=300 -dColorImageDownsampleThreshold=1.0 -dGrayImageDownsampleThreshold=1.0 -dMonoImageDownsampleThreshold=1.0 -dCompatibilityLevel=1.4 -dNOPAUSE -dQUIET -dBATCH -sOutputFile=build/main-compressed.pdf build/main.pdf
```

Para lograr mejores o peores resultado puedes ajustar el valor de los parámetros (`dColorImageResolution`, `dGrayImageResolution`, `dMonoImageResolution`), estos parámetros tienen que ver con la calidad en la que se procesaran las imágenes internas, LaTeX suele conservar la mejor calidad, pero modificando estos parámetros es posible cambiar la resolución de las imágenes logrando un menor tamaño en el peso del archivo pdf final.

En general, si buscas mantener el tamaño del PDF contenido evita usar imágenes en alta calidad, o procésalas previamente con herramientas como [Squoosh (online)](https://squoosh.app/) o [ImageMagick (ejecutable local)](https://www.imagemagick.org)

## 🤝 Contribución

Gracias por tu interés en contribuir, para mantener una colaboración ordenada es importante seguir estas reglas:

- Haz un *fork* del repositorio y trabaja en una rama separada.
- Escribe mensajes de *commit* claros y descriptivos.
- Asegúrate de que el cambio introducido es valido y funciona corretamente antes de armar un *pull request*.
- Respeta la estructura y estilo del proyecto.

Toda contribución es bienvenida, ¡gracias por ayudar a mejorar el proyecto!


> This project was made with ❤️ by [cr0wg4n](https://www.lowleveltech.com/)