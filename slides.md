---
# You can also start simply with 'default'
theme: seriph
background: /images/background-2.png
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
<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

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

<!--1. Bottom case / acryllic plate / FR plate : Screw in PCB into it, can hold sound dampening material (EVA - Ethylene-vinyl acetate, Poron - Urethane material, PE - Polyethylene) -->
<!--2. PCB (Printed Circuit Board) made of FR4 - base material made from a flame retardant epoxy resin and glass fabric composite.-->
<!--3. Plate: -->
<!--Siwtches
      profiles: cherry mx compatible, low profile kailh chock/gateron,
      material: PBT, ABS, resin, metal, 
      process: dye sublimation, Reverse Dye-sublimation , double shot
      different patterns: clicky, linear, tactile, silent
      heaviness: spring rigidity : light / heavy
      types: mechanical, optical, HAL-effect
      mod: O-ring, film, lubrication
-->
 <!-- Stabilizers - mechanisms that keep the larger keys like Space, Shift, Enter, and Backspace in place and, for lack of a better word, stable. -->

---
transition: fade-out
layout: two-cols-header
---

# MCU and SoC <MarkerHardware/>

Microcontrollers and SoCs typically responsible for the following key functions in keyboards
- Host connectivity
- Peripherals connectivity
- Key matrix scanning
- Debouncing
- LED control
- Memory


<div
  v-motion
  :initial="{ x: 1100, y: 190 }"
  :enter="{ x: 50 }"
  :leave="{ y: 400 }"
>
<div class="absolute right-100px bottom-50px">
  <img width="220" src="/images/atmega.avif" alt="atmega32u4 image">
</div>

</div>
<!--
1. Handling USB, Bluetooth Low Energy (BLE), or other communication protocols to connect the keyboard to a host device.
2. Interfacing with various peripherals such as analog-to-digital converters (ADCs), pulse-width modulation (PWM) controllers, I2C, and SPI.
3. Scanning the keyboard matrix to detect key presses and releases.
4. Processing mouse movement data and reporting it to the host.
5. Filtering out switch bouncing to ensure reliable key detection.
6. Controlling LED indicators and underglow effects.
7. Storing configuration data, macros, or other persistent information in flash memory or EEPROM.
-->

---
transition: slide-up
layout:  two-cols-header
---
# MCU and SoC: Top ones <MarkerHardware/>
::left::
<v-clicks>

1. **Atmega32u4** 
- 8-bit AVR RISC-based microcontroller
- Budget-friendly, used in many keyboard projects
- 32 KB of flash memory, 2.5 KB SRAM
- 20 MHz clock speed

2. **STM32F103**
- 32-bit ARM Cortex-M3 microcontroller
- High performance, used in high-end keyboards
- 64 KB to 128 KB of flash memory, 20 KB to 64 KB SRAM
- 72 MHz clock speed

</v-clicks>

::right::

<v-clicks>

3. **RP2040**
- 32-bit ARM Cortex-M0+ microcontroller
- Developed by Raspberry Pi, gaining popularity
- 264 KB of flash memory, 264 KB SRAM
- 133 MHz clock speed
4. **nRF52840**
- 32-bit ARM Cortex-M4 microcontroller
- Supports Bluetooth Low Energy (BLE)
- 1 MB of flash memory, 256 KB SRAM
- 64 MHz clock speed

</v-clicks>
---
transition: slide-up
layout: center
zoom: 0.9
---

# MCU and SoC: A Comparison <MarkerHardware/>
| **Feature**      | **Atmega32u4** | **STM32F103** | **RP2040** | **nRF52840** |
|---------------|------------|------------|---------|-----------|
| 🔲 Processor   | 8-bit AVR  | 32-bit ARM | 32-bit ARM | 32-bit ARM |
| 💾 Flash Memory  | 32 KB      | 64-128 KB  | 264 KB  | 1 MB       |
| RAM           | 2.5 KB     | 20-64 KB   | 264 KB  | 256 KB     |
| 💪 Speed   | 20 MHz     | 72 MHz     | 133 MHz| 64 MHz     |
| 🔌USB Support   | Yes        | Yes        | Yes     | Yes        |
| ᛒ Bluetooth LE  | No         | No         | No      | Yes        |
| 🖱️Peripherals   | [ADC](https://en.wikipedia.org/wiki/Analog-to-digital_converter), [PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation)   | [ADC](https://en.wikipedia.org/wiki/Analog-to-digital_converter), [PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation), [I²C](https://en.wikipedia.org/wiki/I%C2%B2C), [SPI](https://en.wikipedia.org/wiki/Serial_Peripheral_Interface) | [ADC](https://en.wikipedia.org/wiki/Analog-to-digital_converter), [PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation), [I²C](https://en.wikipedia.org/wiki/I%C2%B2C), [SPI](https://en.wikipedia.org/wiki/Serial_Peripheral_Interface) | [ADC](https://en.wikipedia.org/wiki/Analog-to-digital_converter), [PWM](https://en.wikipedia.org/wiki/Pulse-width_modulation), [I²C](https://en.wikipedia.org/wiki/I%C2%B2C), [SPI](https://en.wikipedia.org/wiki/Serial_Peripheral_Interface) |
| 👥 Support | High | High | High | Moderate |
| 💸 Cost        | € | €€ | €€ | €€€ |

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

<!--<div v-click.hide="[2]">-->
<!--  <img  class="absolute right-120px bottom-120px" width="430" src="/pro_micro_pinout.jpg"/>-->
<!--</div>-->

<!--<div v-click.hide="[1]">-->
<!--  <img  class="absolute right-150px bottom-50px" width="500" src="/elite-pi-pinout.png"/>-->
<!--</div>-->
<!---->
<!--<div v-click.hide="[1]">-->
<!--  <img  class="absolute right-100px bottom-50px" width="430" src="/sea-picro-pinout.png"/>-->
<!--</div>-->
<!--<div v-click.hide="[1]">-->
<!--  <img  class="absolute right-100px bottom-50px" width="600" src="/nicenano-pinout-v2.png"/>-->

<img  class="absolute right-290px bottom-150px" width="120" src="/images/nicenano-v2.png"/>
<img  class="absolute right-30px bottom-20px" width="280" src="/images/sea-picro-render.png"/>

<!--Pro Micro initially created by SparkFun as Arduino-compatible board. Open Source Hardware Association(Arduino, Adafruit Industries) . There tons of ProMicro footprint clones with either ATmega32U4 or RP2040.-->
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

- **Realtime keymap updating** ([VIA](https://www.caniusevia.com/), [VIAL](https://get.vial.today/), [remap-keys.app](https://remap-keys.app/), etc) ✨

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
layout: center
---

# Thank you!
