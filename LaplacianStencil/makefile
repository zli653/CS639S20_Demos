CC = g++
WARNING_FLAGS = -Wall -Wextra -g -O0
EXE = lap
EXE_OPENMP = lap_openmp
NUM = {0..1..1}
#SUBDIR = $(wildcard LaplacianStencil_0_*)

all:
	for num in $(NUM); do \
		#echo $$num; \
		echo LaplacianStencil_0_$$num/main.cpp; \
		$(CC) -o LaplacianStencil_0_$$num/$(EXE) LaplacianStencil_0_$$num/main.cpp LaplacianStencil_0_$$num/Laplacian.cpp ; \
		$(CC) -o LaplacianStencil_0_$$num/$(EXE_OPENMP) LaplacianStencil_0_$$num/main.cpp LaplacianStencil_0_$$num/Laplacian.cpp -fopenmp ; \
		.\$(EXE) ; \
		.\$(EXE_OPENMP) ; \
	done

clean: 
	rm -f ./LaplacianStencil_0_0/*.o
	rm -f ./LaplacianStencil_0_1/*.o
	rm -f ./LaplacianStencil_0_2/*.o
	rm -f ./LaplacianStencil_0_3/*.o
	rm -f ./LaplacianStencil_0_4/*.o
	rm -f ./LaplacianStencil_0_5/*.o
	rm -f ./LaplacianStencil_0_6/*.o
	rm -f ./LaplacianStencil_0_7/*.o

remove:
	rm -f ./LaplacianStencil_0_0/$(EXE) 
	rm -f ./LaplacianStencil_0_1/*.o
	rm -f ./LaplacianStencil_0_2/*.o
	rm -f ./LaplacianStencil_0_3/*.o
	rm -f ./LaplacianStencil_0_4/*.o
	rm -f ./LaplacianStencil_0_5/*.o
	rm -f ./LaplacianStencil_0_6/*.o
	rm -f ./LaplacianStencil_0_7/*.o
	rm -f ./LaplacianStencil_0_0/$(EXE_OPENMP) 
	rm -f ./LaplacianStencil_0_1/*.o
	rm -f ./LaplacianStencil_0_2/*.o
	rm -f ./LaplacianStencil_0_3/*.o
	rm -f ./LaplacianStencil_0_4/*.o
	rm -f ./LaplacianStencil_0_5/*.o
	rm -f ./LaplacianStencil_0_6/*.o
	rm -f ./LaplacianStencil_0_7/*.o