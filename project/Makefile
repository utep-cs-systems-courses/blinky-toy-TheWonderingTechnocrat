#makefile configuration
COMMON_OBJECTS =  main.o redcontrol-c.o
CPU		= msp430g2553
CFLAGS		= -mmcu=${CPU} -I../h
LDFLAGS 	= -L/opt/ti/msp430_gcc/include

#switch the compiler
CC	= msp430-elf-gcc
AS 	= msp430-elf-as

all: main.elf

main.elf: ${COMMON_OBJECTS} redcontrol-c.o
	${CC} ${CFLAGS} -o $@ $^

load: main.elf
	msp430loader.sh $^

clean: $^
	rm -f*.o *.elf


