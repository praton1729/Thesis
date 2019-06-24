.PHONY: all watch read clean 

FILE=thesis
TEX=$(FILE).tex
TEX_FILES=$(*.tex)
PDF=$(FILE).pdf
TEXMAKE=latexmk --output-directory=tmp -pdf

all: $(PDF)

$(PDF): ${TEX_FILES}
	$(TEXMAKE) $(TEX)

watch: 
	$(TEXMAKE) -pvc $(TEX)

read: $(PDF)
	mupdf tmp/$(PDF)

clean:
	rm -r tmp/*
