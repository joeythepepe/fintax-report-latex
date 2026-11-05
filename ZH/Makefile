LATEXMK ?= latexmk
BUILD_DIR := build
RELEASE_DIR := output/pdf
RELEASE_PDF := $(RELEASE_DIR)/FinTax_AI_Data_Center_Tax_Incentives_ZH.pdf

.PHONY: pdf release clean
pdf:
	$(LATEXMK) -xelatex -synctex=1 -interaction=nonstopmode -halt-on-error -file-line-error -outdir=$(BUILD_DIR) main.tex
release: pdf
	mkdir -p $(RELEASE_DIR)
	cp $(BUILD_DIR)/main.pdf $(RELEASE_PDF)
clean:
	$(LATEXMK) -C -outdir=$(BUILD_DIR) main.tex
