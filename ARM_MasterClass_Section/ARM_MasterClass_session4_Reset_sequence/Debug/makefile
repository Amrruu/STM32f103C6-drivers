################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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
ARM_MasterClass_session2.axf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
ARM_MasterClass_session2.list \

OBJCOPY_BIN += \
ARM_MasterClass_session2.bin \


# All Target
all: ARM_MasterClass_session2.elf secondary-outputs

# Tool invocations
ARM_MasterClass_session2.elf: $(OBJS) $(USER_OBJS) C:\Users\Amr\Desktop\bootloader_for_stm32f407\ARM_MasterClass_session2\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "ARM_MasterClass_session2.axf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\Amr\Desktop\bootloader_for_stm32f407\ARM_MasterClass_session2\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="ARM_MasterClass_session2.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	
	arm-none-eabi-objdump -D ARM_MasterClass_session2.axf > ARM_MasterClass_session2.s
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

ARM_MasterClass_session2.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "ARM_MasterClass_session2.list"
	@echo 'Finished building: $@'
	@echo ' '

ARM_MasterClass_session2.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "ARM_MasterClass_session2.bin"
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
