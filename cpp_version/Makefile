# include files
CFLAGS :=`pkg-config opencv --cflags` -g -fopenmp
LDFLAGS := `pkg-config opencv --libs` -g -fopenmp
# compile all c++ files in dir
SOURCES :=$(wildcard *.cpp)
# C++ files .cpp removed file is executable
OBJS :=$(SOURCES:.cpp=.o)

all:$(OBJS)
	$(CXX) $(OBJS) $(LDFLAGS) -o pcanet.out

%.o:%.cpp
	$(CXX) -c $< $(CFLAGS) -o $@

clean:
	rm -rf *.o pcanet.out *~ pcanet.*/
print-%  : ; @echo $* = $($*)
