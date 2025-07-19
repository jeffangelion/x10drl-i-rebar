# x10drl-i-rebar
ROM image for Supermicro X10DRL-i (SYS-6018R-MTR) that is patched to enable PCI-e ReBAR.

Included files:
+ X10DRL.ROM - Patched ROM image (via MMTool v5.00.0007)

Files used to patch the rom (also included):
+ ReBarDxe.ffs - Resizeable BAR DXE Driver v0.3 from @xCuri0 on GitHub - https://github.com/xCuri0/ReBarUEFI

Files left for historical purposes (since X10DRL-i already support NVMe boot)
+ NvmExpressDxe_5.ffs - NVMe DXE Driver from Ethanial on WinRaid - https://winraid.level1techs.com/t/small-nvmexpressdxe-driver/32453

Instructions for use:
1. Simply flash the ROM on to your board and you are good to go.
2. To set the maximum BAR size, use the ReBarState tool from @xCuri0. If you do not do this, ReBar will not work correctly.

Fun facts:
+ PciBus module volume and index: `01.7D`
