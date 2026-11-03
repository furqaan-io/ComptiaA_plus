# Operating System (OS): Fundamentals, Architecture, Functions, and Usage

**Subject:** Operating Systems  
**Purpose:** Study notes covering the meaning, working, features, architecture, interfaces, bit types, files, and practical use of an operating system.

## Table of Contents

1. Introduction to Operating Systems
   - Meaning of an operating system
   - Why an OS is needed
   - How an OS works

2. Evolution and Types of Operating Systems
   - Early operating systems
   - Main types of OS
   - Desktop-oriented and server-oriented systems

3. Main Functions of an Operating System
   - Process management
   - Memory management
   - File management
   - Device management
   - Security and user management
   - Networking and error handling

4. Features of an Operating System

5. Operating System Architecture
   - Kernel and user space
   - Monolithic architecture
   - Microkernel architecture
   - Hybrid architecture
   - Layered architecture
   - System calls and interrupts

6. 32-bit and 64-bit Operating Systems
   - Meaning of bits
   - Differences between 32-bit and 64-bit
   - Compatibility and limitations

7. Command-Line Interface and Graphical User Interface
   - CLI
   - GUI
   - Differences and use cases

8. Operating System Programs, Processes, and Files
   - System software and application software
   - Kernel and system utilities
   - Executable files and processes
   - File systems and permissions

9. How an Operating System Starts and Runs Programs

10. Practical Use and Common Operating System Commands

11. Limitations and Common Problems

12. Quick Revision Table

13. Conclusion

---

## 1. Introduction to Operating Systems

### 1.1 Meaning of an operating system

An **Operating System (OS)** is system software that manages computer hardware and provides services for application programs and users.

It acts as an intermediary between applications, users, and the computer's hardware. It manages resources such as the CPU, RAM, storage, and connected devices.

Common examples include Microsoft Windows, Linux distributions, macOS, Android, and iOS.

For example, when a user opens a web browser, the operating system loads the program into memory, schedules CPU time for it, allows it to access files, and provides networking services so it can connect to the internet.

### 1.2 Why is an operating system needed?

A computer's hardware cannot conveniently manage all user activities on its own. Programs need a controlled way to use the CPU, memory, storage, and other devices.

Without an operating system, software would need to handle many hardware details itself. This would make general-purpose computing more complicated and difficult to manage.

The OS makes the computer easier to use by providing a consistent environment in which applications can run.

### 1.3 How an operating system works

A simplified view of a computer system is:

**User → Application → Operating System → Hardware**

For example, when saving a document:

1. The user clicks Save in an application.
2. The application requests that the file be saved.
3. The operating system checks the relevant file and access permissions.
4. The OS uses the file system and storage drivers to arrange the write operation.
5. The storage device records the data.
6. The application receives the result of the operation.

The application does not normally need to control the storage hardware directly. It uses services provided by the operating system.

This arrangement improves convenience, resource sharing, and security.

## 2. Evolution and Types of Operating Systems

### 2.1 Early development

Early computers often required operators to manage jobs manually. As computing developed, operating systems introduced facilities for loading programs, scheduling jobs, managing memory, and controlling input/output devices.

Later, interactive operating systems allowed users to work directly with computers. Graphical interfaces made computers easier for a wider range of people to use, while networked and server systems developed to support shared services and large numbers of users.

Modern operating systems support multitasking, networking, security controls, virtual memory, and a wide range of hardware.

### 2.2 Main types of operating systems

Operating systems can be classified by how they manage tasks or by the devices they are designed for. These categories can overlap.

**Batch operating systems**

Jobs are collected and processed in batches, with limited direct interaction while each job runs. They were useful for repetitive processing tasks.

**Time-sharing and multitasking operating systems**

The CPU switches between tasks so users and programs can make progress without one task having exclusive control of the computer. Modern desktop operating systems commonly support multitasking.

**Multi-user operating systems**

Allow multiple users to access system resources under separate accounts and permissions. Unix and Linux systems are common examples, although many operating systems support multiple user accounts.

**Real-time operating systems (RTOS)**

