# Operating System Installation: Complete Study Notes

## Table of Contents

1. Introduction to Operating System Installation
   1.1 Meaning of Operating System Installation  
   1.2 What an ISO File Is  
   1.3 What a Bootable USB Is  
   1.4 Understanding Disk Partitions  

2. Preparing for Installation
   2.1 Checking System Requirements  
   2.2 Backing Up Important Data  
   2.3 Downloading the Operating System  
   2.4 Creating a Bootable USB Using Rufus  
   2.5 Choosing the Correct Installation Settings  

3. Booting from the USB Drive
   3.1 Connecting the USB Drive  
   3.2 Opening the Boot Menu  
   3.3 Selecting the USB Drive  
   3.4 BIOS and UEFI Firmware  
   3.5 What Happens When the Computer Boots from USB  

4. Starting the Installation Process
   4.1 Loading the Installer  
   4.2 Selecting Language and Regional Settings  
   4.3 Choosing the Installation Type  
   4.4 Understanding the License and Product Key  

5. Disk Selection and Partitioning
   5.1 What a Disk Partition Is  
   5.2 Selecting an Installation Drive  
   5.3 Creating, Deleting, and Formatting Partitions  
   5.4 Understanding GPT and MBR  
   5.5 Risks of Changing Disk Partitions  

6. Installing the Operating System
   6.1 Copying Installation Files  
   6.2 Installing System Components  
   6.3 Restarting the Computer  
   6.4 Completing the Initial Setup  

7. Types of Operating System Installation
   7.1 Clean Installation  
   7.2 Upgrade Installation  
   7.3 Dual-Boot Installation  
   7.4 Installing on a Separate Drive  
   7.5 Choosing the Appropriate Installation Type  

8. Configuration After Installation
   8.1 Creating a User Account  
   8.2 Configuring Network Settings  
   8.3 Installing Device Drivers  
   8.4 Installing System Updates  
   8.5 Installing Applications and Security Software  

9. Troubleshooting Common Installation Problems
   9.1 USB Drive Not Appearing in the Boot Menu  
   9.2 Operating System Installation Not Starting  
   9.3 Disk or Partition Errors  
   9.4 Missing Drivers or Network Connectivity  
   9.5 Activation and Compatibility Problems  

10. Important Safety Measures and Limitations
    10.1 Protecting Personal Data  
    10.2 Avoiding Installation Errors  
    10.3 Hardware and Firmware Compatibility  
    10.4 Understanding Installation Risks  

11. Conclusion
    11.1 Summary of the Installation Process  
    11.2 The Importance of Correct Installation  

---

## 1. Introduction to Operating System Installation

### 1.1 Meaning of Operating System Installation

An operating system (OS) is system software that manages a computer’s hardware and provides the environment in which applications run. Examples include Microsoft Windows, Linux distributions such as Ubuntu, and macOS.

Operating system installation is the process of placing the operating system’s required files on a computer’s storage device and configuring them so that the computer can start and operate using that system.

Installation may be necessary when setting up a new computer, replacing an existing operating system, repairing a damaged installation, or installing another operating system alongside the current one.

### 1.2 What an ISO File Is

An ISO file is a disc-image file that contains the structure and contents of installation media. Operating system ISO files commonly include the installer, system files, and other resources needed to install the OS.

An ISO file is not necessarily the installed operating system itself. It is an installation image from which suitable bootable media can be created.

For example, a user may download a Windows or Ubuntu ISO file and use a utility such as Rufus to prepare a USB drive for installation.

### 1.3 What a Bootable USB Is

A bootable USB is a USB storage device prepared so that a computer can start from it. It contains the necessary boot files and installation resources for an operating system.

A normal USB drive used to store documents is not automatically bootable. It must be prepared using an appropriate tool and a compatible operating system image.

Bootable USB drives are useful because they allow users to install or repair an operating system without relying on an existing installation or an optical disc.

### 1.4 Understanding Disk Partitions

A disk partition is a defined section of a storage device that the operating system treats as a separate logical storage area.

A computer may have separate partitions for the operating system, personal files, recovery tools, or other purposes. Some operating systems also create small system partitions required for booting.

During installation, the user may select an existing partition, create a new one, or format a partition. These operations can affect existing files, so it is essential to understand which disk and partition are being changed.

## 2. Preparing for Installation

### 2.1 Checking System Requirements

Before installing an operating system, check whether the computer meets its hardware requirements. These may include:

