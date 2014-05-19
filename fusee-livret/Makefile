all: fusee-petitlivre.pdf 

include LaTeX.mk

# Fabrique le livret de l'animateur
###################################

# (bon, en fait, il n'existe pas encore)

# Fabrique le petit livre du participant
########################################

fusee-petitlivre.pdf: fusee-petitlivre-page1.pdf fusee-petitlivre-page2.pdf
	pdfjoin fusee-petitlivre-page1.pdf fusee-petitlivre-page2.pdf --outfile fusee-petitlivre.pdf

fusee-petitlivre-page1.pdf: fusee-petitlivre-content.pdf
	./petit-livre.sh fusee-petitlivre-content.pdf fusee-petitlivre-page1.pdf

img/%.pdf: img/%.svg
	inkscape --export-pdf=$@ $<

clean::
	rm -f fusee-petitlivre-page1.pdf fusee-petitlivre-page2.pdf fusee-petitlivre-content.pdf