Designed for tasks with specific timing requirements. They aim to provide predictable responses within defined deadlines. They are used in industrial control, embedded devices, and some medical or automotive systems.

**Distributed operating systems**

A distributed system coordinates resources across multiple computers. The term *distributed operating system* has a more specific meaning than simply using several computers together; many modern distributed applications run on ordinary networked operating systems.

**Embedded operating systems**

Designed for dedicated devices such as routers, appliances, and industrial equipment. They may have limited memory, storage, and processing power.

**Mobile operating systems**

Designed for smartphones and tablets, with features for touchscreens, battery management, sensors, mobile networking, and application permissions.

### 2.3 Desktop-oriented and server-oriented operating systems

This is a useful way to classify operating systems by their intended workload, although the distinction is not absolute.

**Desktop-oriented operating systems**

Examples include Windows, macOS, and desktop Linux distributions.

They commonly focus on:
- Interactive use by a person.
- Running desktop applications.
- Supporting keyboards, mice, touchscreens, and displays.
- Providing user-friendly graphical interfaces.
- Managing everyday tasks such as browsing, office work, gaming, and media.

**Server-oriented operating systems**

Examples include Windows Server and Linux distributions configured for server workloads.

They commonly focus on:
- Hosting websites, databases, files, and network services.
- Handling requests from multiple clients.
- Providing remote administration.
- Supporting access controls, logging, and monitoring.
- Remaining available for long periods.

A server OS may run without a graphical desktop to reduce resource use and simplify administration. However, servers can also have graphical interfaces, and desktop operating systems can run server applications.

The difference is mainly the intended workload, available tools, configuration, and support—not a completely different definition of an OS.

## 3. Main Functions of an Operating System

### 3.1 Process management

A **program** is a set of instructions stored as a file or other executable form. A **process** is a running instance of a program, with its own execution state and allocated resources.

The OS manages processes by:
- Creating and terminating processes.
- Scheduling CPU time.
- Switching between running tasks.
- Managing process states.
- Coordinating communication between processes.
- Handling conflicts when processes share resources.

For example, a browser, music player, and text editor can all run at the same time because the operating system schedules their work.

A process may contain multiple threads, which are separate sequences of execution within that process. Threads in the same process typically share its memory and resources.

**Limitation:** CPU time is finite. Running too many demanding processes can make a computer slow, even when the operating system is functioning correctly.

### 3.2 Memory management

The OS manages RAM and determines how memory is allocated to running programs.

Its functions include:
- Allocating and releasing memory.
- Keeping processes' memory spaces separated.
- Tracking which memory is in use.
- Supporting virtual memory.
- Protecting memory from unauthorized access by other processes.

**Virtual memory** gives processes the appearance of having their own address spaces and allows the OS to use storage to support memory management. When RAM is under pressure, some data may be moved to storage.

Storage is much slower than RAM, so heavy paging can cause significant slowdowns.

**Limitation:** The OS cannot create unlimited physical memory. If applications require more memory than the system can efficiently provide, performance may deteriorate or programs may fail.

### 3.3 File management

The OS organizes information into files and directories and provides a way for applications to create, read, modify, rename, and delete files.

Its functions include:
- Organizing files and folders.
- Tracking file names and storage locations.
- Managing permissions.
- Supporting file systems.
- Coordinating access to files.
- Providing information such as file size and timestamps.

Common file systems include NTFS, FAT32, exFAT, ext4, and APFS.

A file system defines how files and directories are represented on a storage device. Different operating systems and devices may support different file systems.

**Limitation:** A file system may have restrictions on file size, volume size, or supported features. Corruption, hardware failure, or accidental deletion can also make data unavailable.

### 3.4 Device management

The OS coordinates hardware devices such as keyboards, displays, printers, network adapters, storage drives, and audio devices.

It uses device drivers and other system components to communicate with hardware.

A driver provides software instructions that allow the OS to operate a particular device or device family.

For example, when a user prints a document, the application passes the print request to the operating system's printing system, which communicates with the printer through the appropriate driver or supported interface.

**Limitation:** An unsupported, outdated, or faulty driver can prevent a device from working correctly. Some devices may not be supported by every operating system.

