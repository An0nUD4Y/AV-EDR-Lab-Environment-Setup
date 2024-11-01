# AV/EDR Lab Environment Setup
> Initially taken from Maldev Academy Discord and added more resources.

> Notion Notes : https://an0nud4y.notion.site/AV-EDR-Lab-Env-Setup-130bc870022d8071935cc682d3eb34b9?pvs=4


- An example of things that can be used to emulate certain features that paid edrs have:
    - SACL - sysmon
        - https://detect.fyi/sysmon-a-viable-alternative-to-edr-44d4fbe5735a?gi=eb4475ea6b3d
        - https://techcommunity.microsoft.com/t5/windows-server-for-it-pro/active-directory-hunting-set-up-advanced-monitoring-with-sysmon/m-p/3977120
        - Sysmon Config : https://github.com/SwiftOnSecurity/sysmon-config
    - HOOKS
        - bitdefender free : [https://otterhacker.github.io/Malware/Function hooking.html](https://otterhacker.github.io/Malware/Function%20hooking.html)
        - HookDetector (Detect all hooked APIs) : https://github.com/matterpreter/OffensiveCSharp/tree/master/HookDetector
        - TelemetrySourcerer (enumerate and disable common sources of telemetry used by AV/EDR, Including ETW , User-ModeHooks, Kernel Callbacks) : https://github.com/jthuraisamy/TelemetrySourcerer
    - Detecting manual syscalls from usermode
        - https://github.com/jackullrich/syscall-detect
        - hook the current process to identify the manual syscall executions on windows : https://github.com/paranoidninja/Process-Instrumentation-Syscall-Hook
    - PROCESS/PESCAN
        - Yapscan - hoard as many yara rules as you can
        - DetectItEasy(DIE) :  https://github.com/horsicq/Detect-It-Easy
    - ETW-TI/ETW  Providers/Consumers -
        - silketw : https://otterhacker.github.io/Malware/ETW.html
        - ETWInspector : https://github.com/jsecurity101/ETWInspector
        - List ETW Providers for a process : https://github.com/whokilleddb/ETWListicle
        - KrabsETW (Microsoft ETW Consumer) : https://github.com/microsoft/krabsetw
        - BlueKrabsETW (For blueTeams, Based on KrabsETW by microsoft) : https://github.com/threathunters-io/bluekrabsetw
        - SealighterTI (Threat-Intelligence ETW Provider) : https://github.com/pathtofile/SealighterTI
        - TiEtwAgent (Detect Memory injection based on ETW-TI) : https://github.com/xuanxuan0/TiEtwAgent
        - PyWinTrace (ETW python Library) : https://github.com/fireeye/pywintrace
        - EtwExplorer (View ETW Providers Manifest) : https://github.com/zodiacon/EtwExplorer
        - TelemetrySourcerer (enumerate and disable common sources of telemetry used by AV/EDR, Including ETW , User-ModeHooks, Kernel Callbacks) : https://github.com/jthuraisamy/TelemetrySourcerer
        - ETW Resources
            - Contains resources to learn and understand EVTX/ETW (Event Tracing for Windows) : https://github.com/nasbench/EVTX-ETW-Resources
    - KERNEL CALLBACKS -
        - Elastic
        - Sysmon
        - TelemetrySourcerer (enumerate and disable common sources of telemetry used by AV/EDR, Including ETW , User-ModeHooks, Kernel Callbacks) : https://github.com/jthuraisamy/TelemetrySourcerer
    - Capa - Capabilities Scanning
    - Trace API calls - TinyTracer
        - https://github.com/hasherezade/tiny_tracer
- Collect Windows Telemetry for Maldev
    - Collects telemetry like , ETW, ETW-TI, Kernel Callbacks, Hooks, Callstacks, Loaded DLLs, PEB) : https://github.com/dobin/RedEdr (Check other projects by author)
