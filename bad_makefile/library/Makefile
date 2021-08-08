CC:=gcc
CFLAGS:=-Wall
LIB:=calculator.so

SFILES?=math_functions.h
DESTDIR?=/usr/include

all: $(LIB)

$(LIB):
	$(CC) $(CFLAGS) $(SFILES) -o $(LIB) $^

install: $(LIB)
	install -m 644 $(SFILES) $(DESTDIR)

uninstall:
	rm $(DESTDIR)/$(SFILES)

clean:
	rm -f $(LIB)