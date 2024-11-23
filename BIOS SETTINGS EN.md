## CPU Common Options
#### RedirectForReturnDis = Auto
???
#### Platform First Error Handling = Disabled
A technology where system errors are first handled by the platform (processor or chipset) rather than the operating system. For regular users, it can be left as **Disabled**, as operating systems generally handle errors efficiently.
#### Core Performance Boost = Auto
Disabling CPU turbo boost
#### Global C-state Control = Enabled
Power-saving states of the processor, where parts of the processor can temporarily shut down or switch to less power-intensive modes to save energy. **Enabled** is a good choice for most users, as it reduces power consumption without significantly impacting performance. If you want to maximize performance (e.g., for high-load workstations or gaming systems), you can choose **Disabled**, but this will increase power consumption and heat generation.
#### Opcache Control = Enabled
Cache for frequently used processor instructions that helps speed up program execution. Choosing **Enabled** is recommended for most users, as it increases performance by more effectively utilizing the instruction cache. **Disabled** may only be useful in specific scenarios where special control over the processor is required (e.g., for debugging).
#### SEV ASID Count = Auto
???
#### SEV-ES ASID Space Limit Control = Auto
???
#### Streaming Stores Control = Enabled
Optimization for data write operations, allowing the processor to bypass the cache and write data directly to RAM. **Enabled** is recommended for applications that work actively with large volumes of data and frequently perform memory writes (e.g., scientific computing, databases, rendering). In regular user systems, you can leave it **Disabled** if there is no need for write optimization.
#### Local APIC Mode = Auto
???
#### ACPI _CST C1 Declaration = Enabled
This concerns power management through ACPI (Advanced Configuration and Power Interface). C1 is one of the power-saving states known as the "halt" state. Enabling this option allows the operating system to declare support for this state, which can help improve energy savings. It is usually better to leave this **Enabled** so that the system can use all power-saving features.
#### MCA error thresh enable = True
???
#### MCA error thresh count = Stock value
???
#### SMU and PSP Debug Mode = Auto
???
#### PPIN Opt-in = Disabled
This is a unique processor identifier that can be used for identification and tracking. Enabling this option allows the operating system or other programs to access this identifier. If you are concerned about privacy and do not use applications that require this information, it is better to leave it **Disabled**.

## CPU Debug Options
### Cache
#### L3 way locking = FOURTEEN
This is a BIOS setting that allows control over the availability of a certain number of "ways" in the third-level cache (L3 cache) of the processor. For most users and standard workloads, it is better to choose **FOURTEEN** (or the maximum value), as this will ensure the best performance.
#### L3 Range Lock Enable = Disabled
The "L3 Range Lock Enable" setting in BIOS is related to managing access to the third-level cache (L3) on AMD processors. This feature can be used to control access to certain regions of the L3 cache, which may be useful for some applications or for security purposes. It is recommended to leave this option **Disabled**. This will allow applications to use the entire available L3 cache without restrictions.

### General Processor Control
#### SMEE = Disabled
Enables or disables the memory encryption feature. Secure Memory Encryption (SME) helps protect data in RAM from unauthorized access.

### Power Management
#### ACPI _PSS = Enabled
These are ACPI tables that describe the performance states (P-states) supported by the processor. P-states are used to manage the clock speed and voltage of the processor to save energy and manage heat output. Depending on the processor load, the system can switch between different P-states to optimize energy consumption and performance.
#### ACPI C3 Control = LPI
**ACPI C3 Control** determines how the system will manage the transition of the processor to the C3 state, one of the deep power-saving states. In C3 state, the processor significantly reduces power consumption, but it increases the latency when returning to the active state.

## DF Common Options
#### CVIP Reserved Memory Disable = Disabled
CVIP Core not used -> Disabled
#### GlobalReqBandwidthControl = Enabled
**GlobalReqBandwidthControl** manages the global control of memory request bandwidth. This may include prioritizing and managing memory access for various system components.
#### CC6 memory region encryption = Disabled
This option manages the encryption of memory regions when the processor enters the CC6 power-saving state. This can help protect data in memory when the processor transitions to low-power states.
#### DF Cstates = Enabled
This option manages power-saving states for Data Fabric (DF), which allow for reduced power consumption when DF is not actively used. Enabling this option can improve the system's power consumption by allowing Data Fabric to enter low-power states.

## UMC Debug Options:

#### Address Command Tristate Enable = Enabled
This setting manages the state of the memory address bus in standby mode. When enabled, the memory address lines are put into a high-impedance state ("tristate") during idle periods (lack of memory operations). This can help reduce power consumption and electromagnetic interference (EMI).
#### On DIMM Temperature Sensor Enable = Disabled
This setting activates the temperature sensor built into memory modules (if supported). The sensor can be used to monitor RAM temperature and prevent overheating.
#### DBI (Data Bus Inversion) = Enabled
This feature is used to manage data inversion on the memory bus. It helps reduce electromagnetic interference (EMI) and improve memory stability at high frequencies. If the number of "1"s in the transmitted data exceeds a certain threshold, the data is inverted to reduce current fluctuations.
#### Data Encryption = Disabled
This setting controls the use of data encryption during information transfer between the processor and RAM. In modern systems with AMD processors, especially on server or high-performance platforms, memory encryption technology such as AMD Memory Guard may be used to protect data from unauthorized access.
#### DRAM Temperature Controlled Refresh Mode = Disabled
This setting regulates the data refresh rate in RAM based on its temperature. In DRAM, data is periodically refreshed to prevent data loss. At higher memory temperatures, more frequent refresh is required.
#### ProcOdtAlwaysOn = Enabled
This option specifies that **On-Die Termination (ODT)** on the processor should always remain enabled. The processor will maintain signal termination constantly, regardless of whether data transmission is currently in use or not.
#### RRW Memory Test for all PStates = Disabled
#### Memory Context Restore = Enabled
#### CmdThrottleMode = lower
This is a BIOS setting that manages the "Command Throttle" mode for the memory bus. This option affects how frequently commands can be sent to the memory controller. In some cases, this setting may help improve system stability, especially when using high-speed RAM or when overclocking.
!!!!! NOT TESTED
#### AddrTweakEn = 0x1
#### ARdPtrInitValMP0 and ARdPtrInitValMP1 = try higher values
#### DFI MRL Margin = from lower to higher
#### CPU Vref Training Seed and Phy Vref Training Seed Control = tuning
!!!!! NOT TESTED
## DF Debug Options
#### OBFF = Enabled
This is a technology related to power management, designed to optimize the interaction between the processor and other components, such as a video card and chipset. It allows for more efficient use of power-saving states at the system level.
#### System probe filter = Enabled
This is a function that may be related to system diagnostics and monitoring, such as filtering signals or data coming from various sensors.

## NBIO Debug Options
#### UMA Steering = try 1 or 2
