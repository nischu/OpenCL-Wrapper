
CFILES  = $(wildcard *.cpp)
OBJS1   = $(notdir $(CFILES))
OBJS2   = $(patsubst %.cpp,%.o, $(OBJS1))
OBJS    = $(addprefix build/,$(OBJS2))	


TARGET := ../platform

$(TARGET): $(OBJS)
	g++ $(GCC_FLAGS) $(OBJS) $(LIBS) -o $(TARGET)

build/%.o : %.cpp
	g++ -c $(INCS) $(GCC_FLAGS) $< -o $@

.PHONY : clean

clean:
	rm -f build/*  $(TARGET)