- Processor type and supported architecture.
- Minimum RAM capacity.
- Available storage space.
- Graphics and display compatibility.
- Required firmware features, such as Secure Boot or TPM support, when applicable.
- Network access and other device requirements.

Requirements vary by operating system and version. A computer that can run one version may not officially support another.

### 2.2 Backing Up Important Data

Back up important documents, photographs, downloads, application files, and other personal data before beginning installation.

A clean installation, partition deletion, or disk-formatting operation may erase data from the selected storage area. If the wrong partition or disk is selected, information on that device may be lost.

A backup should ideally be stored on a separate drive or a trusted cloud service rather than only on the disk being modified. If encryption or recovery keys are used, make sure they are available before making major system changes.

### 2.3 Downloading the Operating System

Obtain the operating system image from its official source or another trusted provider. Verify that the image is intended for the computer’s hardware architecture and the required edition or distribution.

For example, Windows installation media and Ubuntu installation media have different installers and requirements. A file intended for one architecture or operating system version may not work correctly on another system.

Downloading from trusted sources also reduces the risk of obtaining modified or malicious installation files.

### 2.4 Creating a Bootable USB Using Rufus

Rufus is a utility commonly used on Windows to create bootable USB drives from ISO images.

The general process is:

1. Connect a USB drive with sufficient capacity.
2. Open Rufus.
3. Select the correct USB device.
4. Choose the operating system ISO file.
5. Select the appropriate partition scheme and target-system options.
6. Start the process and follow any prompts.
7. Wait until Rufus finishes preparing the USB drive.

**Warning:** Creating bootable media usually erases the USB drive’s existing contents. Check the selected device carefully before starting.

The correct settings depend on the ISO image and the computer’s firmware. GPT is commonly used with UEFI systems, while MBR is associated with many legacy BIOS configurations, but the appropriate choice depends on the specific system and installer.

### 2.5 Choosing the Correct Installation Settings

Before creating the USB, determine whether the target computer uses UEFI or legacy BIOS booting and check the operating system’s requirements.

Rufus may offer different partition schemes, file systems, and other options. These settings influence whether the computer can boot from the prepared USB drive.

Do not assume that one configuration works for every computer. Use settings compatible with the target computer and the selected operating system image.

## 3. Booting from the USB Drive

### 3.1 Connecting the USB Drive

Once the bootable USB is ready, connect it to the computer on which the operating system will be installed.

If possible, connect it directly to a USB port on the computer rather than through an unreliable hub. If the computer fails to recognize the drive, trying another port may help.

Connecting the USB does not, by itself, install the operating system or change the internal drive.

### 3.2 Opening the Boot Menu

The boot menu allows the user to choose which device the computer should start from.

Restart or power on the computer and press the appropriate boot-menu key when prompted. Depending on the manufacturer and model, this may be a key such as F12, F11, Esc, or another key.

The boot-menu key is not universal. Check the computer manufacturer’s instructions if the menu does not appear.

### 3.3 Selecting the USB Drive

When the boot menu appears, select the USB drive containing the installation media. A UEFI system may show an entry explicitly labelled with the UEFI version of the USB device.

If the computer starts its existing operating system instead, the USB may not have been selected, may not be bootable, or may not be compatible with the current firmware settings.

Selecting the USB starts the installation environment; it does not automatically erase the computer’s existing operating system.

### 3.4 BIOS and UEFI Firmware

BIOS and UEFI are firmware interfaces responsible for initializing hardware and starting the boot process.

- **BIOS:** The traditional firmware interface used on many older computers.
- **UEFI:** The modern firmware interface used on most current computers. It supports features such as Secure Boot and is commonly used with GPT-partitioned disks.

The boot mode matters because the installation media and disk layout must be compatible with the system’s configuration. Changing firmware settings without understanding their purpose can make an existing operating system temporarily unbootable.

### 3.5 What Happens When the Computer Boots from USB

When the computer boots from the USB drive, the firmware loads the boot files from that device and starts the operating system’s installation environment.

The installer then provides options for configuring the installation and selecting the destination storage device.

At this point, the computer is running the installation environment from the USB. The existing operating system on the internal drive normally remains unchanged until the user performs operations that modify it.

## 4. Starting the Installation Process

### 4.1 Loading the Installer

After the computer successfully boots from the USB, the installation program loads. The installer provides the interface used to configure and install the operating system.

Depending on the OS, it may offer options to install the system, repair an existing installation, test a live environment, or access recovery tools.

