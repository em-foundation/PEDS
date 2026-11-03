# BlueJoule-GATT-Secure
+
+- INHERITS [BlueJoule-GATT](bluejoule-gatt.md)
+- Status: experimental RC-26.11 activity; no formal release or fresh scored captures yet
+- Addition: LE Secure Connections / Just Works pairing on every transaction
+- Addition: establish link encryption before application characteristic data access
+- Addition: no bonding and no persistent pairing state
+- Transaction: connect, pairing and encryption setup, targeted GATT discovery, write Command (0x04), read Status (0x84), disconnect, return toward idle/sleep
+- Scored scope: includes connection, pairing/encryption and application exchange; excludes preceding advertising
+- Central: dedicated secure reference central; the ordinary GATT central is not interchangeable
+- PHY and nominal TX power: LE 1M, 0 dBm
+- Measurement parameters and final scan boundaries require validation before publishing scores
+
+Platform keys retain the hardware/implementation names used by ordinary GATT. Secure build/configuration differences must be recorded in capture/build provenance; an inherited platform declaration alone does not specify the secure variant.
+