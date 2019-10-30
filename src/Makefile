LARGEPAGES=large_1.pdf large_2.pdf large_3.pdf

all: ../small.pdf ../large.pdf

%.pdf:  %.svg
	inkscape -A $@ $<

../small.pdf: small.pdf
	cp ./small.pdf ../

../large.pdf: $(LARGEPAGES)
	pdfunite $(LARGEPAGES) $@

clean:
	rm *.pdf
	rm ../*.pdf
