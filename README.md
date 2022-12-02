# PMA-Labs

 Practical Malware Analysis Labs & Notes

Download Labs From: <https://github.com/mikesiko/PracticalMalwareAnalysis-Labs>

Book Link: <https://www.amazon.com/Practical-Malware-Analysis-Hands-Dissecting/dp/1593272901>

Tools Used:

- Windows 7 x64 Image
- VMWare Workstation 17
- Flare VM (<https://github.com/mandiant/flare-vm>)
- Additional Software:
  - Ghidra (<https://ghidra-sre.org>)
  - Wireshark (Updated to latest release)
  - CAPA (<https://github.com/mandiant/capa>)
  - Procmon / Procmon64 version 3.86 (<https://community.chocolatey.org/packages/procmon/3.86>) - This was due to an error with the updated version.
- For Windows Kernel Debugging:
  - EDWK for Windows 10, Version 1703 (<https://learn.microsoft.com/en-us/legal/windows/hardware/enterprise-wdk-license-2015>)
  - Windows 7 WDK (<https://www.microsoft.com/download/confirmation.aspx?id=11800>)
  - VirtualKD-3.0 (<https://sysprogs.com/legacy/virtualkd>)
  - Follow instructions in the [SystemSetupGuide](SystemSetupGuide.pdf)

Setup:

    1. Install Windows
    2. Snapshot VM
    3. Install FlareVM
    4. Install Additional Software (Including the WDK)
    6. Test VM
    7. Snapshot VM
