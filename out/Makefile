INFILE =	../src/cryptowill.asc
BOOK_ASC = cryptowill.asc

all: pdf html

tmp: $(INFILE)
	cp -f $(INFILE) .

pdf:	tmp
	a2x -fpdf -k --fop -v $(BOOK_ASC)

html: tmp
	asciidoc -a theme=volnitsky $(BOOK_ASC)

clean:
	rm -rf *.xml
	rm -rf *.fo
	rm -rf *.asc

nuke: clean
	rm -rf *.pdf
	rm -rf *.epub
	rm -rf .html
