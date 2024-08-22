# crkbd-cherry-v3-build

My journey down the rabbit hole.  
Building from [foostan's archived V3 release](https://github.com/foostan/crkbd/releases/tag/v3-final)

## Check List:
- [ ] [Make parts list](#parts-list)
  - [ ] [Building and ordering the PCB](#building-and-ordering-the-pcb)
- [ ] [Install/Configure QMK](#installconfigure-qmk)
- [ ] [Compile/Flash Firmware](#compileflash-firmware)
- [ ] [Prepare the OLEDS](#prepare-oleds)
- [ ] [Prepare the PCB](#prepare-pcb)
- [ ] [Solder PCB top components](#solder-pcb-top-components)
- [ ] [Solder pro-micro](#solder-pro-micro)
- [ ] [Solder OLEDs](#solder-oleds)
- [ ] [Solder diodes](#solder-diodes)
- [ ] [Solder hot-swaps](#solder-hot-swaps)
- [ ] [Solder under-glow leds](#solder-under-glow-leds)
- [ ] [Solder per-key leds](#solder-per-key-leds)
- [ ] [Mount the case](#mount-the-case)

## Parts list

- [ ] 1x  Corne PCB [Printed on JLCPCB](https://jlcpcb.com/) - $27
- [ ] 1x  Corne Case [Laser cut mine on Brazil](https://www.acrilicos60.com.br/)
- [ ] 42x Keycaps - 1u x 40, 1.5u x 2
- [ ] 2x  [Pro Micro ATmega32U4 5V/16MHz Module controller Mega32U4 Mini leonardo for Arduino with the bootloader](https://www.aliexpress.com/item/32768308647.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 2x  [OLED 128X32 OLED Display Module 0.91" IIC Communicate for ardunio](https://www.aliexpress.com/item/32777216785.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 42x [Kailh Hot-swappable PCB Socket Sip For Mechanical Keyboard](https://www.aliexpress.com/item/4001051840976.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 42x [SMD diodes 1N4148 SOD-123](https://www.aliexpress.com/item/32916398082.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 1M  [Round Copper Wire 0.5mm](https://www.aliexpress.com/item/4000781904492.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 4x  [2.54mm Pin Header Female Single Row 40](https://www.aliexpress.com/item/32817226478.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 2x  [PJ320D 3.5MM Headphone TRRS Jack Socket Female Connector](https://www.aliexpress.com/item/32785315917.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 1x  [1m 4 pole Stero audio cable Car AUX MP3/MP4 3.5mm male to male](https://www.aliexpress.com/item/32459681560.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 2x  [Micro Switch Push Button 3.5X6.0X4.3mm 1136-4.3 DIP Black](https://www.aliexpress.com/item/1068908059.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 42x [Holy Pandas switches](https://www.aliexpress.com/item/1005001465063863.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 24x [Screws M2 6mm](https://www.aliexpress.com/item/32661182311.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 10x [Spacers M2 7mm](https://www.aliexpress.com/item/32970573343.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 4x  [Spacers M2 10mm](https://www.aliexpress.com/item/32970573343.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 42x [Leds SK6812-mini-E](https://www.aliexpress.com/item/4000476037223.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 12x [Leds ws2812b](https://www.aliexpress.com/item/4000750610574.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)

## Building and ordering the PCB
**Convert archived V3 KiCad project files to Gerber files**  
[JLCPCB - How to generate Gerber and Drill files in KiCAD 8](https://jlcpcb.com/help/article/how-to-generate-gerber-and-drill-files-in-kicad-8)

**Order the PCB from JLCPCB**  
[GERBER Files](./GERBER-v3-cherry.zip)


