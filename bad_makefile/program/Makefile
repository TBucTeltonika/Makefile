CC:=gcc
CFlags:=-Wall -Ipwd
OBJS:=main.o math_functions.o
BIN:=calculator

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFlags) $(OBJS) -o  $(BIN)

clean:
	rm -f $(BIN) $(OBJS)