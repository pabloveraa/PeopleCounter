all: slave

CFLAGS=-fPIC -g -Wall -O2 `pkg-config --cflags opencv`
LIBS = `pkg-config --libs opencv`
INCLUDE = -I/home/orbbec/OpenNI-Linux-Arm-2.3/OpenNI-Linux-Arm-2.3/Include
FREE_LIBS =  -L/home/orbbec/OpenNI-Linux-Arm-2.3/OpenNI-Linux-Arm-2.3/Redist -lOpenNI2

slave: slave.cpp
	$(CXX) $(INCLUDE) $(CFLAGS) $? -o $@ $(LIBS) $(FREE_LIBS)

%.o: %.cpp
	$(CXX) -c $(CFLAGS) $< -o $@

clean:
	rm -rf *.o test
