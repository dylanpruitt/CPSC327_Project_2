CFLAGS = -Wall

all: fileio.o utils.o proj_refactor_file.o
	g++ -o myexe fileio.o utils.o proj_refactor_file.o
	
#rebuild object file if fileio.cpp, or fileio.h or constants.h changes
#compile the .cpp file to an object file (-c)
fileio.o: ../fileio/fileio.cpp ../includes/fileio.h ../includes/constants.h
	g++ $(CFLAGS) -c ../fileio/fileio.cpp
	
utils.o: ../utils/utils.cpp ../includes/utils.h ../includes/constants.h
	g++ $(CFLAGS) -c ../utils/utils.cpp
		
proj_refactor_file.o: proj_refactor_file.cpp ../includes/fileio.h ../includes/utils.h ../includes/constants.h	
	g++ $(CFLAGS) -c ../src/proj_refactor_file.cpp	

clean: 
	$(RM) myexe *.o
