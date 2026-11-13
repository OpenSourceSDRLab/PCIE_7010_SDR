# Third-party notices

This repository and its release files contain work by OpenSourceSDRLab together with third-party software. The Apache License 2.0 in [LICENSE](LICENSE) applies **only** to the files created by OpenSourceSDRLab:

- `docs/`, `hardware/`, `images/`, `README.md`, `NOTICE.md`

The firmware in the Releases is third-party software and keeps its own licences:

| Component | Files | Owner | Licence |
|---|---|---|---|
| PlutoSDR firmware v0.38 (build system, HDL design, device trees, scripts), adapted to this board | `flash_firmware/pluto.dfu`, `boot.bin`, `uboot-env.dfu` and `SD_img/` in `PCIE_7010_SDR_firmware_v0.38.zip` | Analog Devices, Inc. | as stated in the PlutoSDR firmware sources (`LICENSE.md` of the Analog Devices plutosdr-fw project) |
| Linux kernel | inside `pluto.dfu` and `SD_img/uImage` | the Linux kernel authors | GPL-2.0 |
| U-Boot | inside `boot.bin` / `BOOT.bin`, used with `uboot-env.dfu` and `uEnv.txt` | the U-Boot authors | GPL-2.0+ |
| Buildroot root file system (BusyBox, libiio, other packages) | inside `pluto.dfu` and `SD_img/uramdisk.image.gz` | the respective authors | each package's own licence (mostly GPL / LGPL / BSD / MIT) |
| FPGA bitstream | inside `pluto.dfu` and `BOOT.bin` | Analog Devices, Inc. and Xilinx, Inc. / AMD | built from the Analog Devices HDL and Xilinx IP |
| First-stage boot loader | `fsbl.elf`, and inside `boot.bin` / `BOOT.bin` | Xilinx, Inc. / AMD | Xilinx/AMD licence terms |

**Source code.** The firmware is a build of the Analog Devices PlutoSDR firmware v0.38 (<https://github.com/analogdevicesinc/plutosdr-fw>, tag `v0.38`) with changes for this board. For three years from the date you received the firmware, OpenSourceSDRLab will provide the complete corresponding source code of the GPL and LGPL components in the firmware on request: write to support@opensourcesdrlab.com.

Software that is **not** included and must be obtained from the vendors:

- PlutoSDR USB drivers for Windows (they also install `dfu-util`) and IIO Oscilloscope: Analog Devices, <https://wiki.analog.com/university/tools/pluto/drivers/windows> and <https://wiki.analog.com/resources/tools-software/linux-software/iio_oscilloscope>
- Network driver for the Realtek RTL8111F PCIe Gigabit Ethernet controller (needed only if the operating system does not include one): Realtek, <https://www.realtek.com/Download/List?cate_id=584>
- Vivado (Lab Edition is enough) for flash recovery: AMD/Xilinx, <https://www.xilinx.com/support/download.html>

"Analog Devices", "AD9363", "ADALM-PLUTO", "PlutoSDR", "Xilinx", "Zynq", "Vivado" and "Realtek" are trademarks of their respective owners. They are used here only to describe compatibility and do not imply endorsement.
