# Computer Hardware Notes
Computer Hardware — Study Notes

A practical overview of computer hardware, covering its components, functions, working mechanisms, features, use cases, compatibility, and limitations.

# Computer Hardware: Components, Working, and Compatibility

## Table of Contents

1. **Introduction to Computer Hardware**
   - Definition of hardware
   - Main hardware components
   - Hardware compatibility

2. **CPU (Central Processing Unit)**
   - Main functions of a CPU
   - Main parts of a CPU
   - How a CPU works
   - Cores and threads
   - Clock speed and cache
   - Types of CPUs
   - CPU architecture and generations
   - CPU socket types: LGA, PGA, and BGA
   - CPU and motherboard compatibility

3. **Motherboard**
   - Main parts of a motherboard
   - Motherboard form factors: ATX, Micro-ATX, and Mini-ITX
   - Chipset and expansion support
   - VRM and power delivery
   - Motherboard compatibility checklist

4. **BIOS, UEFI, CMOS, and POST**
   - BIOS and UEFI
   - CMOS and motherboard battery
   - POST and startup checks

5. **Memory and Storage**
   - RAM and its purpose
   - RAM types and physical formats: DDR, DIMM, SO-DIMM, and LPDDR
   - RAM compatibility
   - RAM capacity, speed, latency, and memory channels
   - HDD (Hard Disk Drive)
   - SSD (Solid-State Drive)
   - SATA SSD and NVMe SSD
   - M.2 form factor versus NVMe protocol

6. **RAID Storage**
   - What RAID means
   - RAID 0: striping and performance
   - RAID 1: mirroring and redundancy
   - RAID 5: distributed parity
   - RAID capacity and drive-failure tolerance
   - RAID versus backup

7. **Peripheral Devices and Ports**
   - Input devices
   - Output devices
   - Storage and communication peripherals
   - USB-A and USB-C
   - HDMI and DisplayPort
   - Ethernet (RJ45)
   - Audio ports
   - SATA, Thunderbolt, and SD card slots

8. **PCIe Slots and Expansion Cards**
   - What PCIe is
   - PCIe slot sizes: x1, x4, x8, and x16
   - PCIe generations and bandwidth
   - Electrical lanes versus physical slot size
   - Expansion-card compatibility

9. **Integrated and Dedicated Graphics**
   - Integrated GPU (iGPU)
   - Dedicated GPU (dGPU)
   - VRAM and shared system memory
   - Graphics hardware compatibility

10. **Power Supply and Cooling**
    - Power Supply Unit (PSU)
    - Power requirements and connectors
    - CPU and GPU cooling
    - Case airflow
    - Thermal throttling

11. **How the Components Work Together**
    - Startup and hardware initialization
    - Loading the operating system
    - CPU, RAM, storage, and GPU interaction
    - Common performance bottlenecks

12. **Quick Revision**
    - Component functions
    - Key compatibility requirements

13. **Conclusion**
## 1. Introduction to Computer Hardware

Computer hardware refers to the physical parts of a computer that we can see and touch. These components work together to process data, store information, and produce output.

The main hardware components are the CPU, motherboard, RAM, storage drive, power supply, graphics hardware, cooling system, and input/output devices.

A computer needs compatible components to work properly. For example, the CPU must be supported by the motherboard, RAM must match the motherboard's memory type, and the power supply must provide enough power for the installed hardware.

## 2. CPU (Central Processing Unit)

The CPU is often called the brain of the computer because it executes instructions and performs calculations.

### Main functions

- Executes instructions from programs.
- Performs arithmetic and logical operations.
- Controls the flow of data between different parts of the computer.
- Coordinates tasks with memory, storage, and input/output devices.

### Main parts of a CPU

- **Control Unit (CU):** Directs the execution of instructions.
- **ALU (Arithmetic Logic Unit):** Performs mathematical and logical operations.
- **Registers:** Very small, fast storage locations inside the CPU.
- **Cache:** Stores frequently used data and instructions to reduce access time.

### How a CPU works

The CPU repeatedly fetches an instruction from memory, decodes it, executes it, and stores or sends the result where needed. Modern CPUs use techniques such as pipelining, branch prediction, and out-of-order execution to improve performance.

### Cores and threads

A **core** is a physical processing unit inside a CPU. A CPU can have multiple cores so it can handle several tasks at the same time.

A **thread** is a sequence of instructions that can be scheduled for execution. In hardware specifications, the advertised thread count usually refers to the logical processors visible to the operating system.

For example:

