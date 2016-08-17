FILE = ms
REF = references
TEX = latex
BIBTEX = bibtex
DVIPDF = dvipdf

.PHONY: all clean

all: $(FILE).dvi $(FILE).pdf

$(FILE).dvi : $(FILE).tex $(REF).bib makefile *.tex
	$(TEX) $(FILE)
	$(BIBTEX) $(FILE)
	$(TEX) $(FILE)
	$(TEX) $(FILE)

$(FILE).pdf : $(FILE).dvi
	$(DVIPDF) $(FILE).dvi
	open $(FILE).pdf &

clean :
	\rm *Notes.bib
	\rm *.aux
	\rm *.bbl
	\rm *.log
	\rm *.blg
	\rm *.dvi
	\rm *.out
