EMACS=emacs

DOC_EL_SOURCES=../telega.el ../telega-root.el ../telega-filter.el ../telega-sort.el ../telega-chat.el ../telega-modes.el ../contrib/*.el

all: telega-manual.org

telega-manual.org: telega-ellit.org $(DOC_EL_SOURCES)
	$(EMACS) -Q -batch -f package-initialize -L ../ -l telega -L ../../ellit-org.el -l ellit-org --eval '(let ((debug-on-error t)) (ellit-org-export "telega-ellit.org" "telega-manual.org"))'