The available choices differ between Windows, Linux distributions, and other operating systems.

### 4.2 Selecting Language and Regional Settings

The installer may ask the user to select a language, region, keyboard layout, time zone, or preferred date and time format.

These settings affect how text is displayed and how the system handles keyboard input, dates, times, and regional conventions. Some can be changed later through the operating system’s settings.

### 4.3 Choosing the Installation Type

Some installers offer different installation paths, such as a standard installation, a custom installation, or an upgrade.

A standard or guided installation may automate several decisions. A custom installation generally gives the user more control over the destination disk and partitions.

Read the descriptions carefully. Options that appear similar may have different effects on existing applications, system files, and personal data.

### 4.4 Understanding the License and Product Key

Some operating systems require users to accept a license agreement before installation can continue.

For Windows, the installer may request a product key or provide an option to enter it later, depending on the edition and installation method. Activation requirements depend on the Windows edition and the computer’s digital licence or product key.

Linux distributions such as Ubuntu generally do not require a Windows-style product key. Their licensing and installation processes differ.

## 5. Disk Selection and Partitioning

### 5.1 What a Disk Partition Is

Partitioning divides a physical storage device into separate logical sections. The operating system uses these sections to organize system files, applications, personal data, and other required information.

For example, a computer may have one partition containing Windows and another partition containing personal files. However, having separate partitions does not automatically protect data if the entire physical drive fails or is erased.

### 5.2 Selecting an Installation Drive

The installer usually displays available storage devices and their partitions. Identify the intended drive using its capacity, partition layout, and other available details.

Do not select a disk merely because it appears first in the list. A computer may contain multiple internal drives, external storage devices, or recovery partitions.

If the computer has more than one drive, disconnecting unnecessary external storage before installation can reduce the risk of selecting the wrong device.

### 5.3 Creating, Deleting, and Formatting Partitions

The installer may allow the user to create, delete, resize, or format partitions.

- **Create:** Allocates a new partition in available space.
- **Delete:** Removes a partition entry and makes its space available for other uses. Its existing data becomes inaccessible through the normal partition structure.
- **Format:** Prepares a partition with a file system so that it can store files. Formatting may destroy access to existing data.
- **Resize:** Changes a partition’s size, if supported by the file system and installer.

The exact consequences depend on the operation and the installer. Formatting or deleting a partition can result in data loss, so confirm the target before proceeding.

### 5.4 Understanding GPT and MBR

GPT and MBR are partition-table formats that describe how a storage device is divided into partitions.

**GPT (GUID Partition Table)** is the modern format commonly used with UEFI systems. It supports large disks and more flexible partition layouts.

**MBR (Master Boot Record)** is an older format associated with legacy BIOS booting. It has limitations, including a typical maximum disk size of about 2 TiB when using 512-byte logical sectors and a limit of four primary partition entries.

The correct format depends on the operating system, firmware, and installation configuration. Converting between GPT and MBR can affect the existing partition layout, so it should not be done without understanding the consequences.

### 5.5 Risks of Changing Disk Partitions

Partition changes can cause data loss or prevent an existing operating system from starting if performed incorrectly.

Before making changes, verify the disk identity, confirm that a usable backup exists, and check whether any partition contains important data or recovery tools.

If the goal is to keep the current operating system, avoid deleting or formatting its partitions unless the installation procedure specifically requires it and the consequences are understood.

## 6. Installing the Operating System

### 6.1 Copying Installation Files

After the destination is selected and the user confirms the installation, the installer copies the required files to the selected storage device.

It may extract compressed files, prepare system directories, and create the initial operating system structure.

The time required depends on the operating system, the speed of the USB drive, the destination storage device, and the computer’s hardware.

### 6.2 Installing System Components

The installer configures the operating system’s core components and prepares the files required for normal operation.

It may also install boot files, configure system services, and set up the initial system environment. Some hardware drivers and optional components may be installed at this stage, while others may need to be installed or updated afterward.

### 6.3 Restarting the Computer

After the main installation stage, the computer usually restarts one or more times.

If the computer boots from the USB again, the installation may restart from the beginning. In that case, remove the USB when instructed or choose the internal drive from the boot menu.

Do not remove installation media while the installer is actively using it unless the instructions say it is safe to do so.

### 6.4 Completing the Initial Setup

After installation, the operating system may guide the user through the initial configuration.

Depending on the OS, this may include:

