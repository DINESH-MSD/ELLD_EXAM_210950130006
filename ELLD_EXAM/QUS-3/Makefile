obj-m:=Timer.o
KD=/lib/modules/$(shell uname -r)/build/
PWD:=$(shell pwd)

default:
	$(MAKE) -C $(KD) M=$(PWD) modules
	gcc -o Timer_Application Timer_Application.c
	
clean:
	$(MAKE) -C $(KD) M=$(PWD) clean
	rm Timer_Application

install:
	$(MAKE) -C $(KD) M=$(PWD) modules_install