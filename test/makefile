
CXX = g++

COMP_OPT = -g -m64 -fpermissive

LIBS = 

TARGETS = mallocTest

all: ${TARGETS}

mallocTest: mallocTest.o
	$(CXX) $(COMP_OPT) -o $@ $^ $(LIBS)

%.o: %.cpp
	$(CXX) $(COMP_OPT) -c $<

check: all
	gdb -q -x verify.py

clean:
	rm *.o ${TARGETS}
