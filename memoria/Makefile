OUT = ./out

.PHONY = all clean crear_carpetas

TEXCC = pdflatex
TEXCCFLAGS = -output-directory=$(OUT)

CARPETA_ENCONTRADA = $(wildcard out)

ifeq ($(CARPETA_ENCONTRADA),)
$(shell echo "Creando carpeta de salida")
$(shell mkdir -p out)
endif

all: $(OUT)/TFG.pdf

$(OUT)/TFG.pdf : TFG.tex
	$(TEXCC) $(TEXCCFLAGS) TFG.tex

clean:
	-rm -I $(OUT)/*
