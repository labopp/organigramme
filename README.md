# Organiramme
L'organigramme du laboratoire de mathématiques Paul Painlevé de Lille

## LaTeX

- `organigramme.tex` : le fichier principal tex contenant l'organigramme sous forme d'image `tikz`
- `organigramme_a4.tex` : ce fichier insère le `organigramme.pdf` dans une page A4

# PDF

Pour obtenir les versions `pdf` il suffit de compiler les fichier tex, de préférence avec `XeLaTeX`.

# PNG

Pour convertir le `pdf` en image `png` on peut utiliser :

## [mudraw](http://mupdf.com/) (Windows)

    mudraw.exe -o organigramme.png -r200 organigramme.pdf 1

## [ghostview](http://pages.cs.wisc.edu/~ghost/gsview/index.htm) (Windows)

    gswin32c -dDownScaleFactor=4 -dSAFER -dBATCH -dNOPAUSE -sDEVICE=png16m -r800 -sOutputFile=organigramme.png organigramme.pdf

## `convert`  (Linux)

    convert -d 200 organigramme.pdf organigramme.png
