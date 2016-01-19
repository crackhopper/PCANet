# compiler
CC := g++
# include files
CFLAGS :=`pkg-config opencv --cflags` -g
LDFLAGS := `pkg-config opencv --libs` -g
# compile all c++ files in dir
SOURCES :=$(wildcard *.cpp)
# C++ files .cpp removed file is executable
OBJS :=$(SOURCES:.cpp=.o)

all:$(OBJS)
	$(CC) $(OBJS) $(LDFLAGS) -o pcanet.out

%.o:%.cpp
	$(CC) -c $< $(CFLAGS) -o $@

clean:
	rm -rf *.o pcanet.out *~
print-%  : ; @echo $* = $($*)
