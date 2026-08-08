# Makefile for Chinese LaTeX book project

PDF = CM.pdf
TEX = xelatex
SRC = CM.tex

all: $(PDF)

$(PDF): $(SRC)
	$(TEX) $(SRC)
	$(TEX) $(SRC)

clean:
	rm -f *.aux *.log *.toc *.out *.gz *.fls *.fdb_latexmk *.synctex\(busy\)

distclean: clean
	rm -f $(PDF)