- Creating a user account.
- Setting a password or sign-in method.
- Choosing privacy and diagnostic settings.
- Connecting to a network.
- Selecting regional preferences.
- Configuring accessibility options.

Once these steps are complete, the system should start into the newly installed operating system.

## 7. Types of Operating System Installation

### 7.1 Clean Installation

A clean installation installs a fresh operating system rather than upgrading the existing installation in place.

It is often used when setting up a new computer, replacing a damaged system, or starting again with a clean software environment.

A clean installation does **not** always require erasing the entire physical disk. Its effect on existing data depends on which partition or disk the user selects and whether that area is formatted or deleted. Data on other partitions may remain intact, but it should still be backed up before installation.

### 7.2 Upgrade Installation

An upgrade installation replaces or updates an existing operating system while attempting to preserve supported applications, personal files, and settings.

Whether an upgrade is possible depends on factors such as the current operating system, target version, edition, architecture, available storage, and compatibility requirements.

An upgrade should not be treated as a substitute for backing up data. Some applications or settings may not be retained, and an unsuccessful upgrade can require recovery or reinstallation.

### 7.3 Dual-Boot Installation

A dual-boot setup allows two operating systems to be installed on the same computer. When the computer starts, a boot manager lets the user choose which operating system to load.

For example, a user might install Windows and a Linux distribution on separate partitions.

Dual boot requires sufficient storage and compatible partition and boot configurations. Installing or modifying boot files can affect an existing operating system, so the partition layout and installation instructions should be checked carefully.

### 7.4 Installing on a Separate Drive

Another option is to install the new operating system on a different physical drive.

For example, a computer might use one SSD for Windows and another SSD for Linux. This can make storage management easier and reduce the need to modify partitions on the original drive.

However, separate drives do not eliminate every risk. The installer may place boot files on a different drive from the one selected for the operating system, depending on the system and installation process. Confirm the target and boot configuration before proceeding.

### 7.5 Choosing the Appropriate Installation Type

The appropriate method depends on the user’s goal.

- Choose a **clean installation** when a fresh system is needed and the effect on the target partition’s data is understood.
- Choose an **upgrade installation** when the existing OS supports an upgrade and preserving compatible applications and settings is important.
- Choose a **dual-boot installation** when both operating systems need to remain available on the same computer.
- Choose a **separate-drive installation** when another physical storage device is available and keeping the installations on different drives is preferable.

The user should decide based on compatibility, available storage, backup status, and whether the existing operating system needs to be retained.

## 8. Configuration After Installation

### 8.1 Creating a User Account

A user account provides access to the operating system and determines which settings, files, and permissions are associated with that user.

During initial setup, the operating system may ask for a username, password, online account, or other sign-in details.

Use a strong password or another supported secure sign-in method. Avoid using an administrator account for routine tasks when the operating system supports separate standard-user accounts.

### 8.2 Configuring Network Settings

Connect the computer to a suitable network through Wi-Fi or Ethernet, if required.

Network access may be needed to download updates, obtain drivers, activate certain software, or install applications. Some operating systems can complete their initial installation without an internet connection, while others may require or strongly encourage connectivity for particular setup options.

If the network does not work, check the adapter, connection settings, and driver status.

### 8.3 Installing Device Drivers

A device driver allows the operating system to communicate correctly with a hardware component.

Drivers may be needed for Wi-Fi adapters, graphics cards, audio devices, chipsets, printers, and other peripherals. Some operating systems install suitable drivers automatically, while others may require additional packages from the device manufacturer or operating system’s official repositories.

Use drivers from trusted sources and make sure they match the hardware and operating system version.

### 8.4 Installing System Updates

After installation, check for operating system updates. Updates can provide security fixes, bug corrections, compatibility improvements, and other changes.

A freshly downloaded ISO may not include every update released since the image was created. Installing updates can therefore be an important part of preparing the system for regular use.

Restart the computer when required to complete an update.

### 8.5 Installing Applications and Security Software

Install the applications needed for work, study, communication, and other tasks.

Use official websites or trusted application stores and package repositories. Avoid installing unfamiliar software from unverified sources.

Keep the operating system’s built-in security protections enabled unless there is a clear, informed reason to change them. Additional security software should be compatible with the system and obtained from a trusted provider.

## 9. Troubleshooting Common Installation Problems

### 9.1 USB Drive Not Appearing in the Boot Menu

If the USB drive does not appear in the boot menu, check that it was created successfully and that the computer supports booting from it.

