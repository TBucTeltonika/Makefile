LDFLAGS:=-lc
CFLAGS:=-Wall
CPPFLAGS:=-I$(PWD)

BIN:=math
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)

.PHONY: all clean

all: $(BIN)
	@echo $(OBJS)

$(BIN): main.o maths.o usage.o
	$(CC) -o $@ $^ $(LDFLAGS)

%.o: %.clean
	$(CC) $(CPPFLAGS) $(CFLAGS) -c -o $@ $^

clean:
	rm -f $(BIN) $(OBJS)