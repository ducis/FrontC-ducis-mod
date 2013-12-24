# $Id: Makefile,v 1.1 2007/10/01 20:45:15 casse Exp $
include ../Makefile.head

SOURCES = \
        printc_bin.ml

OCAML_INC += ../frontc
OCAML_LIB += unix bigarray sexplib ../frontc/frontc
OCAMLC_LDFLAGS += -I `ocamlfind query sexplib` -I `ocamlfind query sexplib.syntax`
OCAMLOPT_LDFLAGS += -I `ocamlfind query sexplib` -I `ocamlfind query sexplib.syntax`

$(eval $(call ocaml_prog,printc,$(SOURCES)))

include ../Makefile.tail
