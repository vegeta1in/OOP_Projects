CXXFLAGS += --std=c++11

main: main.o gas_vehicle.o electric_vehicle.o
	${CXX} ${CXXFLAGS} -o main main.o vehicle.o gas_vehicle.o electric_vehicle.o
main.o: main.cpp *.h
	${CXX} ${CXXFLAGS} -c main.cpp
vehicle.o: vehicle.cpp *.h
	${CXX} ${CXXFLAGS} -c vehicle.cpp
gas_vehicle.o: gas_vehicle.cpp vehicle.o *.h
	${CXX} ${CXXFLAGS} -c gas_vehicle.cpp
electric_vehicle.o: electric_vehicle.cpp vehicle.o *.h
	${CXX} ${CXXFLAGS} -c electric_vehicle.cpp
clean:
	-rm -f *.gch *.o a.out main

