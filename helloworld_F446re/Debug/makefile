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
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
helloworld_F446re.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
helloworld_F446re.list \

OBJCOPY_BIN += \
helloworld_F446re.bin \


# All Target
all: helloworld_F446re.elf secondary-outputs

# Tool invocations
helloworld_F446re.elf: $(OBJS) $(USER_OBJS) C:\ST\STM32CubeIDE_1.4.0\STM32CubeIDE\stm32-examples\helloworld_F446re\STM32F446RETX_FLASH.ld
	arm-none-eabi-gcc -o "helloworld_F446re.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\ST\STM32CubeIDE_1.4.0\STM32CubeIDE\stm32-examples\helloworld_F446re\STM32F446RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="helloworld_F446re.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

helloworld_F446re.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "helloworld_F446re.list"
	@echo 'Finished building: $@'
	@echo ' '

helloworld_F446re.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "helloworld_F446re.bin"
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
