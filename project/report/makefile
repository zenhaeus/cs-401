# Author: Emiliano Carlos de Moraes Firmino @ 10/2012
SHELL=/bin/sh
THESIS=ada2017

.SUFFIXES:
.SUFFIXES: .bib .pdf .tex
.PHONY: clean

run: $(THESIS).pdf

$(THESIS).pdf: $(THESIS).bbl $(THESIS).tex
	pdflatex $(THESIS).tex -draftmode
	pdflatex $(THESIS).tex 

$(THESIS).bbl: $(THESIS).aux
	bibtex $(THESIS).aux

$(THESIS).aux: $(THESIS).bib
	pdflatex $(THESIS).tex -draftmode
	pdflatex $(THESIS).tex -draftmode

clean:
	rm -rf *.aux *.lof *.log *.lot *.toc *.bbl *.blg *pdf
