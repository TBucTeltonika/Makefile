CC:=gcc
BIN:=main

SOSRC?=file_reader.c
SONAME?=file_reader.so
SRC?=main.c

#Norint paleisti reikia naudoti: "LD_LIBRARY_PATH=`pwd` ./main"

.PHONY : all clean

all: library program
	@echo 'Norint paleisti reikia naudoti: "LD_LIBRARY_PATH=`pwd` ./$(BIN)'

library:
	$(CC) -shared -fPIC  $(SOSRC) -Wl,-soname,$(SONAME) -o $(SONAME)

program: 
	gcc $(SRC) $(SONAME) -o $(BIN)

clean:
	rm -f $(BIN) *.so