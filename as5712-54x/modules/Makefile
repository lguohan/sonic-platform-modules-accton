ifneq ($(KERNELRELEASE),)
obj-m:= i2c-mux-accton_as5712_54x_cpld.o  \
        accton_as5712_54x_fan.o accton_as5712_54x_sfp.o \
	cpr_4011_4mxx.o ym2651y.o leds-accton_as5712_54x.o accton_as5712_54x_psu.o 
else
ifeq (,$(KERNEL_SRC))
$(error KERNEL_SRC is not defined)
else
KERNELDIR:=$(KERNEL_SRC)
endif
PWD:=$(shell pwd)
default:
	$(MAKE) -C $(KERNELDIR)  M=$(PWD) modules
clean:
	rm -rf *.o *.mod.o *.mod.o *.ko .*cmd .tmp_versions Module.markers Module.symvers modules.order
endif
