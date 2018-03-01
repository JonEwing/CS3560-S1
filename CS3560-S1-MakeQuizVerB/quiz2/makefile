
# Jonathan Feige 3.01.18
CC=g++

OPTIONS=-Wall

all: build archive

build: College

College : college.o collegemain.o course.o
	$(CC) $(OPTIONS) college.o collegemain.o course.o -o College
	
collegemain.o : collegemain.cc course.h college.h node.h
	$(CC) -c $(OPTIONS) collegemain.cc

college.o : college.cc college.h course.h node.h
	$(CC) -c $(OPTIONS) college.cc

course.o : course.cc course.h
	$(CC) -c $(OPTIONS) course.cc

clean:
	-rm -f College college.o collegemain.o course.o

archive: college.cc college.h collegemain.cc course.cc course.h node.h tarray.h makefile
	tar -cvf quiz2_archive.tar college.cc college.h collegemain.cc course.cc course.h node.h tarray.h makefile