### 3.5 Security and user management

Operating systems help protect data and control access to resources.

Common security functions include:
- User accounts and authentication.
- File and directory permissions.
- Process and memory isolation.
- Privilege management.
- Security updates.
- Logging and auditing.
- Support for encryption and other protection mechanisms.

For example, an ordinary user account may be allowed to open documents but not install system-wide software or change important system settings.

**Limitation:** Security depends on correct configuration, updates, user behaviour, and the absence of exploitable vulnerabilities. An operating system cannot guarantee complete protection against every attack.

### 3.6 Networking

Modern operating systems include networking components that allow applications to communicate across local networks and the internet.

They support functions such as:
- Configuring network interfaces.
- Sending and receiving network data.
- Managing network connections.
- Supporting protocols such as TCP/IP.
- Applying network access controls.

For example, a browser uses operating-system networking services to communicate with a web server.

**Limitation:** Network performance and availability also depend on the network adapter, signal quality, router, service provider, remote server, and configuration.

### 3.7 User interface

The OS provides ways for users to interact with the computer.

The two common forms are:
- **CLI (Command-Line Interface):** Users enter text commands.
- **GUI (Graphical User Interface):** Users interact with windows, icons, menus, buttons, and pointers.

Some operating systems offer both. A user can manage files through a graphical file manager or use commands in a terminal.

### 3.8 Error handling and resource allocation

The OS detects and handles many errors, such as failed device operations, invalid memory access, and unavailable files. It also decides how resources are shared between processes.

For example, if two programs request CPU time, the scheduler determines when each one runs. If a process attempts an operation it is not permitted to perform, the OS can reject the request.

However, not every error can be recovered from automatically. A serious hardware fault, corrupted data, or operating-system bug can still cause a crash or loss of work.

## 4. Features of an Operating System

The functions described above explain what an OS does. Features are the capabilities it offers to users and applications.

### Common features

- **Multitasking:** Allows multiple tasks to make progress.
- **Multi-user support:** Supports separate users and permissions where provided.
- **Memory protection:** Helps prevent processes from interfering with one another's memory.
- **File-system support:** Organizes and manages files.
- **Device support:** Uses drivers and standard interfaces to operate hardware.
- **Networking:** Enables communication with other devices.
- **Security:** Provides authentication, permissions, and other protection mechanisms.
- **User interface:** Offers command-line, graphical, or other interaction methods.
- **Error reporting:** Reports many software and hardware problems.
- **Resource management:** Shares CPU time, RAM, storage, and device access.
- **Power management:** Helps control power consumption and sleep states on supported hardware.

Not every operating system offers all these features in the same way. A small embedded OS, for example, may provide only the functions required by its device.

## 5. Operating System Architecture

Operating system architecture describes how the internal parts of an OS are organized and how they communicate.

### 5.1 Kernel and user space

The **kernel** is the central part of the operating system. It manages critical resources and provides controlled access to hardware.

Its responsibilities commonly include:
- CPU scheduling.
- Memory management.
- Interrupt handling.
- Process and thread management.
- Core device and file-system services.

**User space** is where ordinary applications and many system utilities run. These programs normally cannot execute privileged hardware operations directly. They request services from the kernel through defined interfaces.

This separation helps protect the system. If an ordinary application crashes, it does not necessarily bring down the whole OS.

### 5.2 System calls

A **system call** is a controlled mechanism through which a program requests a service from the operating system kernel.

Examples of services requested through system calls include:
- Opening or reading a file.
- Creating a process.
- Allocating memory.
- Communicating through a network socket.
- Accessing certain devices.

The application does not need to know every hardware detail. It uses the OS interface, and the kernel checks and performs the requested operation where permitted.

### 5.3 Interrupts and exceptions

An **interrupt** signals that the CPU needs to respond to an event, such as a device completing an operation. An **exception** occurs as a result of an event during instruction execution, such as an invalid operation or a memory-access fault.

The processor and OS use these mechanisms to respond to events and handle errors. They are essential for efficient multitasking and hardware interaction.

### 5.4 Monolithic architecture

