---
theme: seriph
background: /assets/background-2.jpg
# some information about your slides (markdown enabled)
title: Welcome to Vienna MKB Meetup 2024
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: relative
layout: cover
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# take snapshot for each slide in the overview
overviewSnapshots: true
fonts:
  # like font-family in css, you can use `,` to separate multiple fonts for fallback
  sans: 'Helvetica Neue,Robot'
  # mark 'Helvetica Neue' as local font
  local: 'WienerMelangeVF'
---

# Vienna 
# Mechanical Keyboard Meetup 2024

<div class="absolute bottom-2 right-2 text-xs bg-black bg-opacity-30 px-2 py-1 rounded">
  <a 
    href="https://keyboardrenderkit.readthedocs.io" 
    target="_blank" 
    alt="Keyboard Render Kit" 
    title="Open Keyboard Render Docs"
    class="text-gray text-jb-medium hover:text-blue-200 transition-colors duration-200"
  >
    Image by Keyboard Render Kit | © 2024 KRK
  </a>
</div>


<style>

@font-face {
  font-family: WienerMelange;
  src: url('/fonts/WienerMelangeVF.woff2');
}
@font-face {
  font-family: JetBrainsMonoMedium;
  src: url('/fonts/JetBrainsMono-Medium.woff2')
}

.text-jb-medium {
  font-family: JetBrainsMonoMedium;
}
h1:first-of-type {
  font-size: 4.75em;
  font-family: WienerMelange;
  will-change: background-position;
  background:
    radial-gradient(100% 58% at top   ,red   99%, white) calc(0*100%/3) 0,
    radial-gradient(100% 58% at bottom,white 99%,red  ) calc(3*100%/3) 0,
    radial-gradient(100% 58% at top   ,red   99%,white) calc(6*100%/3) 0,
    radial-gradient(100% 58% at bottom,white 99%,red  ) calc(9*100%/3) 0;
  background-size:50% 100%;
  background-repeat:no-repeat;
  -webkit-background-clip:text;
  color:transparent;
  background-clip:text;
  display:inline-block;
  padding:20px;
  font-size:100px;
  font-weight:bold;
  animation: move 7s infinite linear;}

h1 {
  position: relative;
  font-family: 'Monospaced';
}

h1:last-of-type {
  font-size: 2.9em !important;
  font-family: 'JetBrainsMonoMedium';
}

h1:last-of-type::after {
  content: '';
  display: inline-block;
  width: 0.35em;  /* adjust width to match your font size */
  height: 0.8em; /* adjust height to match your font size */
  background-color: #F9F6EE;
  animation: blink 1s steps(2) infinite;
}

@keyframes move {
  to {
    background-position:
       calc(-6*100%/3) 0,
       calc(-3*100%/3) 0,
       calc(0*100%/3) 0,
       calc(3*100%/3) 0;
  }
}
@keyframes blink {
  0%, 49% {
    opacity: 1;
  }
  50%, 100% {
    opacity: 0;
  }
}
</style>

---
layout: center
---
# Why Keyboard Meetups?
Keyboard meetups transform an online hobby into a vibrant, tangible community experience

<v-clicks>

🤝 Community Building

🖐️ Hands-on Experience

🎪 Show & Tell

💫 Trading & Shopping

📚 Knowledge Sharing

🔊 Sound Tests

</v-clicks>
---
---

# Keyboard: The Bigger Picture

- Bottom case / plate
- PCB
- Mid plate
- Switches
- Top case / plate
- Keycaps
- Stabilizers

<v-clicks>

