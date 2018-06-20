################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: Yakindu_ejemplo.axf

# Tool invocations
Yakindu_ejemplo.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"D:\Facultad\Digitales II\Repositorio MCU\lpc_board_nxp_lpcxpresso_1769\Debug" -L"D:\Facultad\Digitales II\Repositorio MCU\lpc_chip_175x_6x\Debug" -Xlinker -Map="Yakindu_ejemplo.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "Yakindu_ejemplo_Debug.ld" -o "Yakindu_ejemplo.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) Yakindu_ejemplo.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "Yakindu_ejemplo.axf"; # arm-none-eabi-objcopy -v -O binary "Yakindu_ejemplo.axf" "Yakindu_ejemplo.bin" ; # checksum -p LPC1769 -d "Yakindu_ejemplo.bin";
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
