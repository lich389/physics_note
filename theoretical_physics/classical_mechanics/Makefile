# Makefile for Chinese LaTeX book project

PDF = CM.pdf
TEX = xelatex
BIB = bibtex
SRC = CM.tex

all: $(PDF)

$(PDF): $(SRC) refs.bib
	$(TEX) $(SRC)
	$(BIB) CM
	$(TEX) $(SRC)
	$(TEX) $(SRC)

clean:
	rm -f *.aux *.log *.toc *.out *.gz *.fls *.fdb_latexmk *.synctex\(busy\) *.bbl *.blg

distclean: clean
	rm -f $(PDF)