In a monolithic kernel, many core OS services, such as device drivers, file systems, and networking components, run within kernel space.

**Advantages**
- Efficient communication between components.
- Often good performance.
- Many services can interact directly within the kernel.

**Limitations**
- A serious bug in a kernel component can affect the whole system.
- A large kernel can be difficult to maintain and debug.

Linux is commonly described as using a monolithic kernel with modular capabilities.

### 5.5 Microkernel architecture

A microkernel keeps the kernel relatively small and moves many services, such as drivers or file-system services, into separate processes or servers.

**Advantages**
- Better separation between components.
- Some service failures may be contained.
- The design can improve modularity.

**Limitations**
- Communication between separate components can introduce overhead.
- Designing the interfaces and coordination can be complex.

Not every microkernel-based system has the same performance or reliability characteristics; implementation matters.

### 5.6 Hybrid architecture

A hybrid design combines ideas from monolithic and microkernel approaches. Some services remain in kernel space for performance, while the design may use modular boundaries and other separation mechanisms.

Windows NT-family systems and macOS are commonly described as using hybrid kernel designs, although their internal implementations differ.

### 5.7 Layered architecture

In a layered design, the OS is organized into levels, with each level relying on services from lower levels and providing services to higher ones.

This can make the system easier to understand, design, and maintain.

However, real operating systems do not always follow a strict layered structure. Some components communicate across layers or use specialized paths for performance.

## 6. 32-bit and 64-bit Operating Systems

The terms 32-bit and 64-bit describe aspects of a processor architecture and the software built for it. They are commonly used to describe an operating system's architecture.

### 6.1 What does a bit mean?

A bit is a binary digit that can hold either 0 or 1.

A processor's architecture determines many things, including its instruction set, register sizes, and addressing capabilities. The 32-bit and 64-bit labels are useful summaries, but they do not describe every detail of a processor.

### 6.2 32-bit operating system

A 32-bit OS is designed for a 32-bit processor architecture.

In a simplified address calculation, 32 address bits can represent \(2^{32}\) distinct addresses. If each address identifies one byte, that is 4 GiB of address space.

This is why conventional 32-bit systems have a 4 GiB virtual address-space limit per 32-bit address space. The amount available to an individual application or to the OS can be lower because of system design, memory mapping, and hardware reservations.

Some 32-bit systems support techniques such as Physical Address Extension (PAE) to access more physical memory, but this does not remove the normal per-process virtual address-space constraints.

### 6.3 64-bit operating system

A 64-bit OS runs on a supported 64-bit processor architecture.

Advantages commonly include:
- Access to much larger memory spaces.
- Support for modern applications and workloads.
- More and wider general-purpose registers in many 64-bit architectures.
- Improved performance for certain types of software.

A 64-bit OS does not automatically make every program faster. Performance depends on the CPU, software, memory use, and workload.

Although a 64-bit address is 64 bits wide, real processors generally implement fewer than 64 bits of usable virtual address space. Therefore, it is incorrect to assume that every 64-bit computer can use \(2^{64}\) bytes of RAM.

### 6.4 Main differences

| Feature | 32-bit OS | 64-bit OS |
|---|---|---|
| Processor support | Requires a compatible 32-bit architecture | Requires a compatible 64-bit architecture |
| Address space | More limited | Much larger potential address space |
| RAM support | Conventional address-space limits apply | Can support much larger memory, subject to platform limits |
| Applications | Runs compatible 32-bit software | Runs 64-bit software and often compatible 32-bit software |
| Performance | Can be suitable for older or limited systems | Often better for modern memory-intensive workloads |
| Compatibility | May not support modern 64-bit-only software | Compatibility with older 32-bit applications depends on the OS |

### 6.5 Compatibility and limitations

A 64-bit operating system generally requires a processor that supports its 64-bit architecture.

Many 64-bit operating systems can run compatible 32-bit applications, but this is not universal. Some modern systems have dropped 32-bit application support.

A 32-bit operating system cannot run a normal 64-bit application directly. Compatibility layers or emulators may help in some situations, but they do not make every program compatible.