- 4 cores and 4 threads: one hardware thread per core.
- 4 cores and 8 threads: two hardware threads per core, commonly through simultaneous multithreading (SMT).
- 8 cores and 16 threads: commonly two hardware threads per core.

Cores and threads do **not** need to match the number of anything on the motherboard. A motherboard socket and chipset must support the CPU, while the operating system and software determine how effectively its cores and threads are used. More threads do not automatically mean twice the performance.

### Clock speed and cache

- **Clock speed:** Measured in GHz. It indicates how many clock cycles the CPU runs through per second. Actual performance also depends on architecture, workload, power limits, and cooling.
- **L1 cache:** Very small and usually the fastest cache.
- **L2 cache:** Larger than L1, but generally slower.
- **L3 cache:** Usually larger and often shared among CPU cores.

A CPU with a higher clock speed is not always faster than another CPU with a lower clock speed, because their designs and the amount of work completed per cycle can differ.

### Types of CPUs

- **Desktop CPUs:** Designed for desktop computers, often with higher power and cooling limits.
- **Laptop CPUs:** Usually designed to balance performance, heat, and battery life.
- **Server CPUs:** Often support many cores, large memory capacities, and reliability features.
- **Mobile processors:** Designed for phones and tablets, with a strong focus on power efficiency.

### CPU architecture and generations

CPU architecture refers to the design of the processor and how it executes instructions. Common instruction set architectures include x86-64 and ARM.

A CPU generation usually introduces changes to performance, efficiency, features, or manufacturing technology. However, a newer generation is not automatically compatible with an older motherboard. Compatibility depends on the exact CPU model, socket, chipset, firmware, and motherboard support.

### CPU socket types: LGA, PGA, and BGA

The socket connects the CPU electrically and mechanically to the motherboard.

- **LGA (Land Grid Array):** The contact pins are in the motherboard socket, while the CPU has flat contact pads.
- **PGA (Pin Grid Array):** The CPU has pins that fit into holes in the socket.
- **BGA (Ball Grid Array):** The processor is soldered directly to the board and is not normally replaceable by the user.

### CPU and motherboard compatibility

The CPU and motherboard must be compatible in several ways:

1. **Socket:** The processor must physically and electrically match the motherboard socket.
2. **Chipset:** The chipset must support the processor's features and platform requirements.
3. **BIOS/UEFI version:** Some motherboards need a firmware update before they can start with certain CPUs.
4. **Power delivery:** The motherboard's voltage regulator design must be suitable for the processor.
5. **Cooling:** The cooler must fit the socket and be capable of removing the CPU's heat.
6. **Physical clearance:** The cooler must fit inside the case and not interfere with nearby components.

Matching the socket alone is not enough. Two processors can use the same socket but still not be supported by every motherboard that uses it.

CPU socket dimensions also do not need to match the size of the processor's cores. Cores are internal parts of the CPU; compatibility is determined by the processor's external interface and platform support.

## 3. Motherboard

The motherboard is the main circuit board that connects the CPU, RAM, storage, graphics card, and other devices. It provides the electrical connections and communication pathways that allow these components to work together.

### Main parts of a motherboard

- **CPU socket:** Holds the processor and provides its electrical connections.
- **RAM slots:** Hold the system memory modules.
- **Chipset:** Provides or manages various connections and platform features, depending on the motherboard design.
- **PCIe slots:** Allow expansion cards such as graphics cards and network cards to be installed.
- **Storage connectors:** Connect SATA drives and, on supported boards, M.2 storage devices.
- **VRM (Voltage Regulator Module):** Converts and regulates power for the CPU and other components.
- **Power connectors:** Receive power from the power supply.
- **Rear I/O ports:** Connect external devices.
- **Firmware chip:** Stores the BIOS/UEFI firmware used during startup.

### Motherboard form factors

| Form factor | General characteristics |
|---|---|
| ATX | Full-size desktop board, generally with more expansion and memory options |
| Micro-ATX | Smaller than standard ATX, usually with fewer expansion slots |
| Mini-ITX | Compact board, typically with one full-size PCIe expansion slot |

Mini-ITX is the common name for the small form factor; “Mini-ATX” is not the usual name for this standard.

A motherboard's form factor affects the size of the case it fits into, but it does not by itself determine CPU compatibility or performance. Check the case's supported form factors and the motherboard's exact specifications.

### Chipset and expansion support

The chipset and CPU platform influence which features are available, such as USB ports, SATA connections, PCIe lanes, overclocking support, and other connectivity options. Some connections come directly from the CPU, while others are provided through the chipset.

