.PHONY: clean all watch

FILE=ref_manual
TEX=$(FILE).tex
TEX_FILES=$(*.tex)
PDF=$(FILE).pdf
TEXMAKE=latexmk --output-directory=tmp -pdf

all: $(PDF)

$(PDF): ${TEX_FILES}
	$(TEXMAKE) $(TEX)

watch: 
	$(TEXMAKE) -pvc $(TEX)

read:
	mupdf tmp/$(PDF)
clean:
	rm tmp/*
	#rm -rf *.pdf *.aux *.bbl *.blg *dvi *.log *.out *.synctex.gz *.toc *.lot *.lof *.fls
