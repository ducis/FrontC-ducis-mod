# $Id: Makefile,v 1.1 2007/10/23 09:31:13 casse Exp $

include ../Makefile.head

SOURCES = \
	gen.ml \
	reduce.ml \
	label.ml \
	algo.ml \
	calipso.ml
	
STAT_SOURCES = \
	gen.ml \
	reduce.ml

OCAML_INC += ../frontc
OCAML_LIB += unix bigarray sexplib ../frontc/frontc
OCAMLC_LDFLAGS += -I `ocamlfind query sexplib` -I `ocamlfind query sexplib.syntax`
OCAMLOPT_LDFLAGS += -I `ocamlfind query sexplib` -I `ocamlfind query sexplib.syntax`

$(eval $(call ocaml_prog,calipso,$(SOURCES)))

$(eval $(call ocaml_prog,calipso_stat,$(STAT_SOURCES)))

include ../Makefile.tail
