IDIR = ../include
CC=g++
CFLAGS=-I$(IDIR) -std=c++17 -g

ODIR=../src

.PHONY: all

_OBJ = maquina-de-turing.o cinta.o transicion.o estado.o main.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))

all: maquina-de-turing


$(ODIR)/maquina-de-turing.o: $(ODIR)/maquina-de-turing.cpp $(IDIR)/maquina-de-turing.hpp
	$(CC) -c -o $@ $< $(CFLAGS)

$(ODIR)/cinta.o: $(ODIR)/cinta.cpp $(IDIR)/cinta.hpp
	$(CC) -c -o $@ $< $(CFLAGS)

$(ODIR)/estado.o: $(ODIR)/estado.cpp $(IDIR)/estado.hpp
	$(CC) -c -o $@ $< $(CFLAGS)

$(ODIR)/transicion.o: $(ODIR)/transicion.cpp $(IDIR)/transicion.hpp
	$(CC) -c -o $@ $< $(CFLAGS)

$(ODIR)/main.o: $(ODIR)/main.cpp
	$(CC) -c -o $@ $< $(CFLAGS)

maquina-de-turing: $(OBJ)
	$(CC)  -o $@ $^ $(CFLAGS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o ./P1