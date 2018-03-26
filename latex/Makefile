SHELL=/bin/sh

default: r1.pdf r1.bcf

clean: 
	rm -f *.pdf *.dvi *.log *.aux *.bbl *.bcf *.blg

r1.pdf: Makefile r1.tex
	pdflatex r1.tex

r1.bcf: Makefile r1.tex refs.bib
	pdflatex r1.tex
	biber r1 # doesn't like file extensions, but it is .bcf

r1.dvi: Makefile r1.tex
	latex r1.tex

r1.ps: Makefile r1.dvi
	dvips r1.dvi
