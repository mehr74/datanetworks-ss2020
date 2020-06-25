PAPER_NAME := main

TEX := $(shell find ./ -type f -name "*.tex")
CLS := $(shell find ./ -type f -name "*.cls")
BIB := $(shell find ./ -type f -name "*.bib")
PAPER_DEPS := $(TEX) $(CLS) $(BIB)
LATEX := ./bin/latexrun --color auto

all: $(PAPER_NAME).pdf

$(PAPER_NAME).pdf: $(PAPER_DEPS)
	$(LATEX) $(PAPER_NAME).tex -O .latex.out -o $@

clean:
	$(LATEX) --clean-all -O .latex.out
	@rm -frv .latex.out $(PDFS)
