EXEC=bundle exec
SRC=cw-presentation.adoc
EPUB_SRC=cw-presentation-master.adoc
PLUGINS=-r asciidoctor-diagram -r asciidoctor-mathematical
CODERAY=-a source-highlighter=coderay

all: reveal pdf epub

reveal:
	$(EXEC) asciidoctor-revealjs $(PLUGINS) $(SRC)

pdf:
	$(EXEC) asciidoctor-pdf $(PLUGINS) $(CODERAY) $(SRC)

epub:
	$(EXEC) asciidoctor-epub3 $(PLUGINS) $(CODERAY) $(EPUB_SRC)

server:
	ruby -run -e httpd . -p 5000 -b 0.0.0.0
