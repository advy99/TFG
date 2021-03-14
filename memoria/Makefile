OUT = ./out


.PHONY = all clean crear_carpetas

all: crear_carpetas $(OUT)/TFG.pdf

$(OUT)/TFG.pdf : TFG.tex
	pdflatex -output-directory=$(OUT) TFG.tex

crear_carpetas :
	-mkdir -p $(OUT)

clean:
	-rm -I $(OUT)/*