Also, CPU architecture and operating-system bitness are not exactly the same thing: a 64-bit CPU can sometimes run a 32-bit OS, depending on the platform.

## 7. Command-Line Interface and Graphical User Interface

A user interface is the method through which a person interacts with an operating system or application.

### 7.1 Command-Line Interface (CLI)

A CLI allows users to interact with the system by entering commands as text.

Examples include:
- Command Prompt and PowerShell on Windows.
- Bash and other shells on Linux and Unix-like systems.

**Common uses**
- Managing files and directories.
- Installing or updating software.
- Checking system information.
- Managing services and users.
- Automating repeated tasks through scripts.
- Administering remote computers.

**Advantages**
- Efficient for repetitive or automated work.
- Often uses fewer graphical resources.
- Useful for remote administration.
- Provides access to many advanced system tools.

**Limitations**
- Users need to learn the commands and their syntax.
- Incorrect commands can delete or change important data.
- Some tasks are less convenient without visual feedback.

A shell is the program that interprets commands. The terminal is the interface through which the user interacts with the shell. These terms are related but not identical.

### 7.2 Graphical User Interface (GUI)

A GUI allows users to interact through visual elements such as windows, icons, menus, buttons, and pointers.

Examples include the Windows desktop, the macOS desktop, and graphical Linux desktop environments.

**Common uses**
- Opening and organizing files.
- Running applications.
- Changing system settings.
- Managing printers and displays.
- Working with images, documents, and other visual content.

**Advantages**
- Easier for many beginners to learn.
- Provides visual feedback.
- Makes common tasks discoverable.
- Useful for applications that rely on visual content.

**Limitations**
- May consume more memory and processing resources.
- Some advanced tasks are slower when repeated manually.
- Graphical tools may not expose every available setting.

### 7.3 CLI versus GUI

| Feature | CLI | GUI |
|---|---|---|
| Interaction | Text commands | Visual controls |
| Learning | Requires command knowledge | Often easier for beginners |
| Automation | Strong scripting support | Depends on available tools |
| Resource use | Often relatively low | Often higher |
| Remote management | Common through shells and remote tools | Possible, but may need more bandwidth |
| Error risk | Incorrect commands can have wide effects | Incorrect clicks can also cause problems |
| Best suited for | Administration, scripting, repetitive tasks | Everyday interactive work and visual tasks |

CLI and GUI are not separate types of operating systems. Many operating systems support both interfaces.

## 8. Operating System Programs, Processes, and Files

The terms *program*, *process*, *system file*, and *application* are related, but they do not mean the same thing.

### 8.1 System software and application software

**System software** helps operate and maintain the computer. It includes the operating system, drivers, system utilities, and other supporting components.

**Application software** helps users perform tasks, such as writing documents, browsing websites, editing videos, or managing spreadsheets.

Examples:
- Operating system: Windows or Linux.
- System utility: A disk-management or backup tool.
- Application: A web browser or text editor.

Some utilities are bundled with the OS, while others are installed separately.

### 8.2 Kernel and system utilities

The kernel manages core system resources. System utilities provide tools for tasks such as file management, monitoring, configuration, and maintenance.

Examples include task managers, terminal programs, disk utilities, and system configuration tools.

Not every system utility runs inside the kernel. Most ordinary utilities run in user space and request services from the OS.

### 8.3 Programs and processes

A **program** is a set of instructions, commonly stored in an executable file or other package.

A **process** is a running instance of a program. It has an execution state and resources managed by the OS.

A single program can have multiple processes running at the same time. One process can also contain multiple threads.

For example, opening a browser starts one or more processes. Closing a browser window does not necessarily terminate every process associated with it.

### 8.4 Operating system files

An OS uses many files to start, configure, and operate the system.

These may include:
- Kernel and boot-related files.
- Device drivers.
- System libraries.
- Configuration files.
- Logs.
- System utilities.
- Application files.

The exact file locations and formats differ by operating system. Windows commonly uses directories such as `C:\Windows`, while Linux systems use directories such as `/etc`, `/usr`, and `/var` for different purposes.

