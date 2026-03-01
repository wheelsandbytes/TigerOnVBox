VM data dump obtained using:
```shell
{ echo "--- VM INFO ---"; VBoxManage showvminfo "Tiger"; echo "--- EXTRADATA ---"; VBoxManage getextradata "Tiger" enumerate; } > vm-dump.txt
```

```shell
--- VM INFO ---
Name:                        Tiger
Groups:                      /
Guest OS:                    Mac OS X (32-bit)
UUID:                        c37716f8-b0af-4009-91a2-cb5317c02194
Config file:                 /Users/wheelsandbytes/VirtualBox VMs/Tiger/Tiger.vbox
Snapshot folder:             /Users/wheelsandbytes/VirtualBox VMs/Tiger/Snapshots
Log folder:                  /Users/wheelsandbytes/VirtualBox VMs/Tiger/Logs
Hardware UUID:               c37716f8-b0af-4009-91a2-cb5317c02194
Memory size:                 2048MB
Page Fusion:                 disabled
VRAM size:                   16MB
CPU exec cap:                100%
HPET:                        enabled
CPUProfile:                  Intel Pentium 4 3.00GHz
Chipset:                     ich9
Firmware:                    EFI32
Number of CPUs:              1
PAE:                         enabled
Long Mode:                   disabled
Triple Fault Reset:          disabled
APIC:                        enabled
X2APIC:                      disabled
Nested VT-x/AMD-V:           enabled
CPUID Portability Level:     0
CPUID overrides:             Leaf no.      EAX      EBX      ECX      EDX
                             00000000/000  00000004 756e6547 6c65746e 49656e69
                             00000001/000  00000f43 00020800 fbffffff ffffffff
                             80000001/000  00000000 00000000 ffffffff ffffffff
Boot menu mode:              message and menu
Boot Device 1:               Floppy
Boot Device 2:               DVD
Boot Device 3:               HardDisk
Boot Device 4:               Not Assigned
ACPI:                        enabled
IOAPIC:                      enabled
BIOS APIC mode:              APIC
Time offset:                 0ms
BIOS NVRAM File:             /Users/wheelsandbytes/VirtualBox VMs/Tiger/Tiger.nvram
RTC:                         UTC
Hardware Virtualization:     enabled
Nested Paging:               enabled
Large Pages:                 enabled
VT-x VPID:                   enabled
VT-x Unrestricted Exec.:     enabled
Paravirt. Provider:          Default
Effective Paravirt. Prov.:   Minimal
State:                       powered off (since 2026-02-28T23:39:45.340000000)
Graphics Controller:         VBoxVGA
Monitor count:               1
3D Acceleration:             disabled
2D Video Acceleration:       disabled
Teleporter Enabled:          disabled
Teleporter Port:             0
Teleporter Address:          
Teleporter Password:         
Tracing Enabled:             disabled
Allow Tracing to Access VM:  disabled
Tracing Configuration:       
Autostart Enabled:           disabled
Autostart Delay:             0
Default Frontend:            
VM process priority:         default
Storage Controller Name (0):            SATA
Storage Controller Type (0):            IntelAhci
Storage Controller Instance Number (0): 0
Storage Controller Max Port Count (0):  30
Storage Controller Port Count (0):      2
Storage Controller Bootable (0):        on
SATA (0, 0): /Users/wheelsandbytes/VirtualBox VMs/Tiger/Tiger.vdi (UUID: 61f58490-7ce8-40ca-8067-78d589d3747e)
SATA (1, 0): Empty (ejected)
NIC 1:                       MAC: 0800270B8B48, Attachment: NAT, Cable connected: on, Trace: off (file: none), Type: 82545EM, Reported speed: 0 Mbps, Boot priority: 0, Promisc Policy: deny, Bandwidth group: none
NIC 1 Settings:  MTU: 0, Socket (send: 64, receive: 64), TCP Window (send:64, receive: 64)
NIC 2:                       disabled
NIC 3:                       disabled
NIC 4:                       disabled
NIC 5:                       disabled
NIC 6:                       disabled
NIC 7:                       disabled
NIC 8:                       disabled
NIC 9:                       disabled
NIC 10:                      disabled
NIC 11:                      disabled
NIC 12:                      disabled
NIC 13:                      disabled
NIC 14:                      disabled
NIC 15:                      disabled
NIC 16:                      disabled
NIC 17:                      disabled
NIC 18:                      disabled
NIC 19:                      disabled
NIC 20:                      disabled
NIC 21:                      disabled
NIC 22:                      disabled
NIC 23:                      disabled
NIC 24:                      disabled
NIC 25:                      disabled
NIC 26:                      disabled
NIC 27:                      disabled
NIC 28:                      disabled
NIC 29:                      disabled
NIC 30:                      disabled
NIC 31:                      disabled
NIC 32:                      disabled
NIC 33:                      disabled
NIC 34:                      disabled
NIC 35:                      disabled
NIC 36:                      disabled
Pointing Device:             USB Mouse
Keyboard Device:             USB Keyboard
UART 1:                      disabled
UART 2:                      disabled
UART 3:                      disabled
UART 4:                      disabled
LPT 1:                       disabled
LPT 2:                       disabled
Audio:                       enabled (Driver: CoreAudio, Controller: AC97, Codec: STAC9700)
Audio playback:              enabled
Audio capture:               enabled
Clipboard Mode:              disabled
Drag and drop Mode:          disabled
VRDE:                        disabled
OHCI USB:                    enabled
EHCI USB:                    disabled
xHCI USB:                    disabled

USB Device Filters:

<none>

Bandwidth groups:  <none>

Shared folders:<none>

Capturing:                   active
Capture audio:               not active
Capture screens:             0
Capture file:                /Users/wheelsandbytes/VirtualBox VMs/Tiger/Tiger.webm
Capture dimensions:          1024x768
Capture rate:                512kbps
Capture FPS:                 25kbps
Capture options:             vc_enabled=true,ac_enabled=false,ac_profile=med

Guest:

Configured memory balloon size: 0MB

--- EXTRADATA ---
Key: GUI/LastCloseAction, Value: PowerOff
Key: GUI/LastNormalWindowPosition, Value: 416,53,1024,789
Key: GUI/RestrictedRuntimeDevicesMenuActions, Value: HardDrives
Key: GUI/RestrictedRuntimeMachineMenuActions, Value: SaveState,PowerOff
Key: GUI/ScaleFactor, Value: 2
Key: GUI/StatusBar/IndicatorOrder, Value: HardDisks,OpticalDisks,FloppyDisks,Network,USB,SharedFolders,Display,VideoCapture,Features,Mouse,Keyboard
Key: VBoxInternal/Devices/efi/0/Config/DmiBIOSVersion, Value: EFI32..Virtual.Box
Key: VBoxInternal/Devices/efi/0/Config/DmiUseHostInfo, Value: 0
Key: VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC, Value: 1
```
