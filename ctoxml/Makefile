# $Id$
include ../Makefile.head

SOURCES = \
	ctoxml_bin.ml

OCAML_INC += ../frontc
OCAML_LIB += unix bigarray sexplib ../frontc/frontc
OCAMLC_LDFLAGS += -I `ocamlfind query sexplib` -I `ocamlfind query sexplib.syntax`
OCAMLOPT_LDFLAGS += -I `ocamlfind query sexplib` -I `ocamlfind query sexplib.syntax`

$(eval $(call ocaml_prog,ctoxml,$(SOURCES)))

include ../Makefile.tail
