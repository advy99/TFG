OUT = ./out

.PHONY = all clean crear_carpetas

TEXCC = pdflatex
TEXCCFLAGS = -output-directory=$(OUT)

CARPETA_ENCONTRADA = $(wildcard out)

FICHEROS_TEX = $(wildcard src/*)

ifeq ($(CARPETA_ENCONTRADA),)
$(shell echo "Creando carpeta de salida")
$(shell mkdir -p out)
endif

all: $(OUT)/TFG.pdf

$(OUT)/TFG.pdf : TFG.tex $(FICHEROS_TEX)
	$(TEXCC) $(TEXCCFLAGS) TFG.tex
	# volvemos a compilar, para que genere bien el indice
	$(TEXCC) $(TEXCCFLAGS) TFG.tex

clean:
	-rm -I $(OUT)/*
