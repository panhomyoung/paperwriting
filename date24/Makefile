all: compile 
target=DATE24

pdf:
	pdfopen ${target}.pdf

compile:
	pdflatex ${target}.tex
	bibtex ${target}.aux
	pdflatex ${target}.tex
	bibtex ${target}.aux
	pdflatex ${target}.tex

clean:
	rm -rf *.log
	rm -rf *.aux
	rm -rf *.bbl
	rm -rf *.pdf

git:
	git add *.tex
	git add Makefile
#	git add content/*.tex
	git commit -m "update"
	git push
