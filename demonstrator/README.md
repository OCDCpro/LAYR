![LAYR Logo](pics/LAYR_Logo.png)

# The LAYR 25/26 demonstrator

![LAYR Demonstrator v0.5](pics/demonstrator_v0.5.jpg)

## Description
The LAYR demonstrator is a hardware device. It brings the microchips to live and shows the functionality of the doorlock. Over the span of the LAYR 25/26 challenge the demonstrator goes through some development stages and various enhancements. 

The components of the LAYR hardware kit are used in the demonstrator to assemble a doorlock.

## Schematic V1.0
![High level schematic](schematic/schematic_symbols_v1.0.png)

#### The schematics
[Link to Schematics as OpenOffice document](https://github.com/OCDCpro/LAYR/tree/main/demonstrator/schematic)

#### The symbols
[Link to all the single symbols from the hardware kit, as OpenOffice documents](https://github.com/OCDCpro/LAYR/tree/main/hardware_kit/pics/symbols)

## Pictures V1.0

![LAYR Demonstrator v1.0](pics/demonstrator_v1.0.jpg)

## FPGA prototyping

#### Bitstream for ULX3S 85F FPGA board
There is a bitstream for the ULX3S 85F FPGA board available. This implementations solves all task of the LAYR 25/26 challenge. The HDL sources of the bitstream are not published yet, as they would give away a full solution for the LAYR challenge.

#### Bitstream
[Link to bitstream for ULX3S 85F FPGA](https://github.com/OCDCpro/LAYR/tree/main/demonstrator/bitstream_ulx3s)

#### Flashing the bitstream
The bitstream can be flashed to the ULX3S with the tool fujprog. For the usage, see the readme of fujprog here:

[Link to fujprog](https://github.com/kost/fujprog)

#### ULX3S pinout of the bitstream
This is an extract from the constraints file for the bitstream. It contains not only the pinout, but also additional buffer information for each pin (internal PULL UP / DOWN).

```
LOCATE COMP "rst"    SITE "R1";  # FIRE1
IOBUF  PORT "rst"    PULLMODE=DOWN IO_TYPE=LVCMOS33 DRIVE=4;

LOCATE COMP "mode"        SITE "U18"; # J2_5+  GP14
LOCATE COMP "busy"        SITE "N17"; # J2_7+  GP15
LOCATE COMP "hard_fault"  SITE "N16"; # J2_9+  GP16
LOCATE COMP "unlock"      SITE "L16"; # J2_11+ GP17
LOCATE COMP "spi_sclk"    SITE "D18"; # J2_17+ GP20
LOCATE COMP "spi_cs_1"    SITE "C18"; # J2_23+ GP21
LOCATE COMP "spi_cs_0"    SITE "B15"; # J2_25+ GP22 D15->B15
LOCATE COMP "spi_mosi"    SITE "B17"; # J2_27+ GP23
LOCATE COMP "spi_miso"    SITE "C16"; # J2_29+ GP24
LOCATE COMP "uart_txd"    SITE "D14"; # J2_31+ GP25 B15->D14
LOCATE COMP "uart_rxd"    SITE "B13"; # J2_33+ GP26
LOCATE COMP "uart_clk_in" SITE "D13"; # J2_35+ GP27
IOBUF PORT  "mode"        PULLMODE=NONE IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "busy"        PULLMODE=NONE IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "hard_fault"  PULLMODE=NONE IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "unlock"      PULLMODE=NONE IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "spi_sclk"    PULLMODE=UP IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "spi_cs_1"    PULLMODE=NONE IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "spi_cs_0"    PULLMODE=NONE IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "spi_mosi"    PULLMODE=UP IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "spi_miso"    PULLMODE=NONE IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "uart_txd"    PULLMODE=UP IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "uart_rxd"    PULLMODE=UP IO_TYPE=LVCMOS33 DRIVE=4;
IOBUF PORT  "uart_clk_in" PULLMODE=NONE IO_TYPE=LVCMOS33 DRIVE=4;
```

#### 3V3 supply with the ULX3S
The ULX3s has a built in voltage regulator for converting 5V input to 3V3. In the demonstrator with the ULX3S board, this built in regulator is used instead of the external step-down converter board. Check this in the Kicad schematics of the PCB.

## PCB
![Demonstrator v1.0 PCB editor](pics/demonstrator_v1.0_pcb_editor.png)

![Demonstrator v1.0 PCB white](pics/demonstrator_v1.0_pcb_render_white.png)

![Demonstrator v1.0 PCB green 1](pics/demonstrator_v1.0_pcb_render_green_1.png)

![Demonstrator v1.0 PCB green 2](pics/demonstrator_v1.0_pcb_render_green_2.png)

#### Kicad files
The KiCad files should open with every KiCad version >=8. There are no special libs used for symbols or footprints. Just only the standard libs for KiCad.

[Demonstrator v1.0 PCB Kicad files](https://github.com/OCDCpro/LAYR/tree/main/demonstrator/kicad/demostrator_pcb_v1.0)

[Kicad standard libs](https://www.kicad.org/libraries/download/)





