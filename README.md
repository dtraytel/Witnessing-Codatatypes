This repository contains supplementary material related to the paper

    Witnessing (Co)datatypes
    Jasmin Blanchette, Andrei Popescu, Dmitriy Traytel

The archive codata_wit_devel.tar.gz contains details and pointers concerning the
Isabelle development reported in the paper:

1. Pointers to the ML code handling witnesses,
2. The derivation trees case study,
3. Sample (co)datatype declarations with computed witnesses.

The development has been integrated in the Isabelle2014 distribution, 
available at: 

  http://isabelle.in.tum.de

More details are given below.


1. ML code

The (co)datatype package is located in the Isabelle distribution at:
   
    src/HOL/Tools/BNF

The code handling witnesses (described in the paper's section 5) is located at

    src/HOL/Tools/BNF/bnf_def.ML               (for basic BNFs)
    src/HOL/Tools/BNF/bnf_comp.ML              (for composition)
    src/HOL/Tools/BNF/bnf_comp_tactics.ML
    src/HOL/Tools/BNF/bnf_lfp.ML               (for initial algebras / datatypes)
    src/HOL/Tools/BNF/bnf_lfp_tactics.ML
    src/HOL/Tools/BNF/bnf_gfp.ML               (for final coalgebra / codatatypes)
    src/HOL/Tools/BNF/bnf_gfp_tactics.ML

The *_tactics.ML files certify the witnesses, which are produced (as Isabelle
terms) in the other files.

2. Derivation trees

The theories are available in this archive in both pdf and html-browsable forms.

The Isabelle sources for the generated files are located in the Isabelle
distribution at

    src/HOL/BNF_Examples/Derivation_Trees

The theory DTree contains the definition of the derivation-tree codatatype.  For
convenience, it also transports the package-produced facts from the type "'a
fset" of finite sets over 'a, to the more standard (and better supported) type
"'a set" of arbitrary sets over 'a.

The theory Gram_Lang develops the theory of grammar-generated languages
discussed in the paper.  

The notations are mostly identical to the ones used in the paper, so that the
reader should be able to identify in the formal scripts the relevant
constructions and facts.


3. Sample (co)datatype declarations

The theory Sample in this archive contains the (co)datatype declarations
examplified in the paper.

