################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include USB_DEVICE/Target/subdir.mk
-include USB_DEVICE/App/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Example_LSM6DS3.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Example_LSM6DS3.list \

OBJCOPY_HEX += \
Example_LSM6DS3.hex \


# All Target
all: Example_LSM6DS3.elf secondary-outputs

# Tool invocations
Example_LSM6DS3.elf: $(OBJS) $(USER_OBJS) C:\Users\savvas\Desktop\Example_LSM6DS3\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "Example_LSM6DS3.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\savvas\Desktop\Example_LSM6DS3\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Example_LSM6DS3.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -u _printf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Example_LSM6DS3.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Example_LSM6DS3.list"
	@echo 'Finished building: $@'
	@echo ' '

Example_LSM6DS3.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "Example_LSM6DS3.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
