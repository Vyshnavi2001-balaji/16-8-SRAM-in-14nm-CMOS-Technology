# 16-8-SRAM-in-14nm-CMOS-Technology
VLSI Design

In this project, a 16x8 Static Random Access Memory (SRAM) array was developed using advanced 14nm CMOS technology, integrating all essential components such as memory cells, decoders, sense amplifiers, precharge units, and drivers into a top-level layout. The core of the design is a 6T SRAM cell, which employs two cross-coupled inverters and two NMOS access transistors to enable reliable and high-speed read/write operations while maintaining low static power consumption. The compact cell occupies only 0.232 μm², showcasing efficient scaling. The overall 16x8 array supports 128-bit storage with a total area of 74.99 μm². Robust verification processes, including Design Rule Check (DRC) and Layout Versus Schematic (LVS), were successfully completed, ensuring both manufacturability and correctness of the physical implementation.

### Single SRAM Cell
![image](https://github.com/user-attachments/assets/7856ce99-c9ee-4d9e-b606-bf25118792c2)

## 1. Bus Specifications
The bus specifications define the width of different communication channels used within the system:

Address Bus Width: 4 bits
This means the system can access 2^4 = 16 unique memory addresses or locations, indicating a small-scale memory structure such as a 16-word memory block.

Input Data Bus Width: 8 bits
The system accepts 8-bit wide data inputs, allowing it to receive one byte of information per transaction.

Output Data Bus Width: 8 bits
Similarly, the system sends out 8-bit wide data outputs, maintaining consistent data width between input and output operations. This setup is common in byte-addressable systems.

## 2. Electrical Constraints
These constraints ensure reliable circuit operation under specified electrical and environmental conditions:

All constraints are defined for a nominal supply voltage of 0.8 V and a worst-case temperature of 110°C, representing a low-power, high-temperature operating condition, typical in advanced CMOS nodes or harsh environments.

Minimum Read Static Noise Margin (SNM): ≥ 150 mV
SNM is a measure of how resistant the SRAM cell is to noise during a read operation. A margin of at least 150 mV ensures data stability under process, voltage, and temperature (PVT) variations.

Minimum Bit-Line Differential (Read Mode): ≥ 100 mV
This refers to the minimum voltage difference required between the bit lines during a read for the sense amplifier to correctly detect the stored bit. This differential is measured after enabling the sense amplifier, indicating it's taken during an active read access.

Maximum Standby Power Consumption: ≤ 100 µW
The design must consume no more than 100 microwatts in standby mode, emphasizing low-power operation when the circuit is idle—a key factor for battery-operated or energy-efficient systems.

## 3. Design Goal
The overarching objective of the design is to:

Minimize chip area, access time, active power, or the product of all these metrics.
This implies a balanced optimization across multiple design trade-offs. Reducing chip area lowers cost, minimizing access time improves performance, and lowering power enhances energy efficiency. Depending on the application, one may prioritize one or use a figure-of-merit that combines them.

## Top Level Schematic
![image](https://github.com/user-attachments/assets/6007eb18-a4ce-46cd-b374-2dc3ed9aa14e)

## Top Level Layout
![image](https://github.com/user-attachments/assets/a3b32280-8b81-4501-ae1c-4bf077296ac2)

## Summary
This set of design constraints forms a guideline for building a compact, low-power digital system that operates reliably under extreme conditions. It balances functionality (through defined bus widths), robustness (via electrical constraints), and efficiency (through performance and power goals). These constraints are typical for modern embedded SRAMs or custom memory designs in energy-constrained applications.

Additional data on the other blocks is included in the report; please review the report for detailed information.