A motherboard with a larger price tag does not automatically make the CPU faster. Its main benefits may be better power delivery, more connections, additional expansion slots, or extra features.

### VRM and power delivery

The VRM supplies the CPU with the voltage it needs. A processor that consumes more power can place greater demands on the VRM and cooling system. If power delivery or cooling is insufficient, the CPU may reduce its speed to protect itself.

### Motherboard compatibility checklist

Before choosing a motherboard, check:

- CPU socket and supported processor list.
- Required BIOS/UEFI version.
- RAM type, maximum capacity, supported speeds, and number of slots.
- Case form factor and motherboard mounting points.
- Available PCIe slots and their electrical lane configurations.
- Storage connectors and supported drive types.
- Power connectors and CPU power requirements.
- Rear and internal ports needed for your devices.

## 4. BIOS, UEFI, CMOS, and POST

BIOS and UEFI are types of motherboard firmware. They initialize hardware and help start the operating system. UEFI is the modern successor to traditional BIOS and supports features such as modern boot methods and GPT disks.

**POST (Power-On Self-Test)** is an early startup process that checks whether essential hardware can initialize. If something goes wrong, the motherboard may display an error code, light an indicator, or produce beep codes, depending on the model.

**CMOS** is a term historically associated with the small amount of memory used to retain firmware settings. Modern systems generally store settings in non-volatile memory, but the term “CMOS settings” is still commonly used.

A motherboard battery typically maintains the real-time clock and certain settings when the computer is unplugged. If the clock repeatedly resets, the battery may need replacement.

## 5. Memory and Storage

Memory and storage are both used to hold data, but they serve different purposes.

- **RAM** temporarily holds the programs and data currently in use.
- **Storage** keeps files and installed programs even when the computer is turned off.

### RAM (Random Access Memory)

RAM is the computer's working memory. When a program runs, the operating system loads the required data and instructions from storage into RAM so the CPU can access them quickly.

RAM is volatile, meaning its contents are lost when power is removed.

### RAM types and physical formats

**DDR (Double Data Rate)** is the family of memory technology used in many computers. DDR3, DDR4, and DDR5 are different generations and are not generally interchangeable.

- **DIMM:** The larger memory module format commonly used in desktop computers.
- **SO-DIMM:** A smaller module format used in many laptops and compact computers.
- **LPDDR:** Low-power memory commonly used in phones, tablets, and thin laptops. It is often soldered directly onto the board.

DIMM and SO-DIMM refer to module formats, while DDR generations refer to memory technology. They are not the same thing.

### RAM compatibility

RAM must match the memory type supported by the motherboard and CPU platform. For example, a DDR4 module cannot be installed in a DDR5 slot. The notch position and electrical design differ.

When selecting RAM, check:

- DDR generation.
- DIMM or SO-DIMM format.
- Supported capacity per slot and total capacity.
- Supported memory speed.
- Number of memory channels.
- Whether the memory is buffered or unbuffered, and ECC or non-ECC, as required by the platform.

A module may physically fit but still not run at its advertised speed. The system may operate it at a lower supported speed, depending on the CPU, motherboard, firmware, and memory configuration.

### RAM speed, latency, and channels

- **Capacity:** How much data RAM can hold at once.
- **Data rate:** How quickly data can be transferred, commonly expressed in MT/s.
- **Latency:** The delay before a memory operation returns data.
- **Memory channels:** Separate pathways that can increase available memory bandwidth when populated correctly.

Two memory modules do not need to have the same capacity in every system, but matched modules are often easier to configure and can provide balanced dual-channel operation. The exact behavior depends on the platform.

For example, two 8 GB modules in a supported dual-channel configuration can provide more memory bandwidth than one 16 GB module. This does not mean the total capacity is higher; both configurations provide 16 GB.

More RAM helps when the computer is running out of memory. It does not automatically improve every task once enough RAM is available.

### HDD (Hard Disk Drive)

An HDD stores data magnetically on spinning platters. A mechanical read/write head accesses the data.

Advantages:
- Usually offers a lower cost per gigabyte.
- Available in large capacities.
- Useful for backups, archives, and large media collections.

Limitations:
- Slower access times than SSDs.
- Moving parts can be affected by physical shock.
- Usually noisier and uses more power than a comparable SSD.

### SSD (Solid-State Drive)

An SSD stores data in flash memory and has no spinning platters.

Advantages:
- Faster access times than HDDs.
- Faster system startup and application loading.
- Silent operation and better resistance to ordinary movement.

