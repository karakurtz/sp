CXX = g++
CXXFLAGS = -Wall -g

SRCS = calculator.cpp
OBJS = $(SRCS:.cpp=.o)

LIBS = -lstdc++

TARGET = libcalculator.a
EXECUTABLE = calculator_test

.PHONY: all clean

all: $(TARGET) $(EXECUTABLE)

$(TARGET): $(OBJS)
	ar rcs $@ $^

.INTERMEDIATE: $(OBJS)

$(EXECUTABLE): main.cpp $(TARGET)
	$(CXX) $(CXXFLAGS) -o $@ main.cpp $(TARGET)

clean:
	rm -f $(OBJS) $(TARGET) $(EXECUTABLE)
