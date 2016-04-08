.PHONY: clean

manuscript.tex: manuscript.md
	pandoc manuscript.md -o manuscript.tex
	perl -pi -e 's/^/%% / if /\\includegraphics\{.\/figure01_overview.pdf\}/' manuscript.tex
	perl -pi -e 's/\\begin\{longtable\}/\\begin\{sidewaystable\}\\begin\{longtable\}/' manuscript.tex
	perl -pi -e 's/\\end\{longtable\}/\\end\{longtable\}\\end\{sidewaystable\}/' manuscript.tex

manuscript-plos.pdf: manuscript-plos.tex manuscript.tex
	latex manuscript-plos
	bibtex manuscript-plos
	latex manuscript-plos
	latex manuscript-plos
	dvipdf manuscript-plos

Supplementary-Note.pdf: Supplementary-Note.md
	 Rscript -e "rmarkdown::render('Supplementary-Note.md', output_format = 'pdf_document')"

clean:
	rm -f *~
	rm -f manuscript-plos.aux
	rm -f manuscript-plos.bbl
	rm -f manuscript-plos.blg
	rm -f manuscript-plos.dvi
	rm -f manuscript-plos.log
	rm -f manuscript-plos.out
	rm -f manuscript-plos.tex.pdf
	rm -f manuscript.tex

