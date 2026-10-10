# Overall Specifications
- Field strength: **45 mT**
- Bore size: 32mm diameter
# Components
## B0 Magnetics
- Halbach array
- 649 neodymium magnets
- Concentric rings of SLA-printed magnet holders, with FDM spacers
- [Optimizer](https://github.com/MITMRI/mri_magnet_design)
## Gradient
### Gradient Driver
- DAC (DAC8830) with voltage reference (ADR4525)
- Power op-amps in push-pull configuration to allow for bidirectional voltage-controlled current
- Simpler method with H-bridges; output ripple may be concern
### Gradient Coil
- 3x Flex PCB (2-layer, 0.2mm thickness, 1oz copper)
- [Optimizer](https://github.com/MITMRI/CoilGen)
## RF system
- On transmit side, RFPA to amplify FPGA RF signal; alternatively, STHV800/STHV743 ultrasound pulser
- On receive side, LNA feeding into FPGA ADC
- Possible TX/RX switch
- RF coil made of hand wound wire with impedance matching network
## Control
- FPGA: Red Pitaya 125-14
  - Has a nice RF frontend with a sufficiently powerful ADC and also a Zynq SoC