Possible causes include:

- The USB drive was not prepared correctly.
- The USB port or drive is faulty.
- The firmware does not recognize the selected boot mode.
- Secure Boot or another firmware setting affects whether the media can start.
- The ISO image is incompatible or damaged.

Try another USB port, recreate the installation media if necessary, and consult the computer manufacturer’s instructions before changing firmware settings.

### 9.2 Operating System Installation Not Starting

If the computer selects the USB but the installer does not load, the installation image may be incomplete, the media may be damaged, or the boot configuration may be incompatible.

Download the ISO again from the official source if corruption is suspected, and recreate the USB using settings appropriate for the target computer.

Also check the operating system’s hardware requirements. An incompatible processor architecture or unsupported hardware feature may prevent installation.

### 9.3 Disk or Partition Errors

Disk errors may occur when the installer cannot identify the storage device, cannot use the existing partition layout, or cannot create the required partitions.

Possible causes include incompatible partition-table settings, insufficient free space, storage-controller configuration, or a failing drive.

Before changing partitions or converting the disk format, confirm the intended installation method and back up important data. If the drive is not detected at all, check the manufacturer’s guidance for storage-controller or firmware compatibility.

### 9.4 Missing Drivers or Network Connectivity

If Wi-Fi, audio, graphics, or another component does not work after installation, the appropriate driver may be missing or may not support the device.

Check the operating system’s device-management tools and official driver sources. If internet access is unavailable, another device may be needed to download the correct driver and transfer it to the computer.

Avoid installing drivers that do not match the device model or operating system version.

### 9.5 Activation and Compatibility Problems

Some operating systems or editions require activation after installation. Activation may fail if the product key is invalid, the edition does not match the licence, or the device cannot complete the required online checks.

Check the licence information and use the operating system provider’s official activation guidance.

If installation is blocked by hardware requirements, verify the computer’s specifications and the target OS version. Do not assume that changing firmware settings or bypassing a requirement will make an unsupported system reliable or secure.

## 10. Important Safety Measures and Limitations

### 10.1 Protecting Personal Data

The most important precaution is to back up data before modifying storage partitions or replacing an operating system.

Double-check the selected disk and partition before confirming an installation or formatting operation. Keep recovery keys and any required account information available.

A bootable USB provides an installation environment, but it does not automatically protect files on the internal drive. Data safety depends on the operations performed during installation.

### 10.2 Avoiding Installation Errors

Use a trusted ISO image, prepare the USB correctly, and confirm that the installation settings match the target computer.

Do not interrupt an installation while files are being written or system components are being configured unless the system is clearly unresponsive and recovery steps are necessary.

Read prompts carefully, especially those concerning deletion, formatting, disk conversion, and replacing an existing operating system.

### 10.3 Hardware and Firmware Compatibility

Not every operating system supports every computer. Processor architecture, RAM, storage, graphics, firmware settings, and device drivers can affect whether an OS installs and operates properly.

A USB drive that boots successfully on one computer may not boot on another because the systems use different firmware settings or have different compatibility requirements.

Check the operating system’s official requirements and the computer manufacturer’s documentation before starting.

### 10.4 Understanding Installation Risks

Installation can make an existing operating system unavailable, remove applications, alter boot settings, or cause data loss if the wrong options are selected.

A clean installation may remove the contents of the target partition; deleting all partitions on a drive can remove the data and operating systems stored there. An upgrade usually aims to preserve supported files and settings, but preservation is not guaranteed.

Dual boot can also fail if the boot manager or partition layout is configured incorrectly. Keeping a backup and understanding the chosen installation method reduces these risks.

## 11. Conclusion

### 11.1 Summary of the Installation Process

Installing an operating system involves preparing suitable installation media, booting the computer from that media, configuring the installer, selecting a destination disk or partition, and allowing the system files to be installed.

After installation, the user completes initial setup, checks drivers and network connectivity, installs updates, and configures the system for regular use.

The exact steps differ between operating systems, but the underlying process is similar: prepare the media, start the installer, configure the destination, install the system, and complete the setup.

### 11.2 The Importance of Correct Installation

A correct installation helps the operating system start reliably, recognize the computer’s hardware, and provide a stable environment for applications.

Understanding ISO files, bootable USB drives, firmware, partitions, and installation types helps users make informed choices and avoid common mistakes. Most importantly, checking compatibility and backing up important data before beginning can prevent unnecessary disruption and data loss.