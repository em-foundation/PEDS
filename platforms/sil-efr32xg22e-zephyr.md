# Silicon Labs EFR32xG22E · Zephyr

- INHERITS [Silicon Labs BRD2710A xG22E board target](../elements/silicon-labs/xg22-ek2710a.md)

- Software stack: Silicon Labs Zephyr fork, reports Zephyr 4.4.1
- Zephyr repository: `https://github.com/siliconlabssoftware/zephyr`
- Zephyr commit: `f60fcfc44b27852017a302a08dfe236ccf94804a`
- Board target: `xg22_ek2710a`
- Toolchain: Zephyr SDK 1.0.1, GNU Arm GCC 14.3.0
- Tested host environment: Windows; Python 3.13.5, west 1.5.0
- System power management: enabled
- Controller TX-power configuration: 0 dBm
- EM2 debugging: disabled with `SL_POWER_MANAGER_INIT_EMU_EM2_DEBUG_ENABLE=0`

## BlueJoule-GATT 26.11 baseline

- Ordinary GATT; security and automatic PHY/data-length updates disabled
- Serial console and logging disabled
- [Platform configuration and environment inventory](https://github.com/em-foundation/bluejoule-gatt/tree/RC-26.11/peripheral/platforms/sil-efr32xg22e)
- [Common application and build/load instructions](https://github.com/em-foundation/bluejoule-gatt/tree/RC-26.11/peripheral)

The checked-in frozen manifest records module revisions in addition to the Zephyr commit. This is the Foundation's tested baseline, open to vendor improvements; it does not imply vendor endorsement. Release-time report generation should use the matching PEDS and benchmark revisions. Capture-specific provenance remains authoritative for historical results.
