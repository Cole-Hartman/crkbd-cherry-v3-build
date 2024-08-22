# crkbd-cherry-v3-build

My journey down the rabbit hole.  
Based off [foostan's archived V3 Corne release](https://github.com/foostan/crkbd/releases/tag/v3-final)  
Using [foostan](https://github.com/foostan/crkbd/blob/main/docs/corne-cherry/v3/buildguide_en.md)'s and [rafaeldelboni](https://github.com/rafaeldelboni/buildlogs/blob/main/crkbd-v3.md#compileflash-firmware)'s build guides

**You should follow this guide if you...**  
- Want a CRKBD V3 3x6 Cherry hot-swap keyboard
- Includes OLED
- No RBG or Bluetooth in this build

## Progress:
- [ ] [Make parts list](#parts-list)
  - [X] [Building and ordering the PCB](#building-and-ordering-the-pcb)
- [ ] [Install/Configure QMK](#installconfigure-qmk)
- [ ] [Compile/Flash Firmware](#compileflash-firmware)
- [ ] [Prepare the OLEDS](#prepare-oleds)
- [ ] [Prepare the PCB](#prepare-pcb)
- [ ] [Solder PCB top components](#solder-pcb-top-components)
- [ ] [Solder pro-micro](#solder-pro-micro)
- [ ] [Solder OLEDs](#solder-oleds)
- [ ] [Solder diodes](#solder-diodes)
- [ ] [Solder hot-swaps](#solder-hot-swaps)
- [ ] [Solder per-key leds](#solder-per-key-leds)
- [ ] [Mount the case](#mount-the-case)

## Parts list
**Keyboard**
| Name | Count | Details | Price |
|:-|:-|:-|:-|
| PCB | 1x | [Corne PCB Printed using JLCPCB](https://jlcpcb.com/) | $40 |
| Top Plate 1.5-3mm | 2x |  Printed at school - [.stl file]() | |
| Top Plate | 2x | Printed at school - [.stl file]() | |
| OLED Cover | 2x | |
| Keycaps | 42x | | $ |
| Switches | 42x | | $ |
| OLED | 2x | [OLED 128X32 OLED Display Module 0.91" IIC Communicate for ardunio](https://www.aliexpress.com/item/32777216785.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA) | $0.30 |
| DIODES | 100x | [1N4148W T4 SOD-123](https://www.aliexpress.us/item/2251832735176193.html?spm=a2g0o.cart.0.0.624d38dayf8uXk&mp=1&gatewayAdapt=glo2usa) | $1 |
| Hot Swaps | 50x | [Kailh Hot-swappable PCB socket Hot Plug for Gateron Outemu Cherry MX Switches Mechanical Keyboard](https://www.aliexpress.us/item/2255800865526224.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA&gatewayAdapt=glo2usa4itemAdapt) | $8 |
| Microcontroller | 2x | [TZT Pro Micro ATmega32U4 5V 16MHz Original Chip Type-C](https://www.aliexpress.us/item/2251832581993895.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA&gatewayAdapt=glo2usa4itemAdapt) | $3 |
| TRRS Cable 4 pole | 1x | [Rallonge Jack 3.5mm 4 3 Pole TRRS to TRRS](https://www.aliexpress.us/item/3256805991501373.html?spm=a2g0o.productlist.main.1.10596d99xhZTwL&algo_pvid=9dde26da-8622-45dc-8815-b85b16e86c14&algo_exp_id=9dde26da-8622-45dc-8815-b85b16e86c14-0&pdp_npi=4%40dis%21USD%214.45%210.99%21%21%2131.54%217.01%21%402101c5b117242987081857098e0582%2112000036149303822%21sea%21US%212778608228%21ABX&curPageLogUid=1JhzGCK9fNj9&utparam-url=scene%3Asearch%7Cquery_from%3A) | $3 |
| Screws | 50x | For case - [M2.0 6mm](https://www.aliexpress.us/item/3256805432431543.html?spm=a2g0o.productlist.main.7.71d74614yyKWon&algo_pvid=6ee9a92e-cdc7-460a-af3b-ac2b0e62eb9a&aem_p4p_detail=202408212153242149051534836220006711131&algo_exp_id=6ee9a92e-cdc7-460a-af3b-ac2b0e62eb9a-3&pdp_npi=4%40dis%21USD%211.02%210.96%21%21%217.24%216.81%21%402103094f17243024043121319e1b2a%2112000033767212213%21sea%21US%212778608228%21ABX&curPageLogUid=qknRdn84mFma&utparam-url=scene%3Asearch%7Cquery_from%3A&search_p4p_id=202408212153242149051534836220006711131_1) | $1 |
| Spacer M2 7.5mm | 10x | For case - | $ |
| Spacer M2 9mm | 10x | For case - | $ |
| Rubber feet | | | |
| Round Copper Wire | 1M | [New polyurethane enameled round copper wire 0.55mm](https://www.aliexpress.us/item/2255800595589740.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA&gatewayAdapt=glo2usa4itemAdapt) | $ |

**Tools**
| Name | Count | Details | Price |
|:-|:-|:-|:-|
| Soldering Kit | 1x | [Kit](https://www.amazon.com/Soldering-Kit-Temperature-Desoldering-Electronics/dp/B07GTGGLXN/ref=sr_1_5?crid=38MPRDWM5JBD2&dib=eyJ2IjoiMSJ9.bN2ArPTpgQRijAd577UAx2lb0lxJe9OJfvIrJ6Bhu94uZRdZ0QiOR1-KaozOEwvqRFJO6PmfGYfSgNX8FCBUUr7tF74wEkvH2oPiK_vOUmZ4kcyFUs1GxnhlBGenUVRiocpGicXoasYk4pn2j1hmV_uITJfg-8F86EbmyExxmN_qOA8LUu2XNpdrcps8dFHy3x6Vsxs0nPWFvIyXwVel8fIs0YaS7FLhzvMPE6c5Bm9Sv0gDM9kTUX6UC23l9WSCI8h0VyGKKpOtbs7h1YVjf3JVk5e2DfrIKZ26WudrKVE.zCvhrofR5D4P22aA3xQqujJoRpbFraz-JM9WFvdwxwk&dib_tag=se&keywords=soldering+kit&qid=1724294807&sprefix=soldering+ki%2Caps%2C181&sr=8-5#customerReviews) | $6.5 (split w/ friend) |

---

- [ ] 4x  [2.54mm Pin Header Female Single Row 40](https://www.aliexpress.com/item/32817226478.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 2x  [PJ320D 3.5MM Headphone TRRS Jack Socket Female Connector](https://www.aliexpress.com/item/32785315917.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 2x  [Micro Switch Push Button 3.5X6.0X4.3mm 1136-4.3 DIP Black](https://www.aliexpress.com/item/1068908059.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 10x [Spacers M2 7mm](https://www.aliexpress.com/item/32970573343.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 4x  [Spacers M2 10mm](https://www.aliexpress.com/item/32970573343.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 42x [Leds SK6812-mini-E](https://www.aliexpress.com/item/4000476037223.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- [ ] 12x [Leds ws2812b](https://www.aliexpress.com/item/4000750610574.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)

## Building and ordering the PCB
**Convert archived V3 KiCad project files to Gerber files**  
[JLCPCB - How to generate Gerber and Drill files in KiCAD 8](https://jlcpcb.com/help/article/how-to-generate-gerber-and-drill-files-in-kicad-8)

**Order the PCB from JLCPCB**  
[GERBER Files](./GERBER-v3-cherry.zip)


