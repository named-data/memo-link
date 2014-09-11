GRAFFLE_EXPORT = graffle2pdf

.PHONY: images

IMAGE_FILES=$(shell find . -name '*.graffle')

images: $(IMAGE_FILES:graffle=pdf)

%.pdf: %.graffle
	${GRAFFLE_EXPORT} $< $@
	pdfcrop $@ $@

clean:
	@echo rm -f $(IMAGE_FILES:graffle=pdf)