- **Free Trials EDR/AV Products**
    - Microsoft Defender For Endpoint
        - https://medium.com/@hackenbacker/creating-a-defender-for-endpoint-lab-for-free-695044b75bd6
        - https://learn.microsoft.com/en-us/defender-endpoint/defender-endpoint-trial-user-guide
    - Sophos XDR (trial)
    - Elastic EDR
        - https://github.com/sherifabdlnaby/elastdocker
        - [https://otterhacker.github.io/Malware/Elastic EDR.html](https://otterhacker.github.io/Malware/Elastic%20EDR.html)
        - https://github.com/peasead/elastic-container
        - https://www.youtube.com/watch?v=1luhjL7TN9U
    - TrendMicro
    - McAfee MVISION
    - Avast
    - openEDR - Comodo Free EDR
    - Wazuh : https://github.com/wazuh/wazuh
- Open Source EDRs
    - RedEDR : https://github.com/dobin/RedEdr
    - SimpleEDR - Manual DLL Hooking to find Detection Opportunity : https://github.com/Helixo32/SimpleEDR
    - CrimsonEDR : [https://github.com/Helixo32/CrimsonEDR](https://github.com/Helixo32/CrimsonEDR/tree/main)
    - OpenEDR : https://github.com/ComodoSecurity/openedr/
    - InjDrv :  https://github.com/wbenny/injdrv
    - MyDumbEDR : https://github.com/sensepost/mydumbedr
    - BestEDROfTheMarket : https://github.com/Xacone/BestEdrOfTheMarket
    - JonMon : https://github.com/jsecurity101/JonMon
    - SylantStrike : https://github.com/CCob/SylantStrike
    - Write your own EDR
        - https://blog.whiteflag.io/blog/from-windows-drivers-to-a-almost-fully-working-edr/
        - https://youtube.com/playlist?list=PLc2_LEyTNutFkUliQMTZ_FHl8kNx3f5-E&si=8kHcC_FIxccHBR5H
        - https://sensepost.com/blog/2024/sensecon-23-from-windows-drivers-to-an-almost-fully-working-edr/
- Open Source EDRs Comparison by [@dobin](https://github.com/dobin)
    
    ![Open-Source-EDR-Comparison.png](https://github.com/An0nUD4Y/AV-EDR-Lab-Environment-Setup/blob/main/Images/Open-Source-EDR-Comparison.png)
    

- Process Memory Scanners
    - PE-sieve : https://github.com/hasherezade/pe-sieve
    - Moneta : https://github.com/forrest-orr/moneta
    - YapScan : https://github.com/fkie-cad/yapscan
    - MalMemDetect : https://github.com/waldo-irc/MalMemDetect
    - Patriot : https://github.com/joe-desimone/patriot
    - Hunt-Sleeping-Beacons : https://github.com/thefLink/Hunt-Sleeping-Beacons
    - YaraMemoryScanner : https://github.com/BinaryDefense/YaraMemoryScanner
    - Cobalt Strike Beacon Detection Specific Scanners
        - BeaconEye : https://github.com/CCob/BeaconEye
        - BeaconHunter : https://github.com/3lp4tr0n/BeaconHunter
    - EtwTi-FluctuationMonitor - Doing VirtualAlloc(RWX) changes CFG bitmap accordingly and then after VirtualAlloc(RW) CFG stays the same :  https://github.com/jdu2600/EtwTi-FluctuationMonitor
    - TiEtwAgent (Detect Memory injection based on ETW-TI) : https://github.com/xuanxuan0/TiEtwAgent

- Signature Detection Bypass
    - ThreatCheck : [https://github.com/PACHAKUTlQ/ThreatCheck](https://github.com/PACHAKUTlQ/ThreatCheck?tab=readme-ov-file)
    - AvRed : https://github.com/dobin/avred



## AV/EDR Internals/ Telemetry/Benchmarking/Working

- EDR Internals
    - Matt Hand - Evading EDR book
    - How EDR Works (The Anti-EDR Compedium) : https://blog.deeb.ch/posts/how-edr-works/
- EDR Internals / Working Talks
    - https://youtu.be/SYM4i474JqM?si=ak5fBhcMmHxsopUn
    - https://youtu.be/CKfjLnEMfvI?si=2iiKBt1El9PGnhEt
    - https://www.youtube.com/live/VwpTyS7l5yo?si=djCZpKyWHGm8042-
    - https://youtu.be/vdYdKmgm20U?si=KIUNis9VrO4clSqF
    
- EDR Telemetry - Various EDR Telemetry : https://github.com/tsale/EDR-Telemetry
    - https://www.edr-telemetry.com/
    - EDR Telemetry Spreadsheet : https://docs.google.com/spreadsheets/u/1/d/1ZMFrD6F6tvPtf_8McC-kWrNBBec_6Si3NW6AoWf3Kbg/htmlview
- Defender Harvester : https://github.com/olafhartong/DefenderHarvester
- EDR Hooks Lists : https://github.com/Mr-Un1k0d3r/EDRs
    - HookDetector (Detect all hooked APIs) : https://github.com/matterpreter/OffensiveCSharp/tree/master/HookDetector
- Polonium : A tool from Modern Initial Access and Evasion Tactics course by Binary-Offensive (@mariuszbit). https://github.com/sponsors/mgeeky
- EDR Hooks Telemetry
    
    <img src="https://github.com/An0nUD4Y/AV-EDR-Lab-Environment-Setup/blob/main/Images/EDR-Hooks-Telemetry.png" alt="EDR-Hooks-Telemetry" width="500"/>
    
    - Taken from : https://github.com/helviojunior/hookchain/blob/main/HookChain_en_v1.5.pdf
- Gartner’s Magic Quadrant for EDR Platforms
  
    <img src="https://github.com/An0nUD4Y/AV-EDR-Lab-Environment-Setup/blob/main/Images/Gartner's-Magic-Quadrant.png" alt="Gartner's-Magic-Quadrant" width="500"/>
    
    - Taken From : https://github.com/helviojunior/hookchain/blob/main/HookChain_en_v1.5.pdf


## Credits
- Thanks to MaldevAcademy Discord Members for initial List
- Thanks to [@dobin](https://github.com/dobin) , For Providing a list of more resources and EDR Comparison table.
