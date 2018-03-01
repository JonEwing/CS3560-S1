
# Jonathan Feige 3.01.18

all : college.o collegemain.o course.o
	g++ college.o collegemain.o course.o
	
collegemain.o : collegemain.cc course.h college.h node.h
	cc -c collegemain.cc
college.o : college.cc college.h course.h node.h
	cc -c college.cc
course.o : course.cc course.h
	cc -c course.cc

clean:
	-rm -f *.o core *.core
