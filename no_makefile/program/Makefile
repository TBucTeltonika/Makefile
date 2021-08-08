LDFLAGS:=-lc
CFLAGS:=-Wall
CPPFLAGS:=-I$(PWD)

BIN:=math
SRC=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)

.PHONY: all clean

all: $(BIN)
#	@echo $(OBJS)

$(BIN): $(OBJS)
	$(CC) -o $@ $^ $(LDFLAGS)

OBJ: 
	$(CC) $(CPPFLAGS) $(CFLAGS) -c $(SRC)

clean:
	rm -f $(BIN) $(OBJS)