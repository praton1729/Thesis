SOURCES = $(wildcard mds/*.md)

STRIPPED_SOURCE=$(SOURCES:mds/%=%)
#$(info stripped source is : "$(STRIPPED_SOURCE)")

PDFS= $(STRIPPED_SOURCE:.md=.pdf)
#$(info PDFS is : "$(PDFS)")

EXECS = $(addprefix pdfs/, $(PDFS)) 
#$(info EXECS is : "$(EXECS)")

default:all

all: merge

pdfs/%.pdf: mds/%.md
	pandoc -f markdown -V geometry:margin=0.5in $< -o $@

merge: $(EXECS)
	pdfunite pdfs/00_main.pdf \
		 mds/01_setup_of_the_system.pdf \
		 mds/02_introduction.pdf \
		 mds/03_basic_usage.pdf \
		 mds/04_ddr_access.pdf \
		 mds/05_xsct_access.pdf \
		 manual/manual.pdf 

read:
	mupdf -r 200 manual/manual.pdf

Title.pdf: 
	latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" -use-make Title.tex

clean_latex:
	latexmk -CA

clean:
	rm $(EXECS)
