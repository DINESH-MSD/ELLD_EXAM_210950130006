obj-m:=Driver.o
KD=/lib/modules/$(shell uname -r)/build/
PWD:=$(shell pwd)

default:
	$(MAKE) -C $(KD) M=$(PWD) modules
	gcc -o APP_READ APP_READ.c
	gcc -o APP_WRITE APP_WRITE.c
	gcc -o APP_IOCTL APP_IOCTL.c

clean:
	$(MAKE) -C $(KD) M=$(PWD) clean
	rm APP_READ APP_WRITE APP_IOCTL

install:
	$(MAKE) -C $(KD) M=$(PWD) modules_install