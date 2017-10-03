# Makefile pour convertir en format Encapsulated Postscript
# les graphes produits avec Dot

.SUFFIXES: .png .dot
.PHONY: clean, png

%.png:	%.dot
	@dot -Tpng $< -o $@

%.eps:	%.dot
	@dot -Teps $< -o $@

IMAGES = $(shell ls -1 *.dot 2> /dev/null)

png: ${IMAGES:.dot=.png}

eps: ${IMAGES:.dot=.eps}

clean:
	@rm -f ${IMAGES:.dot=.png}
