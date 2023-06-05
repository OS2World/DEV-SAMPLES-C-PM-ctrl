# make makefile
#
# Tools used:
#  Compile::Resource Compiler
#  Compile::GNU C
#  Make: make
all : text3d.dll

text3d.dll : text3d.obj text3d.def
	gcc -Zdll -Zomf -Zmap  text3d.obj text3d.def -o text3d.dll
	
text3d.obj : text3d.c text3d.h 
	gcc -Wall -Zomf -c -O2 text3d.c -o text3d.obj

text3d.lib : text3d.obj text3d.def text3d.dll
       $(shell emximp -o text3d.lib text3d.def)

clean :
	rm -rf *exe *res *obj *lib *dll *map