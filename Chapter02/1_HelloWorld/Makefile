###############
## TARGETS   ##
###############
# target: prerequisites
#	commands

# The commands are a series of steps typically to make the target,
# 	need to start with a tab character, not space
# The prerequisites are file names, separated by spaces.
# 	These files need to exist before the commands for the target are run.
build:
	g++ main.cc -c
# creates main.o file
	g++ main.o -o main

execute:
	./main

# clean is often used as a target that removes the output of other targets
clean:
	rm -f *.o
	rm -f main

# Namensgebung nicht definiert (build / execute / ... sind keine Keywords)
# es ist einfach auf eine sinnvolle Namensgebung zu achten
