include ../Makefile.common

BIN := SafeBitTest$(BIN_SUFFIX)
SRC := SafeBitTest.cpp
OBJ := $(SRC:.cpp=.o)

.PHONY: all clean
all: $(BIN)
clean: cleandeps
	$(RM) $(BIN)
	$(RM) $(OBJ)

$(BIN): $(OBJ)
	$(CXX) $(LDFLAGS) -o $@ $^ $(LDLIBS)

test: $(BIN)
	$(WINE) ./$(BIN)

include ../../Makefile.deps
