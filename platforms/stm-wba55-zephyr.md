# STMicroelectronics STM32WBA55CG · Zephyr

- INHERITS [STMicroelectronics NUCLEO-WBA55CG](../elements/stmicroelectronics/nucleo-wba55cg.md)

- Software stack: upstream Zephyr 4.4.1
- Zephyr repository: `https://github.com/zephyrproject-rtos/zephyr`
- Zephyr commit: `1f6485eca25431b5ff27ce9a754218c9e559bbbb`
- Board target: `nucleo_wba55cg`
- Toolchain: Zephyr SDK 1.0.1, GNU Arm GCC 14.3.0
- Tested host environment: Windows; Python 3.13.5, west 1.5.0, CMake 4.4.4
- System power management: enabled, with application-local standby integration
- TX power: application requests nominal 0 dBm through the ST controller command

## BlueJoule-GATT 26.11 baseline

- Ordinary GATT; security and automatic PHY/data-length updates disabled
- Serial console and logging disabled
- Fixed 30 ms advertising interval through the platform support wrapper
- Connected standby enabled; wakeup allowance 500 microseconds
- Device-tree overlay permits RAM-retaining standby
- [Platform configuration, support source and environment inventory](https://github.com/em-foundation/bluejoule-gatt/tree/RC-26.11/peripheral/platforms/stm-wba55)
- [Common application and build/load instructions](https://github.com/em-foundation/bluejoule-gatt/tree/RC-26.11/peripheral)

The baseline includes linker wrappers around ST controller/power-management integration. These are revision-dependent and are part of the platform configuration, not changes to the GATT transaction. Long powered-up intervals around exchanges remain unexplained. This is a best-effort Foundation baseline for vendor improvement, not vendor endorsement or an optimized lower bound.

The frozen manifest records module revisions, including STM32 support. Capture-specific provenance remains authoritative for historical results; the current recipe is not automatically attributed to every older capture.
