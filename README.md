# Ghoul TKL PCB

A modern replacement PCB for Filco TKLs, adding support for PCB-mount stabilizers and popular alternate layouts.
In-switch backlight LEDs are also supported.

[Preview the design on KiCanvas](https://kicanvas.org/?github=https://github.com/chillKB/ghoulTKL)

![image](img/pcb_bottom.jpg)

Designed by [chill](https://github.com/chillKB).

## Features
- Confirmed to fit in Filco Majestouch 2 and 3 TKLs,
**unconfirmed** support for additional cases including Majestouch 1 and Cooler Master QuickFire Rapid TKL
(QuickFire TKL in-switch indicator LEDs not supported)
- Powered by STM32F072 MCU, supports QMK (and VIA) firmware
- PCB-mount stabilizer support (requires plate with proper cutouts, sample plate files are provided)
- Multi-layout (see below)
- Backlighting with in-switch single-color LEDs
- Alps switch support (untested, requires Alps plate not provided)

![image](img/keyboard-layout.png)

## Ordering

This PCB is permissively licensed so anyone is welcome to use it
for personal or commercial purposes—see the `LICENSE` file for details.
Please note that no warranty is provided. If you do use it, I would love to hear from you!

I will not provide specific ordering instructions,
but if you wish to use JLCPCB, [this KiCad extension](https://github.com/Bouni/kicad-jlcpcb-tools) should make things easy.
Fabs also provide documentation for how to export production files on their websites.
As this project ages, some part numbers will go out of date and you will need to replace them.

It may also be possible to order a PCB from nickheller if he has any in stock.
If you are interested in owning one without having to order from a PCB fab, you may reach out to him (hickneller) in the MechKeys Discord.

## Additional Components
- 1x OEM JST-PH 5-pin to USB cable (comes with keyboard)
- 2x 3mm indicator LEDs
- 2x [LED spacers](https://octopart.com/7362-keystone-87956)
- 89x 1.8mm backlight LEDs (optional)

## Firmware

VIA compatible firmware (`chill_ghoul_via.bin`) is available from the [VIA website](https://www.caniusevia.com/docs/download_firmware).
If preferred, firmware without VIA support can be downloaded from [QMK Configurator](https://config.qmk.fm/#/chill/ghoul/LAYOUT_tkl_ansi).
Advanced users are welcome to [compile their own](https://github.com/qmk/qmk_firmware/tree/master/keyboards/chill/ghoul).

To flash the keyboard, you can use [QMK Toolbox](https://github.com/qmk/qmk_toolbox).
For beginners, refer to [this guide](https://www.youtube.com/watch?v=fuBJbdCFF0Q).
To put the PCB into bootloader mode, hold the "BOOT" button while tapping the "RST" button once (you may then release "BOOT").
If working firmware is already flashed, you can also enter bootloader mode by holding the escape key while plugging in the keyboard,
or pressing a `QK_BOOT` key, if you have one in your modified keymap.

## Acknowledgements

Special thanks to nickheller for commissioning this PCB and agreeing to open-source it.

Additionally, thanks/credit to
- [KiCad EDA](https://www.kicad.org/)
- [QMK Firmware](https://qmk.fm/)
- [Keyboard Layout Editor](https://www.keyboard-layout-editor.com/)
- kkatano for the [Yurei](https://github.com/kkatano/yurei) PCB, from which this project borrows dimensions needed for physical compatibility
- bpiphany for the Phantom PCB, which is the original Filco replacement PCB
- ebastler for [marbastlib](https://github.com/ebastler/marbastlib), my preferred keyboard library for KiCad
- Zykrah for [tools](https://zykrah.me/) and [references](https://guide.zykrah.me/) that I use often