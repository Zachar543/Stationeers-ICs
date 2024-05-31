# Notes
### stack-loader-recipies.ic10 must be run once on every IC except for icN2OManager

# Bill of Materials

| Qty | Item                       |
|-----|----------------------------|
| 1   | Kit (Advanced Furnace)     |
| 1   | Kit (Digital Valve)        |
| 1   | Kit (Pipe Analyzer)        |
| 1   | Kit (Gas Mixer)            |
| 2   | Kit (Volume Pump)          |
| 2   | Pipe Heater Kit (Gas)      |
| 2   | Kit (Lights)               |
| 3   | Kit (Logic Switch)         |
| 4   | Kit (Tank Insulated)       |
| 4   | Gas Display                |
| 6   | Kit (Logic Memory)         |
| 6   | Kit (Medium Radiator)      |
| 6   | Kit (IC Housing)           |
| 6   | Integration Circuit (IC10) |
| 6   | Hash Display               |
| 15  | Kit (Console)              |

# Naming & Wiring
### ICs
#### icDisplayIngredients
| Port | Device           |
|------|------------------|
| d0   | memIngot1Hash    |
| d1   | memIngot2Hash    |
| d2   | memIngot3Hash    |
| d3   | displayIngotQty1 |
| d4   | displayIngotQty2 |
| d5   | displayIngotQty3 |
#### icDisplayAtmos
| Port | Device           |
|------|------------------|
| d0   | memSelectedAlloy |
| d1   | furnace          |
| d2   | ledPresGood      |
| d3   | ledTempGood      |
| d4   | displayPresOff   |
| d5   | displayTempOff   |
#### icAlloySelector
| Port | Device               |
|------|----------------------|
| d0   | dialSelection        |
| d1   | buttonSelect         |
| d2   | memPreviewHash       |
| d3   | memSelectedAlloy     |
| d4   | memSelectedHash      |
| d5   | icDisplayIngredients |
#### icBufferManager
| Port | Device           |
|------|------------------|
| d0   | memSelectedAlloy |
| d1   | pumpFuel         |
| d2   | pumpCool         |
| d3   | pumpVent         |
| d4   | tankBuffer       |
#### icFurnaceManager
| Port | Device           |
|------|------------------|
| d0   | furance          |
| d1   | memSelectedAlloy |
| d2   | switchEject      |
| d3   | tankBuffer       |
#### icN2OManager
| Port | Device         |
|------|----------------|
| d0   | tankH2         |
| d1   | tankN2O        |
| d2   | heaterH2       |
| d3   | heaterN2O      |
| d4   | mixer          |
| d5   | analyzerOutput |
## Advanced Furnace
  - furnace
## Memory
  - memSelectedHash
  - memSelectedAlloy
  - memPreviewHash
  - memIngot1Hash
  - memIngot2Hash
  - memIngot3Hash
## Volume Pump
  - pumpFuel
  - pumpVent
## Digital Valve
  - pumpCool
## Insulated Tank
  - tankN2O
  - tankH2
  - tankHot
  - tankBuffer
## Pipe Heater
  - heaterN2O
  - heaterH2
## Gas Mixer
  - mixer
## Pipe Analyzer
  - analyzerOutput
## Console

| Type | Name             | Target          |
|------|------------------|-----------------|
| Gas  | Furnace Pressure | furnace         |
| Gas  | Furnace Temp     | furnace         |
| Hash | Furnace Contents | furnace         |
| Hash | Target Alloy     | memSelectedHash |
| Hash | Selected Alloy   | memPreviewHash  |
| Hash | Ingot 1          | memIngot1Hash   |
| Hash | Ingot 2          | memIngot2Hash   |
| Hash | Ingot 3          | memIngot3Hash   |
| Gas  | Buffer Pressure  | tankBuffer      |
| Gas  | Buffer Temp      | tankBuffer      |
## LED Display
  - displayIngotQty1
  - displayIngotQty2
  - displayIngotQty3
  - displayPresOff
  - displayTempOff
## LED Diode
  - ledPresGood
  - ledTempGood
## Dial
  - dialSelection
## Lever
  - switchEject
## Button
  - buttonSelect
