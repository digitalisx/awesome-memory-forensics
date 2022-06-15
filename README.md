# Awesome Memory Forensics [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of awesome Memory Forensics for DFIR.

> [Memory Forensics](https://en.wikipedia.org/wiki/Memory_forensics) is forensic analysis of a computer's memory dump. Its primary application is investigation of advanced computer attacks which are stealthy enough to avoid leaving data on the computer's hard drive. Consequently, the memory (RAM) must be analyzed for forensic information.

If you want to contribute, please read the [contribution guidelines](contributing.md).

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

## Memory Acquisition
Introduce commercial and open source tools for memory acquisition.

### Software
- [MAGNET RAM](https://www.magnetforensics.com/resources/magnet-ram-capture/) - MAGNET RAM Capture is a free imaging tool designed to capture the physical memory of a suspect's computer, allowing investigators to recover and analyze valuable artifacts that are often only found in memory.
- [FTK Imager](https://www.exterro.com/ftk-imager)
- [Winpmem](https://github.com/Velocidex/WinPmem)
- [Ram Capturer](https://belkasoft.com/ram-capturer) - Belkasoft Live RAM Capturer is a tiny free forensic tool that allows to reliably extract the entire contents of computer's volatile memory—even if protected by an active anti-debugging or anti-dumping system.
- [LiME](https://github.com/504ensicsLabs/LiME) - A Loadable Kernel Module (LKM) which allows for volatile memory acquisition from Linux and Linux-based devices, such as Android. 
- [AVML](https://github.com/microsoft/avml) - AVML is an X86_64 userland volatile memory acquisition tool written in Rust, intended to be deployed as a static binary. 
- [fmem](https://github.com/NateBrune/fmem)
- [FEX Memory Imager](https://getdataforensics.com/product/fex-memory-imager/) - FEX Memory Imager (FEX Memory) is a free imaging tool designed to capture the physical Random Access Memory (RAM) of a suspect's running computer. This allows investigators to recover and analyze valuable artifacts found only in memory.
- [MacQuisition](https://www.blackbagtech.com/category/blog/macquisition/)

### Hardware
- [PCILeech](https://github.com/ufrisk/pcileech) - PCILeech uses PCIe hardware devices to read and write target system memory. This is achieved by using DMA over PCIe. No drivers are needed on the target system.

## Memory Analysis
Introduce commercial and open source tools for memory analysis.
- [Volcano](https://www.volexity.com/products-overview/volcano) - A comprehensive, cross-platform, next- generation memory analysis solution, Volexity Volcano Professional's powerful core extracts, indexes, and correlates artifacts to provide unprecedented visibility into systems' runtime state and trustworthiness.
- [Volatility3](https://github.com/volatilityfoundation/volatility3) - Volatility is the world's most widely used framework for extracting digital artifacts from volatile memory (RAM) samples.
- [MemProcFS](https://github.com/ufrisk/MemProcFS) - The Memory Process File System (MemProcFS) is an easy and convenient way of viewing physical memory as files in a virtual file system.
- [WinDbg](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugger-download-tools) - The Windows Debugger (WinDbg) can be used to debug kernel-mode and user-mode code, analyze crash dumps, and examine the CPU registers while the code executes.
- [Volatility](https://github.com/volatilityfoundation/volatility) - The Volatility Framework is a completely open collection of tools,
implemented in Python under the GNU General Public License, for the
extraction of digital artifacts from volatile memory (RAM) samples.
- [Volafox](https://github.com/n0fate/volafox) - macOS Memory Analysis Toolkit' is developed on Python 2.x (***Deprecated***)
- [Rekall](https://github.com/google/rekall) - A new branch within the Volatility project was created to explore how to make the code base more modular, improve performance, and increase usability. (***Deprecated***)
- [Redline](https://fireeye.market/apps/211364) - Redline®, FireEye's premier free endpoint security tool, provides host investigative capabilities to users to find signs of malicious activity through memory and file analysis and the development of a threat assessment profile.


## Books
- [The Art of Memory Forensics](https://www.amazon.com/Art-Memory-Forensics-Detecting-Malware/dp/1118825098) - Detecting Malware and Threats in Windows, Linux, and Mac Memory.
- [Practical Memory Forensics](https://www.amazon.com/Practical-Memory-Forensics-Jumpstart-effective/dp/1801070334) - Jumpstart effective forensic analysis of volatile memory.


## Course
- [Malware and Memory Forensics Training**](https://www.memoryanalysis.net/memory-forensics-training)

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

### DFIR Science
- [Introduction to Memory Forensics with Volatility 3](https://www.youtube.com/watch?v=Uk3DEgY5Ue8)
- [Amazon AWS EC2 Forensic Memory Acquisition - LiME](https://www.youtube.com/watch?v=3oto8Bl2vaE)
- [Forensic Memory Acquisition in Linux - LiME](https://www.youtube.com/watch?v=_7Tq8dcmP0k)
- [Forensic Memory Acquisition in Windows - FTK Imager](https://www.youtube.com/watch?v=1OxR4KLj-4I)
- [Fast password cracking - Hashcat wordlists from RAM](https://www.youtube.com/watch?v=lOTDevvqOq0)

### Black Hat 2022
- [New Memory Forensics Techniques to Defeat Device Monitoring Malware](https://www.blackhat.com/us-22/briefings/schedule/index.html#new-memory-forensics-techniques-to-defeat-device-monitoring-malware-27403)

### Black Hat 2019
- [Investigating Malware Using Memory Forensics - A Practical Approach](https://www.youtube.com/watch?v=BMFCdAGxVN4)

### Black Hat 2012
- [One-byte Modification for Breaking Memory Forensic Analysis](https://www.youtube.com/watch?v=HPgHLUVjxBU)

### SANS Digital Forensics and Incident Response
- [SANS DFIR Webcast - Memory Forensics for Incident Response](https://www.youtube.com/watch?v=3xAEsDT-4NA)

### ETC
- [Memory Forensics with Jupyter Notebooks](https://www.youtube.com/watch?v=MaKYas4sOfU)

## Articles

### JPCERT
- [How to Use Volatility 3 Offline](https://blogs.jpcert.or.jp/en/2021/09/volatility3_offline.html)
- [Migrate Volatility Plugins 2 to 3](https://blogs.jpcert.or.jp/en/2020/07/how-to-convert-vol-plugin.html)
- [MalConfScan with Cuckoo: Plugin to Automatically Extract Malware Configuration](https://blogs.jpcert.or.jp/en/2019/08/malconfscan-with-cuckoo.html)
- [Volatility Plugin for Detecting RedLeaves Malware](https://blogs.jpcert.or.jp/en/2017/05/volatility-plugin-for-detecting-redleaves-malware.html)
- [A New Tool to Detect Known Malware from Memory Images – impfuzzy for Volatility –](https://blogs.jpcert.or.jp/en/2016/12/a-new-tool-to-d-d6bc.html)
- [A Volatility Plugin Created for Detecting Malware Used in Targeted Attacks](https://blogs.jpcert.or.jp/en/2015/11/a-volatility-plugin-created-for-detecting-malware-used-in-targeted-attacks.html)
- [Volatility Plugin for Detecting Cobalt Strike Beacon](https://blogs.jpcert.or.jp/en/2018/08/volatility-plugin-for-detecting-cobalt-strike-beacon.html)

### Blogs
- [Memory analysis using volatility3 (1) - Windows 10](https://cpuu.postype.com/post/9993241)
- [Memory analysis using volatility3 (2) - Ubuntu Linux](https://cpuu.postype.com/post/11807930)

### WriteUps

## Papers

### Digital Investigation
- [The evidence beyond the wall: Memory forensics in SGX environments](https://www.sciencedirect.com/science/article/abs/pii/S2666281721002389)

### DFRWS USA 2022
- [Memory Analysis of .NET and .Net Core Applications](https://dfrws.org/presentation/memory-analysis-of-net-and-net-core-applications)
- [Juicing V8: A Primary Account for the Memory Forensics of the V8 JavaScript Engine](https://dfrws.org/presentation/juicing-v8-a-primary-account-for-the-memory-forensics-of-the-v8-javascript-engine/)

### DFRWS EU 2022
- Extraction and analysis of retrievable memory artifacts from Windows Telegram Desktop application
- Defining Atomicity (and Integrity) for Snapshots of Storage in Forensic Computing
- Memory forensic analysis of a programmable logic controller in industrial control systems

### DFRWS USA 2021
- Duck Hunt: Memory Forensics of USB Attack Platforms
- Seance: Divination of Tool-Breaking Changes in Forensically Important Binaries
- Leveraging Intel DCI for Memory Forensics

### DFRWS EU 2021
- [One key to rule them all: Recovering the master key from RAM to break Android's file-based encryption](https://dfrws.org/presentation/one-key-to-rule-them-all-recovering-the-master-key-from-ram-to-break-androids-file-based-encryption/)

### DFRWS USA 2020
- [Hiding Process Memory via Anti-Forensic Techniques](http://dfrws.org/presentation/hiding-process-memory-via-anti-forensic-techniques/)
- [Memory Analysis of macOS Page Queues](https://dfrws.org/presentation/memory-analysis-of-macos-page-queues/)
- [Memory FORESHADOW: Memory FOREnSics of HArDware cryptOcurrency Wallets – A Tool and Visualization Framework](https://dfrws.org/presentation/memory-foreshadow-memory-forensics-of-hardware-cryptocurrency-wallets-a-tool-and-visualizaton-framework/)

## Datasets

- Digital Corpora
- NIST
- Memory Forensic Training
- [MemLabs](https://github.com/stuxnet999/MemLabs)

## Challenges
- [2021 Volatility Plugin Contest](https://volatility-labs.blogspot.com/2022/02/the-2021-volatility-plugin-contest-results.html)
- [2020 Volatility Plugin Contest](https://volatility-labs.blogspot.com/2020/11/the-2020-volatility-plugin-contest-results.html)
- [2019 Volatility Plugin & Analysis Contests](https://volatility-labs.blogspot.com/2019/11/results-from-2019-volatility-contests.html)
- [2018 Volatility Plugin & Analysis Contests](https://volatility-labs.blogspot.com/2018/11/results-from-annual-2018-volatility-contests.html)
- [2017 Volatility Plugin Contest](https://volatility-labs.blogspot.com/2017/11/results-from-5th-annual-2017-volatility.html)
- [2016 Volatility Plugin Contest](https://volatility-labs.blogspot.com/2016/12/results-from-2016-volatility-plugin.html)
- [2015 Volatility Plugin Contest](https://www.volatilityfoundation.org/2015)
- [2015 DFRWS Forensic Challenge](https://github.com/dfrws/dfrws2005-challenge)
- [2014 Volatility Plugin Contest](https://www.volatilityfoundation.org/2014-cjpn)
- [2013 Volatility Plugin Contest](https://www.volatilityfoundation.org/2013-c19yz)


## Contributors
Thank you for your contribution!

We welcome any contribution to the extent that Code of Conduct and the License comply.

<a href="https://github.com/Digitalisx/awesome-memory-forensics/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Digitalisx/awesome-memory-forensics" />
</a>