Users should not delete or modify system files without understanding their role. Doing so can cause applications or the operating system to malfunction.

### 8.5 File systems and permissions

A file system determines how files and directories are organized on a storage device. It keeps track of names, metadata, and where file data is stored.

Permissions determine who can read, modify, execute, or otherwise access particular files and directories.

For example, a Linux file may allow its owner to modify it while other users have read-only access. Windows uses access-control permissions to manage access to files and folders.

Permissions help protect data, but they must be configured correctly. Administrators and privileged services may have broader access than ordinary users.

## 9. How an Operating System Starts and Runs Programs

### 9.1 Booting the computer

When the computer is powered on, a sequence of events takes place.

1. The CPU begins executing firmware instructions.
2. The firmware initializes essential hardware and performs startup checks.
3. The firmware locates a suitable bootloader or operating-system boot entry.
4. The boot process loads the OS kernel and the required startup components.
5. The kernel initializes memory management, drivers, and other core services.
6. The system starts the services and user interface needed for operation.

The exact sequence depends on the hardware, firmware, and operating system. Some systems use UEFI, while older systems may use traditional BIOS.

### 9.2 Running an application

When a user opens an application:

1. The OS locates the executable or application package.
2. It creates a process and prepares the required memory.
3. Required program code and data are mapped into the process's address space.
4. The OS schedules the process so its threads can run on the CPU.
5. The application requests services such as file access, networking, or display output.
6. The OS coordinates access to the relevant resources.

This is why an application depends on more than its executable file. It may also require libraries, configuration files, permissions, drivers, and other services.

### 9.3 Shutting down

During a normal shutdown, the OS asks applications and services to finish, closes resources, and flushes pending data to storage where possible. It then coordinates the final shutdown or restart process.

Forcing power off can interrupt these operations and may result in lost unsaved work or file-system problems.

## 10. Practical Use and Common Operating System Commands

Commands differ between operating systems and shells. The following examples are common starting points.

| Task | Windows Command Prompt | Linux shell |
|---|---|---|
| Show current directory | `cd` | `pwd` |
| List files | `dir` | `ls` |
| Change directory | `cd foldername` | `cd foldername` |
| Create a directory | `mkdir foldername` | `mkdir foldername` |
| Display network configuration | `ipconfig` | `ip addr` |
| Test network reachability | `ping hostname` | `ping hostname` |
| Display running processes | `tasklist` | `ps` or `top` |

Commands may behave differently depending on the shell, installed tools, and user permissions. Some commands require administrator or root privileges.

Before running a command, check what it does, especially if it modifies files, partitions, permissions, or system settings.

## 11. Limitations and Common Problems

Operating systems make computers easier to use, but they have limitations.

**Resource limitations:** The OS cannot provide more physical CPU capacity, RAM, or storage than the hardware and platform support.

**Compatibility issues:** An application or driver may not support the current operating system or hardware.

**Security vulnerabilities:** Bugs, outdated software, weak passwords, and incorrect permissions can expose a system to attacks.

**Performance overhead:** The OS itself consumes CPU time, RAM, and storage. Background services can affect performance, especially on limited hardware.

**System failures:** Software bugs, driver problems, damaged files, or hardware faults can cause crashes or prevent startup.

**Maintenance requirements:** Updates, backups, security settings, and storage management are necessary to keep systems reliable.

**Limited recovery:** The OS cannot always recover unsaved work, repair every corrupted file, or protect data from every hardware failure.

Many problems can be reduced through regular updates, appropriate permissions, backups, compatible drivers, and sensible system configuration.

## 13. Conclusion

An operating system is the main system software that makes a computer practical to use. It manages the CPU, RAM, storage, processes, files, devices, and user access while providing services that applications depend on.

Different operating systems are designed for different needs. A desktop OS focuses heavily on interactive use, while a server OS commonly emphasizes hosting services and remote administration. CLI and GUI are different ways of interacting with a system, while 32-bit and 64-bit describe aspects of processor and software architecture.

Understanding the OS kernel, system calls, memory management, file systems, and process management makes it easier to understand what happens behind the scenes whenever a program runs or a file is saved.