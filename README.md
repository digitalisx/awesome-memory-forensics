# Awesome Memory Forensics [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of awesome Memory Forensics for DFIR.

> [Memory Forensics](https://en.wikipedia.org/wiki/Memory_forensics) is forensic analysis of a computer's memory dump. Its primary application is investigation of advanced computer attacks which are stealthy enough to avoid leaving data on the computer's hard drive. Consequently, the memory (RAM) must be analyzed for forensic information.

If you want to contribute, please read the [contribution guidelines](CONTRIBUTING.md).

## Contents
- [Tool](#tool)
- [Books](#books)
- [Course](#course)
- [Videos](#videos)
- [Articles](#articles)
- [Papers](#papers)
- [Datasets](#datasets)
- [Challenges](#challenges)
- [Contributors](#contributors)


## Tool

### Memory Acquisition
Introduce commercial and open source tools for memory acquisition.

#### Software
- [Surge](https://www.volexity.com/products-overview/surge/) - Volexity's Surge Collect offers flexible storage options and an intuitive interface that any responder can run to eliminate the issues associated with the corrupt data samples, crashed target computers, and ultimately, unusable data that commonly results from using other tools.
- [MAGNET RAM](https://www.magnetforensics.com/resources/magnet-ram-capture/) - MAGNET RAM Capture is a free imaging tool designed to capture the physical memory of a suspect's computer, allowing investigators to recover and analyze valuable artifacts that are often only found in memory.
- [FTK Imager](https://www.exterro.com/digital-forensics-software/ftk-imager) - FTK® Imager is a data preview and imaging tool that lets you quickly assess electronic evidence to determine if further analysis with a forensic tool such as Forensic Toolkit (FTK®) is warranted. 
- [Winpmem](https://github.com/Velocidex/WinPmem) - WinPmem has been the default open source memory acquisition driver for windows for a long time.
- [Ram Capturer](https://belkasoft.com/ram-capturer) - Belkasoft Live RAM Capturer is a tiny free forensic tool that allows to reliably extract the entire contents of computer's volatile memory—even if protected by an active anti-debugging or anti-dumping system.
- [LiME](https://github.com/504ensicsLabs/LiME)(Not actively maintained 😵🍋‍🟩) - A Loadable Kernel Module (LKM) which allows for volatile memory acquisition from Linux and Linux-based devices, such as Android. 
- [AVML](https://github.com/microsoft/avml) - AVML is an X86_64 userland volatile memory acquisition tool written in Rust, intended to be deployed as a static binary. 
- [fmem](https://github.com/NateBrune/fmem) - This module creates /dev/fmem device, that can be used for dumping physical memory, without limits of /dev/mem (1MB/1GB, depending on distribution).
- [FEX Memory Imager](https://getdataforensics.com/product/fex-memory-imager/) - FEX Memory Imager (FEX Memory) is a free imaging tool designed to capture the physical Random Access Memory (RAM) of a suspect's running computer. This allows investigators to recover and analyze valuable artifacts found only in memory.
- [Digital Collector](https://cellebrite.com/en/digital-collector/) - A powerful forensic imaging software solution to perform triage, live data acquisition and targeted data collection for Windows and Mac computers. (Formerly BlackBag MacQuisition)
- [varc](https://github.com/cado-security/varc) - Volatile Artifact Collector gathers a snapshot of volatile data from a system.
- [MAGNET DumpIt for Windows](https://www.magnetforensics.com/resources/magnet-dumpit-for-windows/) - Free Windows physical memory acquisition tool (formerly Comae DumpIt) that produces Microsoft crash dump format images.
- [MAGNET DumpIt for Linux](https://github.com/MagnetForensics/dumpit-linux) - Linux memory acquisition tool written in Rust that creates compressed core dump style images readable by Volatility and MemProcFS.
- [LEMON](https://github.com/eurecom-s3/lemon) - eBPF-based memory acquisition tool for modern Android devices and hardened Linux systems, working without kernel modules, kernel sources or code signing where LiME/AVML are blocked.

#### Hardware
- [PCILeech](https://github.com/ufrisk/pcileech) - PCILeech uses PCIe hardware devices to read and write target system memory. This is achieved by using DMA over PCIe. No drivers are needed on the target system.

#### Misc
- [EVTXtract](https://github.com/williballenthin/EVTXtract) - EVTXtract recovers and reconstructs fragments of EVTX log files from raw binary data, including unallocated space and memory images.
- [Volatility3 Inodes Plugin](https://github.com/forensicxlab/volatility3_plugins/blob/main/inodes.py) - The plugin is a pushed verion of the lsof plugin extracting inode metadata information from each files.
- [Volatility3 Prefetch Plugin](https://github.com/forensicxlab/volatility3_plugins/blob/main/prefetch.py) - The plugin is scanning, extracting and parsing Windows Prefetch files from Windows XP to Windows 11.
- [volatility3-symbols](https://github.com/Abyss-W4tcher/volatility3-symbols) - Continuously updated collection of ready-to-use Volatility 3 symbol tables (ISF) for Linux and macOS kernels across many distributions.
- [btf2json](https://github.com/vobst/btf2json) - Generates Volatility 3 symbol tables from the kernel's BTF type information, without needing a debug kernel or dwarf2json. (1st place, 2024 Volatility Plugin Contest)
- [BPFVol3](https://github.com/vobst/BPFVol3) - Volatility 3 plugins to extract and analyze Linux eBPF programs, maps and links for detecting BPF-based malware. (1st place, 2023 Volatility Plugin Contest)
- [ETW Scan](https://github.com/JPCERTCC/etw-scan) - JPCERT/CC Volatility 3 plugin that recovers Event Tracing for Windows (ETW) events from memory images.
- [MemProcFS-Analyzer](https://github.com/evild3ad/MemProcFS-Analyzer) - PowerShell automation for MemProcFS that mounts a Windows memory dump and runs triage, IOC, YARA and timeline analysis.

### Memory Analysis
Introduce commercial and open source tools for memory analysis.
- [Volcano](https://www.volexity.com/products-overview/volcano) - A comprehensive, cross-platform, next- generation memory analysis solution, Volexity Volcano Professional's powerful core extracts, indexes, and correlates artifacts to provide unprecedented visibility into systems' runtime state and trustworthiness.
- [Volatility3](https://github.com/volatilityfoundation/volatility3) - Volatility is the world's most widely used framework for extracting digital artifacts from volatile memory (RAM) samples.
- [MemProcFS](https://github.com/ufrisk/MemProcFS) - The Memory Process File System (MemProcFS) is an easy and convenient way of viewing physical memory as files in a virtual file system.
- [WinDbg](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugger-download-tools) - The Windows Debugger (WinDbg) can be used to debug kernel-mode and user-mode code, analyze crash dumps, and examine the CPU registers while the code executes.
- [Volatility](https://github.com/volatilityfoundation/volatility) - The Volatility Framework is a completely open collection of tools,
implemented in Python under the GNU General Public License, for the
extraction of digital artifacts from volatile memory (RAM) samples. (***Deprecated*** in favor of Volatility3 since the 2025 parity release)
- [Volafox](https://github.com/n0fate/volafox) - macOS Memory Analysis Toolkit' is developed on Python 2.x (***Deprecated***)
- [Rekall](https://github.com/google/rekall) - A new branch within the Volatility project was created to explore how to make the code base more modular, improve performance, and increase usability. (***Deprecated***)
- [Redline](https://fireeye.market/apps/211364) - Redline®, FireEye's premier free endpoint security tool, provides host investigative capabilities to users to find signs of malicious activity through memory and file analysis and the development of a threat assessment profile.
- [Memoryze](https://web.archive.org/web/20220519011256/https://www.fireeye.com/services/freeware/memoryze.html) - Mandiant's Memoryze™ is free memory forensic software that helps incident responders find evil in live memory. Memoryze can acquire and/or analyze memory images and on live systems can include the paging file in its analysis. (***Deprecated***, archived page)
- [dwarf2json](https://github.com/volatilityfoundation/dwarf2json) - Go utility that processes files containing symbol and type information to generate Volatilty3 Intermediate Symbol File (ISF) JSON output suitable for Linux and macOS analysis.
- [VolWeb](https://github.com/k1nd0ne/VolWeb) - Collaborative web platform built on Volatility 3 for memory analysis, with case management, process tree visualization and evidence storage.
- [Orochi](https://github.com/LDO-CERT/orochi) - Django-based web GUI for Volatility 3 that lets multiple analysts work on the same memory dumps.
- [Volatility Workbench](https://www.osforensics.com/tools/volatility-workbench.html) - Free, open source Windows GUI for Volatility 3 from PassMark.
- [mquire](https://github.com/trailofbits/mquire) - Trail of Bits' Linux memory forensics tool that uses the kernel's embedded BTF and kallsyms, so no external debug symbols or profiles are required.
- [memflow](https://github.com/memflow/memflow) - Rust framework for physical memory introspection that reads from memory dumps, live VMs and DMA hardware through pluggable connectors.
- [Volatility MCP Server](https://github.com/bornpresident/Volatility-MCP-Server) - Model Context Protocol (MCP) server that exposes Volatility 3 plugins to LLM clients for AI-assisted memory analysis.

## Books
- [The Art of Memory Forensics](https://www.amazon.com/Art-Memory-Forensics-Detecting-Malware/dp/1118825098) - Detecting Malware and Threats in Windows, Linux, and Mac Memory.
- [Practical Memory Forensics](https://www.amazon.com/Practical-Memory-Forensics-Jumpstart-effective/dp/1801070334) - Jumpstart effective forensic analysis of volatile memory.


## Course
- [Malware and Memory Forensics Training](https://www.memoryanalysis.net/memory-forensics-training)
- [A Complete Practical Approach To Malware Analysis And Memory Forensics - 2022 Edition](https://www.blackhat.com/us-22/training/schedule/index.html#a-complete-practical-approach-to-malware-analysis-and-memory-forensics----edition-25509)
- [Malware and Memory Forensics Training on Volatility 3 (2024)](https://volatilityfoundation.org/in-person-malware-and-memory-forensics-training-on-volatility-3-october-2024/) - The first official in-person training focused solely on Volatility 3, taught by the core developers.
- [13Cubed Investigating Windows Memory](https://training.13cubed.com/investigating-windows-memory) - Self-paced Windows memory forensics course covering Volatility, MemProcFS and WinDbg.
- [SANS FOR508](https://www.sans.org/cyber-security-courses/advanced-incident-response-threat-hunting-training/) - Advanced Incident Response, Threat Hunting, and Digital Forensics, including a memory forensics section.

## Videos

### 13 Cubed
- [Introduction to Memory Forensics](https://www.youtube.com/watch?v=1PAGcPJFwbE)
- [Windows Memory Analysis](https://www.youtube.com/watch?v=gHbejxlPbRQ)
- [Windows Process Genealogy](https://www.youtube.com/watch?v=s98_p3bheL0)
- [Windows Process Genealogy (Update)](https://www.youtube.com/watch?v=vpSIw-zGhhE)
- [Memory Forensics Baselines](https://www.youtube.com/watch?v=1thWaC6uvI4)
- [Extracting Prefetch from Memory](https://www.youtube.com/watch?v=6y9Wxch7NKk)
- [Detecting Persistence in Memory](https://www.youtube.com/watch?v=shF8hAprD4g)
- [Introduction to Redline](https://www.youtube.com/watch?v=tCIEYCWTdk4)
- [Introduction to Redline (Update)](https://www.youtube.com/watch?v=Oiac0t0RllM)
- [Profiling Network Activity with Volatility 3 - GeoIP from Memory](https://www.youtube.com/watch?v=egv63oso8Qc)
- [Volatility Profiles and Windows 10](https://www.youtube.com/watch?v=Us1gbPqtdtY)
- [Dumping Processes with Volatility 3](https://www.youtube.com/watch?v=v9oFztyRkbA)
- [First Look at Volatility 3 Public Beta](https://www.youtube.com/watch?v=ozeedYjv5Lw)
- [Volatility 3 and WSL 2 - Linux DFIR Tools in Windows?](https://www.youtube.com/watch?v=rwTWZ7Q5i_w)
- [MemProcFS - This Changes Everything](https://www.youtube.com/watch?v=hjWVUrf7Obk)
- [Hyper-V Memory Forensics - MemProcFS to the Rescue!](https://www.youtube.com/watch?v=Wbk6ayF_zaQ)
- [Linux Memory Forensics Challenge](https://www.youtube.com/watch?v=IHd85h6T57E)
- [A New(ish) Way to Detect Process Hollowing](https://www.youtube.com/watch?v=x5mGPAG41I4)
- [Windows Memory Forensics Challenge](https://www.youtube.com/watch?v=6JN6iAenEoA)
- [The Easy Way to Analyze Linux Memory](https://www.youtube.com/watch?v=W40gdWNdwUI)
- [Automate Volatility 3 Memory Analysis with This Tool](https://www.youtube.com/watch?v=0GMTydimOP4)

### DFIR Science
- [Introduction to Memory Forensics with Volatility 3](https://www.youtube.com/watch?v=Uk3DEgY5Ue8)
- [Amazon AWS EC2 Forensic Memory Acquisition - LiME](https://www.youtube.com/watch?v=3oto8Bl2vaE)
- [Forensic Memory Acquisition in Linux - LiME](https://www.youtube.com/watch?v=_7Tq8dcmP0k)
- [Forensic Memory Acquisition in Windows - FTK Imager](https://www.youtube.com/watch?v=1OxR4KLj-4I)
- [Fast password cracking - Hashcat wordlists from RAM](https://www.youtube.com/watch?v=lOTDevvqOq0)
- [What is Random Access Memory?](https://www.youtube.com/watch?v=7CqWBw6aOrs)
- [Forensics: What data can you find in RAM?](https://www.youtube.com/watch?v=kkHNhtpa0SU)

### Volatility Foundation (FTSCon)
- [Detection and Analysis of Memory-Only Linux Rootkits (2025)](https://www.youtube.com/watch?v=QrrjfuVFNOY)
- [Rethinking DMA Attacks with Erebus (2025)](https://www.youtube.com/watch?v=uJEy9rCVAPw)
- [Detecting & Defeating EDR-Evading Malware with Volatility 3 (2024)](https://www.youtube.com/watch?v=OWNGcxyNjIQ)
- [Ghidra + Volatility – Adventures in Kernel Debugging (2024)](https://www.youtube.com/watch?v=UDZlH_9uo4Y)

### DEF CON 32
- [Defeating EDR Evading Malware with Memory Forensics](https://www.youtube.com/watch?v=PmqvBe1LSZc)

### Black Hat 2022
- [New Memory Forensics Techniques to Defeat Device Monitoring Malware](https://www.blackhat.com/us-22/briefings/schedule/index.html#new-memory-forensics-techniques-to-defeat-device-monitoring-malware-27403)

### Black Hat 2019
- [Investigating Malware Using Memory Forensics - A Practical Approach](https://www.youtube.com/watch?v=BMFCdAGxVN4)

### Black Hat 2012
- [One-byte Modification for Breaking Memory Forensic Analysis](https://www.youtube.com/watch?v=HPgHLUVjxBU)

### SANS Digital Forensics and Incident Response
- [SANS DFIR Webcast - Memory Forensics for Incident Response](https://www.youtube.com/watch?v=3xAEsDT-4NA)
- [Memory Forensics: How we used to do it & how we use it to respond to large-scale breaches today](https://www.youtube.com/watch?v=fhBQ3IZnW-Q)

### ETC
- [Memory Forensics with Jupyter Notebooks](https://www.youtube.com/watch?v=MaKYas4sOfU)
- [Modern Memory Forensics with Volatility 3 - BSides Seattle 2024](https://www.youtube.com/watch?v=6d9a0HQ-FNU)
- [Using Volatility 3 to Combat Modern Malware - RVAsec 2025](https://www.youtube.com/watch?v=qkAQzGNhn0U)
- [Using Volatility 3 to Detect Sophisticated Malware - BSidesNYC 2025](https://www.youtube.com/watch?v=cpjP2wius-k)
- [Intro to Memory Forensics - RITSEC 2026](https://www.youtube.com/watch?v=4mcOQF0Kfsk)

## Articles

### Volatility Foundation
- [Announcing the Official Parity Release of Volatility 3!](https://volatilityfoundation.org/announcing-the-official-parity-release-of-volatility-3/)
- [Memory Forensics R&D Illustrated: Recovering Raw Sockets on Windows 10+](https://volatilityfoundation.org/memory-forensics-rd-illustrated-recovering-raw-sockets-on-windows-10/)
- [Memory Forensics R&D Illustrated: Detecting Hidden Windows Services](https://volatilityfoundation.org/memory-forensics-rd-illustrated-detecting-hidden-windows-services/)

### JPCERT
- [ETW Forensics - Why use Event Tracing for Windows over EventLog?](https://blogs.jpcert.or.jp/en/2024/11/etw_forensics.html)
- [How to Use Volatility 3 Offline](https://blogs.jpcert.or.jp/en/2021/09/volatility3_offline.html)
- [Migrate Volatility Plugins 2 to 3](https://blogs.jpcert.or.jp/en/2020/07/how-to-convert-vol-plugin.html)
- [MalConfScan with Cuckoo: Plugin to Automatically Extract Malware Configuration](https://blogs.jpcert.or.jp/en/2019/08/malconfscan-with-cuckoo.html)
- [Volatility Plugin for Detecting RedLeaves Malware](https://blogs.jpcert.or.jp/en/2017/05/volatility-plugin-for-detecting-redleaves-malware.html)
- [A New Tool to Detect Known Malware from Memory Images – impfuzzy for Volatility –](https://blogs.jpcert.or.jp/en/2016/12/a-new-tool-to-d-d6bc.html)
- [A Volatility Plugin Created for Detecting Malware Used in Targeted Attacks](https://blogs.jpcert.or.jp/en/2015/11/a-volatility-plugin-created-for-detecting-malware-used-in-targeted-attacks.html)
- [Volatility Plugin for Detecting Cobalt Strike Beacon](https://blogs.jpcert.or.jp/en/2018/08/volatility-plugin-for-detecting-cobalt-strike-beacon.html)

### Blogs
- [📦 Volatility3 Windows Plugin : Prefetch](https://www.forensicxlab.com/blog/prefetch)
- [📦 Volatility3 Linux Plugin : Inodes](https://www.forensicxlab.com/blog/inodes)
- [Memory analysis using volatility3 (1) - Windows 11](https://cpuu.hashnode.dev/how-to-perform-memory-forensic-analysis-in-windows-11-using-volatility-3)
- [Memory analysis using volatility3 (2) - Ubuntu Linux](https://cpuu.hashnode.dev/how-to-perform-memory-forensic-analysis-in-linux-using-volatility-3)
- [Memory analysis using volatility3 (3) - macOS](https://cpuu.hashnode.dev/how-to-perform-memory-forensic-analysis-in-macos-using-volatility-3)
- [Realizing Windows Memory Forensics with Volatility and Gimp](https://developpaper.com/ctf-realizing-windows-memory-forensics-with-volatility-and-gimp/)
- [Using Volatility for advanced memory forensics](https://www.pentestpartners.com/security-blog/using-volatility-for-advanced-memory-forensics/)
- [Mounting memory with MemProcFS for advanced memory forensics](https://www.pentestpartners.com/security-blog/mounting-memory-with-memprocfs-for-advanced-memory-forensics/)
- [Memory Analysis with Velociraptor - Part 1](https://docs.velociraptor.app/blog/2025/2025-11-15-memory-analysis-pt1/)
- [Memory Analysis with Velociraptor - Part 2](https://docs.velociraptor.app/blog/2025/2025-12-22-memory-analysis-pt2/)
- [eBPF rootkits and the Volatility blind spot in Linux memory forensics](https://andreafortuna.org/2026/05/27/ebpf-rootkits/)
- [Mind the (Patch) Gap, Part 3: Analysis with Volexity Volcano, Threat Intel, and MCP](https://www.volexity.com/blog/2026/10/16/mind-the-patch-gap-part-3-analysis-with-volexity-volcano-threat-intel-and-mcp/)

### CheatSheet
- [Volatility3 CheatSheet](https://blog.onfvp.com/post/volatility-cheatsheet/)
- [Volatility - CheatSheet (HackTricks)](https://hacktricks.wiki/en/generic-methodologies-and-resources/basic-forensic-methodology/memory-dump-analysis/volatility-cheatsheet.html)

### WriteUps
- [13Cubed Windows Memory Forensics Challenge](https://www.iblue.team/ctf-challenges/13cubed-windows-memory-forensics)
- [13Cubed Linux Memory Forensics Challenge](https://www.iblue.team/ctf-challenges/13cubed-linux-memory-forensics)

## Papers

### Digital Investigation
- [The evidence beyond the wall: Memory forensics in SGX environments](https://www.sciencedirect.com/science/article/abs/pii/S2666281721002389)

### DFRWS USA 2026
- [With or Without Logs: Memory Forensic Reconstruction of Model Context Protocol (MCP) Activity in Agentic LLM Systems](https://dfrws.org/presentation/with-or-without-logs-reconstructing-model-context-protocol-activity-from-volatile-memory/)
- [Rusting Volatility: Accelerating Memory Forensics through LLM-Assisted Cross-Language Migration](https://dfrws.org/presentation/rusting-volatility-accelerating-memory-forensics-through-llm-assisted-cross-language-migration/)
- [Memory Forensics Techniques for Automated Detection and Analysis of Go Malware](https://dfrws.org/presentation/memory-forensics-techniques-for-automated-detection-and-analysis-of-go-malware/)
- [I Guess it is Correct – A Survey about Acquiring and Analyzing Main Memory](https://dfrws.org/presentation/i-guess-it-is-correct-a-survey-about-acquiring-and-analyzing-main-memory/)

### DFRWS EU 2026
- [Structural Analysis of the Windows NT Heap for Memory Forensics](https://dfrws.org/presentation/structural-analysis-of-the-windows-nt-heap-for-memory-forensics/)
- [LEMON: A Universal eBPF-based Volatile Memory Acquisition Tool for Modern Android Devices and Hardened Linux Systems](https://dfrws.org/presentation/lemon-a-universal-ebpf-based-volatile-memory-acquisition-tool-for-modern-android-devices-and-hardened-linux-systems/)

### RAID 2025
- [A Comprehensive Quantification of Inconsistencies in Memory Dumps](https://s3.eurecom.fr/docs/raid25_oliveri.pdf)

### DFRWS USA 2025
- [Memory Analysis of the Python Runtime Environment](https://dfrws.org/presentation/memory-analysis-of-the-python-runtime-environment/)
- [Leveraging Memory Forensics to Investigate and Detect Illegal 3D Printing Activities](https://dfrws.org/presentation/leveraging-memory-forensics-to-investigate-and-detect-illegal-3d-printing-activities/)
- [Detecting Hidden Kernel Modules in Memory Snapshots](https://dfrws.org/presentation/detecting-hidden-kernel-modules-in-memory-snapshots/)
- [Uncovering Linux Desktop Espionage](https://dfrws.org/presentation/uncovering-linux-desktop-espionage/)

### DFRWS EU 2025
- [A Scenario-Based Quality Assessment of Memory Acquisition Tools and its Investigative Implications](https://dfrws.org/presentation/a-scenario-based-quality-assessment-of-memory-acquisition-tools-and-its-investigative-implications/)
- [A Study on the Evolution of Kernel Data Types Used in Memory Forensics and Their Dependency on Compilation Options](https://dfrws.org/presentation/a-study-on-the-evolution-of-kernel-data-types-used-in-memory-forensics-and-their-dependency-on-compilation-options/)

### DFRWS APAC 2025
- [All Your TLS Keys Are Belong to Us: A Novel Approach to Live Memory Forensic Key Extraction](https://dfrws.org/presentation/all-your-tls-keys-are-belong-to-us-a-novel-approach-to-live-memory-forensic-key-extraction/)
- [Advanced Monero Wallet Forensics: Demystifying Off-Chain Artifacts to Trace Privacy-Preserving Cryptocurrency Transactions](https://dfrws.org/presentation/advanced-monero-wallet-forensics-demystifying-off-chain-artifacts-to-trace-privacy-preserving-cryptocurrency-transactions/)

### NDSS 2025
- [SCRUTINIZER: Towards Secure Forensics on Compromised TrustZone](https://www.ndss-symposium.org/ndss-paper/scrutinizer-towards-secure-forensics-on-compromised-trustzone/)

### USENIX Security 2024
- [AI Psychiatry: Forensic Investigation of Deep Learning Networks in Memory Images](https://www.usenix.org/conference/usenixsecurity24/presentation/oygenblik)

### DFRWS USA 2024
- [volGPT: Evaluation on triaging ransomware process in memory forensics with Large Language Model](https://dfrws.org/presentation/volgpt-evaluation-on-triaging-ransomware-process-in-memory-forensics-with-large-language-model/)
- [TLS key material identification and extraction in memory: Current state and future challenges](https://dfrws.org/presentation/tls-key-material-identification-and-extraction-in-memory-current-state-and-future-challenges/)
- [On enhancing memory forensics with FAME: Framework for advanced monitoring and execution](https://dfrws.org/presentation/on-enhancing-memory-forensics-with-fame-framework-for-advanced-monitoring-and-execution/)
- [In the time loop: Data remanence in main memory of virtual machines](https://dfrws.org/presentation/in-the-time-loop-data-remanence-in-main-memory-of-virtual-machines/)
- [A step in a new direction: NVIDIA GPU kernel driver memory forensics](https://dfrws.org/presentation/a-step-in-a-new-direction-nvidia-gpu-kernel-driver-memory-forensics/)

### DFRWS APAC 2024
- [MIC: Memory analysis of IndexedDB data on Chromium-based applications](https://dfrws.org/presentation/mic-memory-analysis-of-indexeddb-data-on-chromium-based-applications/)

### DFRWS USA 2023
- [Windows memory forensics: Identification of (malicious) modifications in memory-mapped image files](https://dfrws.org/presentation/windows-memory-forensics-identification-of-malicious-modifications-in-memory-mapped-image-files/)
- [Database memory forensics: Identifying cache patterns for log verification](https://dfrws.org/presentation/database-memory-forensics-identifying-cache-patterns-for-log-verification/)
- [cRGB_Mem: At the intersection of memory forensics and machine learning](https://dfrws.org/presentation/crgb_mem-at-the-intersection-of-memory-forensics-and-machine-learning/)
- [As if Time Had Stopped – Checking Memory Dumps for Quasi-Instantaneous Consistency](https://dfrws.org/presentation/as-if-time-had-stopped-checking-memory-dumps-for-quasi-instantaneous-consistency/)

### DFRWS EU 2023
- [Towards generic memory forensic framework for programmable logic controllers](https://dfrws.org/presentation/towards-generic-memory-forensic-framework-for-programmable-logic-controllers/)
- [Module extraction and DLL hijacking detection via single or multiple memory dumps](https://dfrws.org/presentation/module-extraction-and-dll-hijacking-detection-via-single-or-multiple-memory-dumps/)
- [Database memory forensics: A machine learning approach to reverse-engineer query activity](https://dfrws.org/presentation/database-memory-forensics-a-machine-learning-approach-to-reverse-engineer-query-activity/)
- [Forensic method for decrypting TPM-protected BitLocker volumes using Intel DCI](https://dfrws.org/presentation/forensic-method-for-decrypting-tpm-protected-bitlocker-volumes-using-intel-dci/)

### DFRWS APAC 2023
- [Chracer: Memory analysis of Chromium-based browsers](https://dfrws.org/presentation/chracer-memory-analysis-of-chromium-based-browsers/)
- [About the applicability of Apache2 web server memory forensics](https://dfrws.org/presentation/about-the-applicability-of-apache2-web-server-memory-forensics/)

### NDSS 2023
- [An OS-agnostic Approach to Memory Forensics](https://www.ndss-symposium.org/ndss-paper/an-os-agnostic-approach-to-memory-forensics/)

### DFRWS USA 2022
- [Memory Analysis of .NET and .Net Core Applications](https://dfrws.org/presentation/memory-analysis-of-net-and-net-core-applications)
- [Juicing V8: A Primary Account for the Memory Forensics of the V8 JavaScript Engine](https://dfrws.org/presentation/juicing-v8-a-primary-account-for-the-memory-forensics-of-the-v8-javascript-engine/)

### DFRWS EU 2022
- [Extraction and analysis of retrievable memory artifacts from Windows Telegram Desktop application](https://dfrws.org/presentation/extraction-and-analysis-of-retrievable-memory-artifacts-from-windows-telegram-desktop-application/)
- [Defining Atomicity (and Integrity) for Snapshots of Storage in Forensic Computing](https://dfrws.org/presentation/defining-atomicity-and-integrity-for-snapshots-of-storage-in-forensic-computing/)
- [Memory forensic analysis of a programmable logic controller in industrial control systems](https://dfrws.org/presentation/memory-forensic-analysis-of-a-programmable-logic-controller-in-industrial-control-systems/)

### DFRWS USA 2021
- [Duck Hunt: Memory Forensics of USB Attack Platforms](https://dfrws.org/presentation/duck-hunt-memory-forensics-of-usb-attack-platforms/)
- [Seance: Divination of Tool-Breaking Changes in Forensically Important Binaries](https://dfrws.org/presentation/seance-divination-of-tool-breaking-changes-in-forensically-important-binaries/)
- [Leveraging Intel DCI for Memory Forensics](https://dfrws.org/presentation/leveraging-intel-dci-for-memory-forensics/)

### DFRWS EU 2021
- [One key to rule them all: Recovering the master key from RAM to break Android's file-based encryption](https://dfrws.org/presentation/one-key-to-rule-them-all-recovering-the-master-key-from-ram-to-break-androids-file-based-encryption/)

### DFRWS USA 2020
- [Hiding Process Memory via Anti-Forensic Techniques](http://dfrws.org/presentation/hiding-process-memory-via-anti-forensic-techniques/)
- [Memory Analysis of macOS Page Queues](https://dfrws.org/presentation/memory-analysis-of-macos-page-queues/)
- [Memory FORESHADOW: Memory FOREnSics of HArDware cryptOcurrency Wallets – A Tool and Visualization Framework](https://dfrws.org/presentation/memory-foreshadow-memory-forensics-of-hardware-cryptocurrency-wallets-a-tool-and-visualizaton-framework/)

### DFRWS EU 2020
- [BMCLeech: Introducing Stealthy Memory Forensics to BMC Tobias Latzo](http://dfrws.org/wp-content/uploads/2020/05/BMCLeech-Introducing-Stealthy-Memor_2020_Forensic-Science-International-Di.pdf)
- [Tampering Digital Evidence is Hard: The Case of Main Memory Images](http://dfrws.org/wp-content/uploads/2020/05/Tampering-with-Digital-Evidence-is-Hard-_2020_Forensic-Science-Internationa.pdf)
- [On Challenges in Verifying Trusted Executable Files in Memory Forensics](http://dfrws.org/wp-content/uploads/2020/05/On-Challenges-in-Verifying-Trusted-Execut_2020_Forensic-Science-Internationa.pdf)

## Datasets

- [Digital Corpora](https://downloads.digitalcorpora.org/corpora/scenarios/2009-m57-patents/ram/) - Daily RAM images from the M57-Patents scenario.
- [NIST](https://cfreds.nist.gov/mem/memory-images.rar)
- [The Art of Memory Forensics](https://www.memoryanalysis.net/amf)
- [MemLabs](https://github.com/stuxnet999/MemLabs)
- [Windows XP](https://downloads.volatilityfoundation.org/volatility3/images/win-xp-laptop-2005-06-25.img.gz)
- [Volatility Memory Samples](https://github.com/volatilityfoundation/volatility/wiki/Memory-Samples) - Index of public Windows, Linux, macOS and Android memory images.
- [CIC-MalMem-2022](https://www.unb.ca/cic/datasets/malmem-2022.html) - Obfuscated malware memory dataset (spyware, ransomware, trojan) from the Canadian Institute for Cybersecurity.

## Challenges
- [2026 Volatility Plugin Contest](https://volatilityfoundation.org/the-14th-annual-volatility-plugin-contest-is-open/)
- [2025 Volatility Plugin Contest](https://volatilityfoundation.org/the-2025-volatility-plugin-contest-results-are-in/)
- [2024 Volatility Plugin Contest](https://volatilityfoundation.org/the-2024-volatility-plugin-contest-results-are-in/)
- [2023 Volatility Plugin Contest](https://volatilityfoundation.org/the-2023-volatility-plugin-contest-results-are-in/)
- [2022 Volatility Plugin Contest](https://volatilityfoundation.org/the-2022-volatility-plugin-contest-results-are-in/)
- [2021 Volatility Plugin Contest](https://volatility-labs.blogspot.com/2022/02/the-2021-volatility-plugin-contest-results.html)
- [2020 Volatility Plugin Contest](https://volatility-labs.blogspot.com/2020/11/the-2020-volatility-plugin-contest-results.html)
- [2019 Volatility Plugin & Analysis Contests](https://volatility-labs.blogspot.com/2019/11/results-from-2019-volatility-contests.html)
- [2018 Volatility Plugin & Analysis Contests](https://volatility-labs.blogspot.com/2018/11/results-from-annual-2018-volatility-contests.html)
- [2017 Volatility Plugin Contest](https://volatility-labs.blogspot.com/2017/11/results-from-5th-annual-2017-volatility.html)
- [2016 Volatility Plugin Contest](https://volatility-labs.blogspot.com/2016/12/results-from-2016-volatility-plugin.html)
- [2015 Volatility Plugin Contest](https://www.volatilityfoundation.org/2015)
- [2014 Volatility Plugin Contest](https://www.volatilityfoundation.org/2014-cjpn)
- [2013 Volatility Plugin Contest](https://www.volatilityfoundation.org/2013-c19yz)
- [2005 DFRWS Forensic Challenge](https://github.com/dfrws/dfrws2005-challenge)
- [CyberDefenders - Reveal](https://cyberdefenders.org/blueteam-ctf-challenges/reveal/) - Windows memory analysis lab with Volatility 3.
- [CyberDefenders - Ramnit](https://cyberdefenders.org/blueteam-ctf-challenges/ramnit/) - Memory lab to identify a malicious process and extract IOCs.
- [CyberDefenders - RedLine](https://cyberdefenders.org/blueteam-ctf-challenges/redline/) - Memory lab to spot suspicious processes and C2 activity.

## Contributors
Thank you for your contribution!

We welcome any contribution to the extent that Code of Conduct and the License comply.

<a href="https://github.com/Digitalisx/awesome-memory-forensics/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Digitalisx/awesome-memory-forensics" />
</a>
