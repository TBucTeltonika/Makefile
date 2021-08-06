CC:=gcc
CFLAGS:=-Wall
LIB:=calculator.so

PREFIX?=/usr
DESTDIR?=/

all: $(LIB)

$(LIB): 
	$(CC) $(CFLAGS) -c math_functions.h -o $(LIB) $^

install: $(LIB)
	install -m 644 math_functions.h $(DESTDIR)/$(PREFIX)/include

uninstall:
	rm $(DESTDIR)/$(PREFIX)/include/math_functions.h

clean:
	rm -f $(LIB)
