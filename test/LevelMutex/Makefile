include ../Makefile.common

BIN := main$(BIN_SUFFIX)
SRC := main.cpp MultiThreadTests.cpp Thing.cpp ThreadPool.cpp
OBJ := $(SRC:.cpp=.o)
LDLIBS += -lpthread

.PHONY: all clean
all: $(BIN)
clean: cleandeps
	$(RM) $(BIN)
	$(RM) $(OBJ)

$(BIN): $(OBJ)
	$(CXX) $(LDFLAGS) -o $@ $^ $(LDLIBS)

test: $(BIN)
	$(WIN) ./$(BIN)

include ../../Makefile.deps
