################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
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
CUBE_F4_test.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
CUBE_F4_test.list \

OBJCOPY_BIN += \
CUBE_F4_test.bin \


# All Target
all: CUBE_F4_test.elf secondary-outputs

# Tool invocations
CUBE_F4_test.elf: $(OBJS) $(USER_OBJS) D:\HENGE\My_project\robot\develop\stm32F4\CUBE_PROJECT\test\STM32F407VETX_FLASH.ld
	arm-none-eabi-gcc -o "CUBE_F4_test.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\HENGE\My_project\robot\develop\stm32F4\CUBE_PROJECT\test\STM32F407VETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="CUBE_F4_test.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

CUBE_F4_test.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "CUBE_F4_test.list"
	@echo 'Finished building: $@'
	@echo ' '

CUBE_F4_test.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "CUBE_F4_test.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
