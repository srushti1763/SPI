The Serial Peripheral Interface (SPI) is a widely used synchronous serial communication protocol employed for high-speed data exchange between master and slave devices in embedded systems. In this project, we implement a fully functional SPI Master on the Programmable Logic (PL) section of the MYIR Z-turn board, which is based on the Xilinx Zynq-7020 SoC.

Unlike conventional approaches that rely solely on the Processing System (PS) for SPI control, this design offloads SPI timing and signal generation to the PL for greater flexibility and deterministic control. The SPI Master is implemented using custom Verilog logic or PL-side IP, and is interfaced with external SPI slave devices via assigned GPIO pins acting as MOSI, MISO, SCLK, and SS.

The control and configuration of the SPI Master is handled by C code running on the ARM Cortex-A9 processor in the PS, utilizing memory-mapped I/O to drive the GPIO pins and initiate SPI transactions. This setup enables standalone operation of the SPI interface from the PL while maintaining programmable flexibility from the software side.

This project demonstrates a clean partitioning of hardware and software responsibilities in a Zynq-based SoC and serves as a foundational reference for developing high-performance, custom SPI interfaces in embedded applications.
