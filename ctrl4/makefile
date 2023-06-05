# make makefile
#
# Tools used:
#  Compile::Resource Compiler
#  Compile::GNU C
#  Make: make
all : barchart.dll

barchart.dll : barchart.obj barchart.def
	gcc -Zdll -Zomf -Zmap  barchart.obj barchart.def -o barchart.dll
	
barchart.obj : barchart.c barchart.h 
	gcc -Wall -Zomf -c -O2 barchart.c -o barchart.obj

barchart.lib : barchart.obj barchart.def barchart.dll
       $(shell emximp -o barchart.lib barchart.def)

clean :
	rm -rf *exe *res *obj *lib *dll *map
