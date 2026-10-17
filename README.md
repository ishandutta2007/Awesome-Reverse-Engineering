# Awesome-Reverse-Engineering

## Top Reverse Engineering Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Disassembly, Decompilation & Binary Analysis Automation*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Reverse Engineering**. These tools help security researchers, malware analysts, and vulnerability hunters understand compiled binaries — disassembling machine code, decompiling to C-like pseudocode, tracing execution, and automating binary analysis at scale.

**Examples** include IDA Pro, Binary Ninja, Ghidra, JEB Decompiler, Hopper, Radare2, Cutter, Angr, Veles, and Rizin (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, scriptable analysis, and transparent binary lifting — ideal for security researchers prioritizing cost, extensibility, and control over their analysis pipelines.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[IDA Pro](https://hex-rays.com/ida-pro)**  
  **The long-standing industry standard for disassembly and decompilation** — the tool most professional reverse engineers learned on . **Best-in-class x86/x64 and ARM decompiler** via the Hex-Rays Decompiler add-on, which remains a separate paid plugin . **Extensive plugin ecosystem, debugger support, and scripting** via IDAPython . **Pro pricing starts around $1,879 for the base license**, with the decompiler adding roughly $2,769 for named licenses — among the highest per-seat costs in the category . **ARM decompilation quality remains weaker than Ghidra's in head-to-head testing** despite the premium price . **Best for professional malware analysts and vulnerability researchers** whose organizations already standardize on it .

- **[Binary Ninja](https://binary.ninja/)**  
  **The modern challenger with the best API-first design** — **Intermediate Language (BNIL)** exposes multiple analysis layers, making it the easiest platform for writing automated analysis plugins . **Decompiler quality is strong across architectures** including x86, ARM, MIPS, and PowerPC . **Personal license at $299, Commercial at $1,499** — significantly cheaper than IDA Pro with faster release cadence . **First-class Rust and Python APIs** . **Struggles with malformed or obfuscated binaries where Ghidra is more tolerant** . **Best for security engineers automating binary analysis at scale** and teams wanting modern tooling without IDA's cost .

- **[JEB Decompiler](https://www.pnfsoftware.com/)**  
  **Specialized in Android/Dalvik, DEX, and APK analysis** — the reference tool for mobile reverse engineering and obfuscated Android bytecode . **Pricing from €1,000+/year per seat** depending on modules and floating licenses . **Strong for iOS and firmware analysis** in later versions . **Best for mobile security researchers and Android malware analysts** where its DEX handling is unmatched .

- **[Hopper Disassembler](https://www.hopperapp.com/)**  
  **macOS-native reverse engineering tool** — the practical choice for Mach-O binaries and iOS app analysis . **Personal license around $99, Pro around $229** — the cheapest commercial option in this list . **Decompiler quality is adequate but behind Binary Ninja and Ghidra** . **Best for macOS and iOS researchers** wanting a native-feeling tool without IDA's price or Ghidra's Java overhead .

- **[Veles](https://codisec.com/veles/)**  
  **Open-source binary analysis tool for data visualization and pattern recognition** — developed by Codisec . **Combines data visualization and pattern recognition algorithms** to help analysts identify structures in raw binary data . **Best for initial reconnaissance** of unknown file formats and firmware images where visual pattern discovery beats line-by-line disassembly .

## Open-Source GitHub Projects

- **[Ghidra](https://github.com/NationalSecurityAgency/ghidra)**  
  **The NSA's open-source reverse engineering framework** — Apache 2.0 licensed, **60,000+ GitHub stars** . **Full-featured disassembler, decompiler, and scripting environment** supporting x86, ARM, MIPS, PowerPC, RISC-V, and dozens more architectures . **Head-to-head testing shows Ghidra produces the most reliable decompilation and is most robust against malformed, obfuscated, or packed binaries** — where Binary Ninja and IDA struggle, Ghidra often succeeds . **Scriptable in Java and Python** (via Ghidra's Jython) with a large plugin ecosystem . **Free and unrestricted** — no license cost at any scale . **Trade-offs**: Java-based, heavier resource usage, and a steeper learning curve for the UI compared to Binary Ninja . **The strongest all-around open-source choice for malware analysis and vulnerability research** .

- **[Radare2](https://github.com/radareorg/radare2)**  
  **The UNIX-like reverse engineering framework and command-line toolset** — LGPL-3.0 licensed, **20,000+ GitHub stars** . **Scriptable in Python, JavaScript, and native r2pipe** — designed for automation and batch analysis . **Supports dozens of architectures and file formats** . **Hex editor, debugger, disassembler, and binary diffing** in one toolkit . **r2dec** and **r2ghidra-dec** provide decompilation via plugins . **Cutter** is the official GUI . **The most flexible CLI-driven RE framework** — everything is scriptable and pipeable . **Trade-offs**: steep learning curve and a command syntax that takes time to internalize . **Best for automation-heavy reverse engineering** and researchers who live in the terminal .

- **[Cutter](https://github.com/rizinorg/cutter)**  
  **The official GUI for Rizin (Radare2 fork)** — GPL-3.0 licensed, **18,000+ GitHub stars** . **Qt-based interface on top of the Rizin engine** (a community fork of Radare2 after maintainership changes) . **Graph view, decompiler integration (Ghidra decompiler plugin), and debugger** . **Best for users wanting Radare2's power with a graphical interface** and a more active development cadence than Radare2 .

- **[Rizin](https://github.com/rizinorg/rizin)**  
  **The community fork of Radare2** — LGPL-3.0 licensed . **Forked to accelerate development after Radare2's maintainership slowed** . **Compatible with much of the r2 plugin ecosystem** while modernizing the codebase . **Best for teams wanting Radare2-style scripting with more active maintenance** .

- **[Angr](https://github.com/angr/angr)**  
  **The Python framework for binary analysis with symbolic execution and concolic testing** — BSD-2-Clause licensed, **7,500+ GitHub stars** . **Symbolic execution engine** that explores program paths to find inputs that reach specific states — **the standard tool for automated vulnerability discovery** . **CFG recovery, data dependency analysis, decompilation, and patching** . **The foundation for automated CTF solving and vulnerability research** . **Best for automated binary analysis research** and finding bugs that manual review misses .

- **[Capstone](https://github.com/capstone-engine/capstone)**  
  **The lightweight multi-platform, multi-architecture disassembly framework** — BSD-3-Clause licensed, **7,500+ GitHub stars** . **Disassembly engine used by many other tools** including Radare2, Angr, and countless plugins . **Supports ARM, ARM64, MIPS, x86, PowerPC, SPARC, SystemZ, and more** . **Python, Java, and C bindings** . **Best for building custom disassembly tooling** — it's a library, not an application .

- **[Keystone](https://github.com/keystone-engine/keystone)**  
  **The lightweight multi-platform, multi-architecture assembler framework** — GPL-2.0 licensed . **The assembler counterpart to Capstone** — assembles instructions for ARM, ARM64, MIPS, x86, PowerPC, SPARC, SystemZ, and more . **Best for binary patching, shellcode generation, and assembly automation** .

- **[Unicorn](https://github.com/unicorn-engine/unicorn)**  
  **The lightweight multi-platform, multi-architecture CPU emulator framework** — GPL-2.0 licensed, **8,000+ GitHub stars** . **Based on QEMU** but focused on CPU emulation only, making it lightweight and embeddable . **Emulates ARM, ARM64, MIPS, x86, PowerPC, SPARC, and more** . **The foundation for many emulation-based analysis tools** including some Angr components . **Best for emulating specific code paths** in isolation without running a full VM .

- **[RetDec](https://github.com/avast/retdec)**  
  **Retargetable machine-code decompiler based on LLVM** — MIT licensed . **Decompiles ARM, MIPS, PIC32, PowerPC, and x86 binaries to LLVM IR and then to C** . **Supports both executable formats and raw machine code** . **Best for batch decompilation** where you want C output across many binaries .

- **[dnSpy](https://github.com/dnSpyEx/dnSpy)**  
  **.NET debugger and assembly editor** — GPL-3.0 licensed . **Decompiles .NET assemblies to C# and Visual Basic** with editable output . **The standard tool for .NET reverse engineering** — .NET's IL metadata makes decompilation cleaner than native code . **dnSpyEx** is the actively maintained community fork after the original was archived . **Best for .NET malware analysis and game modding** .

- **[ILSpy](https://github.com/icsharpcode/ILSpy)**  
  **The open-source .NET assembly browser and decompiler** — MIT licensed, **20,000+ GitHub stars** . **Cross-platform with Avalonia UI** . **Decompiles IL to C#** with strong support for modern language features . **Best for .NET development** and understanding library internals .

### Additional Strong Open-Source Options

- **Frida** — Dynamic instrumentation toolkit for injecting JavaScript into native apps. The standard for runtime reverse engineering on mobile and desktop.
- **x64dbg** — Open-source x64/x32 debugger for Windows with plugin support.
- **GDB** — The GNU debugger with reverse debugging capabilities and extensive scripting.
- **LLDB** — LLVM's debugger with Python scripting, the default on macOS.
- **Pwndbg / GEF / PEDA** — GDB extensions enhancing binary exploitation workflows.
- **Binwalk** — Firmware analysis tool for extracting filesystems and identifying embedded structures.
- **Detect It Easy (DIE)** — Packer, compiler, and protector detection for PE, ELF, and Mach-O files.
- **PE-bear** — PE file reversing tool with headers, sections, imports, and resources.

**Frameworks for building custom systems**: Combine **Ghidra** for the most robust free decompilation across architectures, **Radare2** or **Rizin** with **Cutter** for scriptable CLI and GUI analysis, **Binary Ninja** for the best plugin API if budget allows, **Angr** for symbolic execution and automated vulnerability discovery, **Capstone** and **Keystone** for custom disassembly and assembly tooling, and **Unicorn** for lightweight CPU emulation — to build a reverse engineering environment tailored to your architecture targets, automation needs, and budget.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Reverse engineering tools should be used ethically and legally — analyzing software you own, have permission to analyze, or for security research within applicable laws. **Bypassing licensing protections, extracting copyrighted code, or analyzing systems without authorization may violate laws including the DMCA and CFAA** . **Ghidra produces the most reliable decompilation and is most robust against malformed or obfuscated binaries** in independent testing — despite IDA Pro's higher price . **IDA Pro's ARM decompilation quality lags Ghidra** while costing significantly more . **Binary Ninja has the cleanest API** but struggles with malformed binaries where Ghidra succeeds . **Decompiler output is never perfect** — always verify critical logic against disassembly .
- Self-hosted open-source solutions require proper Java runtime for Ghidra, Python environments for Angr, and hardware capable of handling large binaries — some firmware images can consume many gigabytes of RAM during analysis.

---

**Made for security researchers, malware analysts, vulnerability hunters, and CTF players.**
Let's make reverse engineering more open, accessible, and automation-friendly.
