
# Kernel makefile for motions sensors
#
#

# MPU
obj-$(CONFIG_MPU_SENSORS)+=
ifdef CONFIG_MPU_SENSORS_MPU3050
MPU_MODULE_NAME := mpu3050
endif

obj-$(CONFIG_MPU_SENSORS)	+= $(MPU_MODULE_NAME).o

$(MPU_MODULE_NAME)-objs += mpuirq.o \
	slaveirq.o \
	mpu-dev.o \
	mpu-i2c.o \
	mlsl-kernel.o \
	mlos-kernel.o \
	$(MLLITE_DIR)mldl_cfg.o

#
# Accel options
#
ifdef CONFIG_MPU_SENSORS_KXTF9
$(MPU_MODULE_NAME)-objs += $(MLLITE_DIR)accel/kxtf9.o
endif

#
# Compass options
#
ifdef CONFIG_MPU_SENSORS_AK8975
$(MPU_MODULE_NAME)-objs += $(MLLITE_DIR)compass/ak8975.o
endif

EXTRA_CFLAGS += -I$(M)/$(MLLITE_DIR) \
		-I$(M)/../../include \
		-Idrivers/misc/mpu3050 \
		-Iinclude/linux

obj-$(CONFIG_MPU_SENSORS_TIMERIRQ)+= timerirq.o
