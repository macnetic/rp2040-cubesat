# rp2040-cubesat

## Requirements

| ID  | DESCRIPTION |
|-----|-------------|
| 001 | Device shall include a minimum of one RP2040 integrated circuit. |
| 002 | Dimensions shall conform with PCI/104 form factor. |
| 003 | Device shall supply 1 external UART interface. |
| 004 | Device shall supply 1 external CAN interface. |
| 005 | Device shall supply 1 on-board SPI interface. |
| 006 | Device shall supply 1 on-board I2C interface. |
| 007 | Device shall use a TCXO to generate a stable reference clock. |

## External interfaces

- UART (PHY TBD)
- CAN
- ARM CoreSight-10

## Schematic strategy

The schematics for this project is laid out across multiple sheets. 
The top-level sheets contain functional block diagrams. 
The functional circuit blocks themselves are implemented in the lower-level sheets.

## PCB Layout strategy

A 4-layer controlled impedance stackup is used.

|Layer       | Designation |
|------------|-------------|
| L1 (Top)   | SIG         |
| L2         | GND         |
| L3         | GND         |
| L3 (Bottom)| SIG+PWR     |

Functional circuit blocks are routed first. The blocks are then laid out and connected.

High-speed electrical interfaces are routed with controlled impedance transmission lines.

Priority is given to routing high-speed interfaces.

Sensitive analog circuitry is separated from digital circuitry.

## References

[1] [CubeSat Information - CubeSat.org](https://www.cubesat.org/cubesatinfo)

[2] [CubeSat Kit PCB Specification](https://web.archive.org/web/20220302180556/http://www.cubesatkit.com/docs/CSK_PCB_Spec-A5.pdf) (archived from the original at http://www.cubesatkit.com/docs/CSK_PCB_Spec-A5.pdf)

[3] [RP2040 Documentation](https://www.raspberrypi.com/documentation/microcontrollers/rp2040.html)

[4] 
