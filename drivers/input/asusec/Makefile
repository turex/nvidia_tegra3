ifeq ($(CSC_BUILD), true)
	KBUILD_CFLAGS += -DCSC_IMAGE=1
endif
obj-$(CONFIG_ASUSPEC)		+= asuspec.o
obj-$(CONFIG_ASUSDEC)		+= asusdec.o elan_i2c_asus.o
