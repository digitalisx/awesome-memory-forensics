# Awesome Memory Forensics [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome Memory Forensics for DFIR.

## Fundamental
- Operating Systems
- Computer Structure
- Reverse Engineering
- Malware Analysis
- Windows Internals
- Digital Forensics
- Incident Response

## Tools

### Memory Acquisition
Introduce commercial and open source tools for memory acquisition.

* [**Magnet RAM Capture**](https://www.magnetforensics.com/free-tool-magnet-ram-capture/) - Free imaging tool designed to capture the physical memory of a suspect’s computer. Supports recent versions of Windows.
* [**Belkasoft Live RAM Capturer**](http://belkasoft.com/ram-capturer) - Tiny free forensic tool to reliably extract the entire content of the computer’s volatile memory – even if protected by an active anti-debugging or anti-dumping system.
* [**Surge**](https://www.volexity.com/products-overview/surge/) - Volexity’s Surge Collect offers flexible storage options and an intuitive interface that any responder can run to eliminate the issues associated with the corrupt data samples, crashed target computers, and ultimately, unusable data that commonly results from using other tools.
* [**AVML**](https://github.com/microsoft/avml) - A portable volatile memory acquisition tool for Linux.
* [**LiME**](https://github.com/504ensicsLabs/LiME) - Loadable Kernel Module (LKM), which allows the acquisition of volatile memory from Linux and Linux-based devices, formerly called DMD.
* [**Linux Memory Grabber**](https://github.com/halpomeranz/lmg/) - Script for dumping Linux memory and creating Volatility profiles.
* [**OSForensics**](http://www.osforensics.com/) - Tool to acquire live memory on 32-bit and 64-bit systems. A dump of an individual process’s memory space or physical memory dump can be done.
- MDD
- FTK Imager
- Winpmem
- fmem

### Memory Analysis
Introduce commercial and open source tools for memory analysis.
- [**Volcano**](https://www.volexity.com/products-overview/volcano) - A comprehensive, cross-platform, next- generation memory analysis solution, Volexity Volcano Professional’s powerful core extracts, indexes, and correlates artifacts to provide unprecedented visibility into systems’ runtime state and trustworthiness.
- [**Volatility3**](https://github.com/volatilityfoundation/volatility3) - Volatility is the world's most widely used framework for extracting digital artifacts from volatile memory (RAM) samples.
- [**WinDbg**](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugger-download-tools) - The Windows Debugger (WinDbg) can be used to debug kernel-mode and user-mode code, analyze crash dumps, and examine the CPU registers while the code executes.
- [**Volatility**](https://github.com/volatilityfoundation/volatility) - The Volatility Framework is a completely open collection of tools,
implemented in Python under the GNU General Public License, for the
extraction of digital artifacts from volatile memory (RAM) samples. (***Deprecated***)
- [**Volafox**](https://github.com/n0fate/volafox) - Mac OS X Memory Analysis Toolkit' is developed on Python 2.x (***Deprecated***)
- [**Rekall**](https://github.com/google/rekall) - A new branch within the Volatility project was created to explore how to make the code base more modular, improve performance, and increase usability. (***Deprecated***)
- [**Redline**](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugger-download-tools) - The Windows Debugger (WinDbg) can be used to debug kernel-mode and user-mode code, analyze crash dumps, and examine the CPU registers while the code executes. (***Deprecated***)


## Books
- [**The Art of Memory Forensics**]()

## Course
- [**Malware and Memory Forensics Training**](https://www.memoryanalysis.net/memory-forensics-training)

## Videos

### 13 Cubed
- Introduction to Memory Forensics
- Windows Memory Analysis
- Windows Process Genealogy
- Memory Forensics Baselines
- Extracting Prefetch from Memory
- Detecting Persistence in Memory
- Introduction to Redline
- Profiling Network Activity with Volatility 3 - GeoIP from Memory
- Volatility Profiles and Windows 10
- Dumping Processes with Volatility 3
- First Look at Volatility 3 Public Beta
- Volatility 3 and WSL 2 - Linux DFIR Tools in Windows?

### DFIR Science
- Forensic Memory Acquisition in Linux - LiME
- 

## Articles


### Blogs

### WriteUps

## Papers
### DFRWS EU 2022
- Extraction and analysis of retrievable memory artifacts from Windows Telegram Desktop application
- Defining Atomicity (and Integrity) for Snapshots of Storage in Forensic Computing
- Memory forensic analysis of a programmable logic controller in industrial control systems
### DFRWS USA 2021
- Duck Hunt: Memory Forensics of USB Attack Platforms
- Seance: Divination of Tool-Breaking Changes in Forensically Important Binaries
- Leveraging Intel DCI for Memory Forensics


## Test Dataset

## Challenge
- Volatility Plugin Contest
- Volatility Analysis Contest

## Contribution
