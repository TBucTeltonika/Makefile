CC:=gcc
BIN:=main
Libpath=$(shell pwd)

#export LD_LIBRARY_PATH
#nepavyko su LD_LIBRARY_PATH nezinau kodel bandziau ivairius budus bet kazkaip vis nerasdavo to .so failo.
#ikelus faila tiesiai i usr/local/bin problemu nebuvo.
#kodas truputi nesvarus nes palikau kas nepavyko.

.PHONY : all clean addlibpath run

all: library addlibpath program  run
#	@echo $("kompiliuojama")

library:
#	$(CC) -Wall -g -c file_reader.c -o file_reader.o
	$(CC) -shared -fPIC -o file_reader.so file_reader.c -Wl,-soname,/usr/local/lib/file_reader.so

program: 
	gcc main.c /usr/local/lib/file_reader.so -o $(BIN)
#	$(CC)  -Wall main.c  -o $(BIN) file_reader.o

addlibpath:
	LD_LIBRARY_PATH=$(Libpath)
#ldconfig
	@echo $(LD_LIBRARY_PATH)
	

run:
	./main

clean:
	rm -f $(BIN) *.so