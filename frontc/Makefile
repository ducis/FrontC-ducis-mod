# $Id$
include ../Makefile.head

# Library
SOURCES = \
	cabs.ml \
	cxml.ml \
	cprint.ml \
	clexer.mll \
	cparser.mly \
	ctoxml.ml \
	frontc.ml
OCAMLYACC_FLAGS = -v
DUCIS_MOD_FLAGS = -pp "camlp4o -I `ocamlfind query type_conv` -I `ocamlfind query sexplib` pa_type_conv.cma pa_sexp_conv.cma" \
	-I `ocamlfind query sexplib`
OCAMLC_CFLAGS += $(DUCIS_MOD_FLAGS) 
OCAMLOPT_CFLAGS += $(DUCIS_MOD_FLAGS)

$(eval $(call ocaml_lib,frontc,$(SOURCES)))

INSTALL_AFTER += install_doc
include ../Makefile.tail


# Documentation
DOCS = \
	cabs.ml \
	cxml.ml \
	cprint.ml \
	ctoxml.ml \
	frontc.ml

DOC_FLAGS=-colorize-code -I .
doc:
	ocamldoc -html -d ../autodoc  -t "FrontC" $(DOCS)

install_doc: doc $(DATA_DIR)
	cp -R ../autodoc $(DATADIR)
	