Limitations:
- Usually costs more per gigabyte than an HDD.
- Flash memory has finite write endurance, although modern SSDs are designed to handle normal workloads for years.
- Performance can vary depending on the drive, interface, workload, and remaining free space.

### SATA SSD and NVMe SSD

A SATA SSD uses the SATA interface, which was originally designed for storage devices including hard drives. An NVMe SSD uses the NVMe protocol over PCIe, commonly offering much higher bandwidth and lower overhead.

**M.2 is a physical form factor and connector, not a storage protocol.** An M.2 drive may use SATA or PCIe/NVMe, depending on the drive and motherboard. The specifications must explicitly support the type of drive being installed.

Before buying a drive, check the motherboard's M.2 slot support, drive length, interface, and any lane-sharing restrictions. Some M.2 installations can disable certain SATA ports or share bandwidth with other devices.

## 6. RAID Storage

RAID stands for Redundant Array of Independent Disks. It combines multiple drives to improve performance, provide redundancy, or both, depending on the RAID level.

### RAID 0

RAID 0 spreads data across two or more drives to improve performance and combine their capacities.

- Requires at least two drives.
- Provides no redundancy.
- If one drive fails, the entire array can become unusable.

For example, two 1 TB drives can provide about 2 TB of usable capacity in RAID 0, but either drive failing can cause data loss across the array.

RAID 0 is useful when speed and capacity matter more than fault tolerance. It is not suitable as the only location for important data.

### RAID 1

RAID 1 mirrors data across drives.

- Usually requires at least two drives.
- Provides redundancy against the failure of one drive in a two-drive mirror.
- Usable capacity is generally equal to the capacity of the smallest drive in the mirror.

For example, two 1 TB drives provide about 1 TB of usable capacity.

RAID 1 can keep a system running after a drive failure, but it does not protect against accidental deletion, malware, theft, or damage affecting both drives.

### RAID 5

RAID 5 distributes data and parity information across at least three drives. The parity information allows the array to recover from the failure of one drive.

- Requires at least three drives.
- Can tolerate one drive failure.
- Usable capacity is approximately the capacity of the smallest drive multiplied by the number of drives minus one.

For example, three 2 TB drives provide about 4 TB of usable capacity before formatting and other overhead.

RAID 5 has more write overhead than RAID 0 and can take time to rebuild after a drive replacement. A second drive failure during a rebuild can cause data loss.

### RAID versus backup

RAID and backup solve different problems. RAID mainly helps with availability or performance. A backup is a separate copy of data that can be restored after deletion, corruption, malware, or other loss.

Important data should be backed up to a separate device or location, and the backups should be tested periodically. RAID should not be treated as a replacement for backups.

## 7. Peripheral Devices and Ports

Peripheral devices connect to the computer to provide input, output, or additional functions.

- **Input devices:** Keyboard, mouse, microphone, scanner, webcam.
- **Output devices:** Monitor, speakers, printer, projector.
- **Storage devices:** External drives and USB flash drives.
- **Communication devices:** Network adapters and wireless adapters.

### Common ports

| Port | Common use |
|---|---|
| USB-A | Keyboards, mice, flash drives, and many accessories |
| USB-C | A connector used for data, power, and sometimes display output |
| HDMI | Digital video and audio to displays |
| DisplayPort | Digital video and audio, commonly used with computer monitors |
| Ethernet (RJ45) | Wired network connection |
| 3.5 mm audio jack | Headphones, speakers, or microphones, depending on the jack |
| SATA | Internal storage drives |
| Thunderbolt | High-speed data, display, and docking connections on supported hardware |
| SD card slot | Reading memory cards |

USB-C describes the connector shape, not a guaranteed speed or feature set. A USB-C port may support basic USB data only, or it may also support high-speed data, charging, and video output. Check the device specifications.

Likewise, HDMI and DisplayPort capabilities depend on the exact version and the devices connected. The port alone does not guarantee a particular resolution or refresh rate.

## 8. PCIe Slots and Expansion Cards

PCIe (Peripheral Component Interconnect Express) is a high-speed connection standard used by graphics cards, network cards, capture cards, and some storage devices.

Common physical slot sizes include:
- PCIe x1
- PCIe x4
- PCIe x8
- PCIe x16

The number indicates the physical slot or lane configuration, but physical size and electrical lane count can differ. A long x16 slot, for example, may be wired for fewer than 16 lanes.

PCIe generations increase the amount of data that can be transferred per lane. A newer PCIe device can often work in an older compatible slot, but it will generally operate at the capabilities supported by both ends.

