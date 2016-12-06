FILES=small.pdf large_1.pdf large_2.pdf large_3.pdf
TARGETS=../small.pdf ../large.pdf

all: $(TARGETS)

%.pdf:  %.svg
	inkscape -A $@ $<

../small.pdf: small.pdf
	cp ./small.pdf ../

../large.pdf: large_1.pdf large_2.pdf large_3.pdf
	pdfunite $? $@

clean:
	rm *.pdf
	rm ../*.pdf
