# Nordic nRF54L15 DK · Zephyr · NCS 3.0.2

- INHERITS [Nordic nRF54L15 DK](../elements/nordic/nrf54l15-dk.md)
- INHERITS [Nordic nRF Connect SDK 3.0.2](../elements/nordic/ncs-3.0.2.md)

- Retained SRAM: default configuration
- LF clock source: LFXO (50 ppm configuration)
- DC-DC converter: enabled
- Compiler optimization: size (`CONFIG_SIZE_OPTIMIZATIONS=y`)

## BlueJoule-GATT 26.11 configuration reference

- Nordic toolchain bundle `66cdf9b75e`; sysbuild; external LF crystal configured at 50 ppm; size optimization.
- [Platform configuration and environment inventory](https://github.com/em-foundation/bluejoule-gatt/tree/RC-26.11/peripheral/platforms/nrf-54l15)
- [Common application and build/load instructions](https://github.com/em-foundation/bluejoule-gatt/tree/RC-26.11/peripheral)

The maintainer built, loaded and observed this baseline working with the reference central on Windows. These links describe the current RC recipe; they do not retroactively change the configuration of older captures. Exact capture attribution should retain source/module revisions and published firmware provenance. Secure GATT is not implied by this ordinary GATT baseline.