Before installing an expansion card, check:
- Whether the motherboard has a suitable slot.
- How many electrical lanes the slot provides.
- Whether other slots or M.2 drives share those lanes.
- Whether the card needs extra power.
- Whether it fits inside the case and has enough cooling.

A graphics card may physically fit into a PCIe x16 slot but still require a suitable power supply, sufficient case clearance, and compatible software drivers.

## 9. Integrated and Dedicated Graphics

Graphics hardware processes images, video, and 3D workloads.

### Integrated GPU (iGPU)

An integrated GPU is built into the processor or included as part of the same platform package. It commonly uses system RAM instead of having its own dedicated graphics memory.

Advantages:
- Lower cost and power consumption.
- Suitable for everyday work, video playback, and some games.
- Does not require a separate graphics card.

Limitations:
- Performance depends on the specific GPU and memory configuration.
- It shares system memory with the CPU.
- It may not be powerful enough for demanding games or professional graphics workloads.

Not every CPU has an integrated GPU. A computer may need a dedicated graphics card to produce display output if its processor lacks integrated graphics.

### Dedicated GPU (dGPU)

A dedicated GPU is a separate graphics processor, usually installed on a graphics card in desktop computers or built into some laptop designs. It typically has its own video memory called VRAM.

Dedicated GPUs are commonly used for demanding games, 3D rendering, video editing, and other graphics-intensive tasks. They generally consume more power and produce more heat than basic integrated graphics.

A dedicated graphics card requires a compatible expansion slot, enough power, sufficient physical space, and appropriate cooling.

## 10. Power Supply and Cooling

### Power Supply Unit (PSU)

The PSU converts power from the wall outlet into the voltages used by the computer's components.

When selecting a PSU, consider:
- Total power requirements of the CPU and graphics card.
- Required motherboard and graphics-card power connectors.
- PSU quality and efficiency.
- Case size and cable compatibility.
- Some extra capacity for short power spikes and future upgrades.

A PSU's wattage rating alone does not guarantee quality. A poor-quality unit can cause instability or potentially damage hardware.

### Cooling system

CPUs and GPUs produce heat while operating. Cooling systems transfer this heat away using heatsinks, fans, and sometimes liquid cooling.

If temperatures become too high, a processor or GPU may reduce its clock speed to protect itself. This is called thermal throttling.

The cooler must be compatible with the CPU socket, fit inside the case, and handle the component's heat output. Case airflow also matters because the cooler needs access to cooler air and a path for hot air to escape.

## 11. How the Components Work Together

When the computer is switched on, the motherboard firmware initializes the hardware and performs early checks. It then starts the boot process and loads the operating system from storage into RAM.

When a program runs, its instructions and required data are loaded into RAM. The CPU processes those instructions, while the GPU handles graphics tasks when needed. The motherboard provides the connections that allow these components to communicate.

Files are saved to an HDD or SSD so they remain available after shutdown. Peripheral devices connect through the motherboard's ports or through expansion cards.

The performance of a computer depends on how well its components work together. A fast CPU may be held back by insufficient RAM, slow storage, poor cooling, or an unsuitable workload. Similarly, installing a powerful GPU does not guarantee better performance if the application is limited by the CPU or another part of the system.

## 12. Quick Revision

| Component | Main purpose | Important compatibility point |
|---|---|---|
| CPU | Executes instructions | Socket, chipset, firmware, power and cooling |
| Motherboard | Connects hardware | CPU support, form factor, RAM and expansion options |
| RAM | Holds active data | DDR generation, module format, capacity and supported speed |
| HDD | High-capacity storage | SATA connection, size and power |
| SSD | Fast persistent storage | SATA or NVMe interface, form factor and slot support |
| RAID | Combines multiple drives | RAID level, number of drives and backup plan |
| GPU | Processes graphics | Slot, power, case clearance and cooling |
| PSU | Supplies electrical power | Wattage, connectors and quality |
| Cooling system | Removes heat | Socket compatibility, clearance and cooling capacity |
| Peripheral ports | Connect external devices | Connector, protocol and supported features |
| PCIe | Connects expansion cards | Slot size, lane count and generation |

## Conclusion

Computer hardware is not just about knowing the names of individual components. It is also important to understand compatibility and how the components depend on one another. A CPU needs a supported motherboard, RAM must match the platform, storage needs the correct interface, and the power supply and cooling system must handle the installed hardware. Understanding these relationships makes it easier to build, upgrade, and troubleshoot a computer.