[Keyboard University](https://www.keyboard.university/)  👨‍🎓

</v-clicks>

 <img class="absolute right-30px top-100px" src="/images/keyboard-render.png" width="700" alt="3D keybord layrs render">

<div class="absolute bottom-2 right-2 text-xs bg-black bg-opacity-30 px-2 py-1 rounded">
  <a 
    href="https://github.com/Frugivore8894" 
    target="_blank" 
    alt="Keyboard Render Kit" 
    title="Open Keyboard Render Docs"
    class="text-gray text-jb-medium hover:text-blue-200 transition-colors duration-200"
  >
    3D Render by Frugivore8894
  </a>
</div>

<!--1. Bottom case / acryllic plate / FR plate : Screw in PCB into it, can hold sound dampening material (EVA - Ethylene-vinyl acetate, Poron - Urethane material, PE - Polyethylene)
2. PCB (Printed Circuit Board) made of FR4 - base material made from a flame retardant epoxy resin and glass fabric composite.
3. Plate
4. Siwtches
      profiles: cherry mx compatible, low profile kailh chock/gateron,
      material: PBT, ABS, resin, metal, 
      process: dye sublimation, Reverse Dye-sublimation , double shot
      different patterns: clicky, linear, tactile, silent
      heaviness: spring rigidity : light / heavy
      types: mechanical, optical, HAL-effect
      mod: O-ring, film, lubrication

5. Stabilizers - mechanisms that keep the larger keys like Space, Shift, Enter, and Backspace in place and, for lack of a better word, stable. 
-->

---
transition: fade-out
---

# MCU and SoC <MarkerHardware/>

Microcontrollers and SoCs features

- CPU Core
- Memory systems
- USB / HID Connectivity
- Wireless features
- GPIO & Peripherals
- Reset & Power management
- Programming (ISP)

<img class="absolute right-150px top-100px" src="/images/sea-picro-pinout.png" width="380" alt="sea-picro pinout image">

<div
  v-motion
  :initial="{ x: 1100, y: 190 }"
  :enter="{ x: 50 }"
  :leave="{ y: 400 }"
>
<div class="absolute right-50px bottom-20px">
  <img width="120" src="/images/rp2040_MCU.png" alt="rp2040 image">
</div>

</div>
<!--
EEPROM (Electrically Erasable Programmable Read-Only Memory) is a type of non-volatile memory that retains data even when power is removed.

USB controller, Bluetooth Low Energy (BLE) controller

Interfacing with various peripherals such as analog-to-digital converters (ADCs), pulse-width modulation (PWM) controllers, I2C, and SPI.

ISP allows you to program a microcontroller while it's installed in the target system, without needing to remove the chip. 

Pinout is identical to the SparkFun Pro Micro

RX (Receive) and TX (Transmit) pins, which are fundamental to serial communication. UART stands for universal asynchronous receiver / transmitter :

SDA and SCL pins are part of the I2C:

ADC - analog-digital-converter

VCC(voltage common collector) and GND for power

MOSI (Master Out Slave In)

MISO (Master In Slave Out)

SCK (Serial Clock)

RAW - direct, unprocessed input/output pin (Debugging)

D- and D+ pins, which are essential for USB (Universal Serial Bus) communication.
-->

---
transition: slide-up
layout: center
---
# MCU and SoC: Top ones <MarkerHardware/>

<v-switch>
  <template #0> 

  1. **Atmega32u4**
      - 8-bit AVR RISC-based microcontroller
      - Budget-friendly, used in many keyboard projects
      - 32 KB of flash memory, 2.5 KB SRAM
      - 20 MHz clock speed

 </template>
  <template #1>

  2. **STM32F103**
     - 32-bit ARM Cortex-M3 microcontroller
     - High performance
     - 64 KB to 128 KB of flash memory, 20 KB to 64 KB SRAM
     - 72 MHz clock speed

  </template>

  <template #2>

  3. **RP2040**
     - 32-bit ARM Cortex-M0+ microcontroller
     - Developed by Raspberry Pi, gaining popularity
     - 264 KB of flash memory, 264 KB SRAM
     - 133 MHz clock speed

  </template>

  <template #3>

  4. **nRF52840**
     - 32-bit ARM Cortex-M4 microcontroller
     - Supports Bluetooth Low Energy (BLE)
     - 1 MB of flash memory, 256 KB SRAM
     - 64 MHz clock speed

  </template>
</v-switch>

---
transition: slide-up
layout: center
zoom: 0.9
---

# MCU and SoC: A Comparison <MarkerHardware/>
| **Feature** | **Atmega32u4** | **STM32F103** | **RP2040** | **nRF52840** |
|-------------|----------------|---------------|------------|--------------|
| Processor | 8-bit AVR | 32-bit ARM | 32-bit ARM | 32-bit ARM |
| Flash Memory | 32 KB | 64-128 KB | 264 KB | 1 MB |
| RAM | 2.5 KB | 20-64 KB | 264 KB | 256 KB |
| Speed | 20 MHz | 72 MHz | 133 MHz | 64 MHz |
| USB Support | Yes | Yes | Yes | Yes |
| Bluetooth LE | No | No | No | Yes |
| Peripherals | [ADC](https://en.wikipedia.org/wiki/Analog-to-digital_converter), [PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation) | [ADC](https://en.wikipedia.org/wiki/Analog-to-digital_converter), [PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation), [I²C](https://en.wikipedia.org/wiki/I%C2%B2C), [SPI](https://en.wikipedia.org/wiki/Serial_Peripheral_Interface) | [ADC](https://en.wikipedia.org/wiki/Analog-to-digital_converter), [PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation), [I²C](https://en.wikipedia.org/wiki/I%C2%B2C), [SPI](https://en.wikipedia.org/wiki/Serial_Peripheral_Interface) | [ADC](https://en.wikipedia.org/wiki/Analog-to-digital_converter), [PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation), [I²C](https://en.wikipedia.org/wiki/I%C2%B2C), [SPI](https://en.wikipedia.org/wiki/Serial_Peripheral_Interface) |
| 👥 Support | High | High | High | Moderate |
| 💸 Cost        | € | €€ | €€ | €€€ |

<!-- 
ADC - analog sensing, preasure, temperature, battery, audio inputs

PWM (Pulse-width modulation) RGB color intensity, haptic devices, motors, etc

I2C (Inter-Integrated Circuit) Communication with Peripherals:  EEPROM,RGB controllers, Sensors, audio controllers

SPI (Serial Peripheral Interface) serial communication protocol: hight speed data transfer, Display, Flash communication and storing, full duplex unline I2C

1. 4 euro
2. 9 euro
3. 9 euro
4. 10 euro 
-->
---
transition: slide-up
layout: two-cols-header
zoom: 1.2
---
# MCU and SoC: Boards <MarkerHardware/>
::left::

<v-clicks>

- [Pro Micro](https://learn.sparkfun.com/tutorials/pro-micro--fio-v3-hookup-guide/all)
- [Sea-Picro](https://github.com/joshajohnson/sea-picro)
- [Elite-C](https://deskthority.net/wiki/Elite-C)
- Elite-Pi
- Bluepill
- Blackpill
- Supermini ESP32
- [Supermini NRF52](https://github.com/joric/nrfmicro/wiki)
- [Nice!Nano](https://nicekeyboards.com/docs/nice-nano/)

</v-clicks>
::right::

<img  class="absolute right-290px bottom-150px" width="120" src="/images/nicenano-v2.png"/>
<img  class="absolute right-30px bottom-20px" width="280" src="/images/sea-picro-render.png"/>

<!--Pro Micro initially created by SparkFun as Arduino-compatible board. Open Source Hardware Association(Arduino, Adafruit Industries) . There tons of ProMicro footprint clones with either ATmega32U4 or RP2040.-->
---
layout: two-cols-header
---
# Firmware: The Features  <MarkerFirmware/>

::left::

<v-click>

**1. Core features**
- Matrix scanning
- Debounce
- HID bidirectional communication
- N-Key Rollover

</v-click>

<v-click at="+1">

**2. Advance features**
- Layers
- Macros
- Lighting control
- OLED/Display control
- Media controls
- MIDI

</v-click>

::right::

<v-click at="+1">

**3. User customization**

- Key remapping
- Tap dance
- Combos
- Hold/Tap

</v-click>

<v-click at="+1">

**4. Hardware managment**
- Peripheral control
- Power Management (Sleep/wake)
- Split keyboard communication
- BLE profiles
- EEPROM clearing
- Bootloader mode

</v-click>

<!-- 
Matrix scanning is the process of detecting which keys are currently pressed

Debounce: A lot  of things can interfere with key presses: noice signals, oxydized contacts

HID(human interface device) Talk with hidapi implementation

N-key rollover - reporting any number of key-presses at once.
-->
---
---
# Firmware: QMK <MarkerFirmware/>
<a href="https://qmk.fm/">
<LightOrDark>
  <template #dark><img class="absolute right-100px top-50px" src="/images/qmk-logo-dark.svg" height="150" width="150" alt="QMK project logo"></template>
  <template #light><img class="absolute right-100px top-50px" src="/images/qmk-logo-light.svg" height="150" width="150" alt="QMK project logo"></template>
</LightOrDark>
</a>

#### Pros
- **Large community**
- **AVR/8 Bit Support** (ATmega32U4, etc.)

- **Real-time keymap updating** ([VIA](https://www.caniusevia.com/), [VIAL](https://get.vial.today/), [remap-keys.app](https://remap-keys.app/), etc) ✨

#### Cons
- **Limited wireless support** (BLE: Adafruit Bluefruit LE SPI Friend only, BT2.1: RN-42)

- **Firmware build process is meh**

📝 License: GPL-2

⌨ Notable keyboards: ZSA (Voyager, Moonlander, ErgoDox), Nuphy



---
---
# Firmware: ZMK <MarkerFirmware/>

<a href="https://zmk.dev/">
  <img class="absolute right-130px bottom-80px" src="/images/zephyr_project_logo.png" width="100" alt="ZMK project logo">
  <img class="absolute right-100px top-80px" src="/images/zmk_logo.svg" height="150" width="130" alt="ZMK project logo">
</a>

#### Pros:
- **Built on the [Zephyr Framework](https://zephyrproject.org/)** ([1](https://zephyrproject.org/building-open-keyboards-with-zmk-zephyr/))
- **Rock solid Bluetooth support**
- **Bluetooth profiles support** 💻📱🖥️
- **Power-efficient** 🔋
- **Elegant firmware build** (GitHub Actions) 🔥
 
#### Cons:
- **32/64-bit platforms only**
- **Limited display support (OLED I2C)**

📝 License: MIT

⌨ Notable keyboards: Kinesis Advantage 360 Pro

---
---
# Firmware: RMK <MarkerFirmware/>

<a href="https://github.com/haobogu/rmk">
  <img class="absolute right-130px bottom-80px" src="/images/ferris.png" width="100" alt="ZMK project logo">
  <img class="absolute right-100px top-80px" src="/images/rmk-logo.png" width="200" alt="ZMK project logo">
</a>

#### Pros:
- Powered by [embassy](https://embassy.dev/)
- **Easy configuration through TOML**
- **Bluetooth support**
- **Power-efficient** 🔋
- **Straightforward build using Cargo** 📦
- **Built-in [Vial](https://get.vial.today/)**
 
#### Cons:
- **32/64-bit platforms only**
- **RGB, encoder and Display support is not there yet**
- **Small community**

📝 License: MIT
---
layout: two-cols-header
---
# Firmware: Other noticeable <MarkerFirmware/>

::left::

### KMK

#### Pros
- **Beginner-friendly (Circuit Python)** 🐍

- **Easy single file configuration**

#### Cons

- **32-bit platforms only**

📝 License: GPLv3

<img class="absolute left-70px bottom-50px" src="/images/kmk_logo.svg" width="200" alt="ZMK project logo">

::right::

<a href="https://bluemicro.jpconstantineau.com/">
  <img class="absolute top-140px right-70px" src="/images/bluemicro-logo.png" width="100" alt="ZMK project logo">
</a>

### BlueMicro

#### Pros

- [**Arduino framework**](https://www.arduinolibraries.info/architectures/nrf52)

- [**Arduino IDE/CLI building/flashing**](https://bluemicro.jpconstantineau.com/docs/)

#### Cons
- **Not active**

- **nRF52 Nordic family only** (32-bit ARM Cortex-M4F)

📝 License: BSD 3-Clause

---
layout: two-cols-header
---

<style>
.col-right {
 padding: 0 2em !important;
}
</style>

# Firmware Demo <MarkerFirmware/>

Build & Flash

::left::

#### AVR
```bash

# Flash only, build with QMK
 avrdude -v -c usbtiny -p m32u4 -U flash:w:your_firmware.hex:i
```

#### QMK
```bash

# QMK CLI
qmk flash -kb <keyboard> -km <keymap>
```

```bash

# QMK Docker Build only
./util/docker_build.sh <keyboard>:<keymap>
```

#### ZMK
 
```bash

# Commit you zmk-config folder for the GitHub Actions
# Or run it with the west tool
west build -b <keyboard>

# DFU enabled
west flash
```

::right::

#### RMK
```bash

# Simply `cago build` inside a keyboard config folder
cargo build

```

---
layout: two-cols-header
---

# Manufacturing & Parts Sourcing

### PCB / Plate
- Get / Design your KiCad schematics
- [Generate Gerber and drill files](https://jlcpcb.com/help/article/how-to-generate-gerber-and-drill-files-in-kicad-8)
- [Generate BOM file (only for assemby service)](https://jlcpcb.com/help/article/How-to-generate-the-BOM-and-Centroid-file-from-KiCAD)
- Upload Gerber files and BOM to JLCPC.com
- Default settings should be fine
- Add SMT assemby service if needed

::right::

<v-click>

#### 💡 Cost saving
 - Buy multiple (5 at JLPCB)
 - Combine orders
 - Basic colors are cheaper

</v-click>

<!---->
<!--• Use 1.6mm PCB thickness-->
<!--• Min trace width: 0.15mm-->
<!--• Min hole size: 0.3mm-->
<!---->

---
layout: iframe
zoom: 0.7
url: https://cart.jlcpcb.com/quote?orderType=1&stencilLayer=2&stencilWidth=100&stencilLength=100&stencilCounts=5&spm=Jlcpcb.Homepage.1010
---

---
layout: end
---
# Thank you!

<div class="absolute bottom-0 right-20 text-xs bg-black bg-opacity-30 px-2 py-1 rounded">
  <a 
    href="https://github.com/mskry" 
    target="_blank" 
    alt="presenter's github link" 
    title="Mykola Skrypets"
    class="text-gray text-jb-medium hover:text-blue-200 transition-colors duration-200"
  >
    Presented by Mykola Skrypets
  </a>
</div>
