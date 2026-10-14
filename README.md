# MICROSCOPY

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-scientific_lab-lightgrey)

> Anticloud-hardened packaging of the upstream project `MICROSCOPY` in category **SCIENTIFIC LAB**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SCIENTIFIC LAB · **Upstream:** https://github.com/IBM/MicroscoPy · **Upstream pin:** `afc20d1d74053fe1d923274ad4d8b0caf470d1ef` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# An open-source MICROSCOPE built using LEGO bricks, 3D-printing, Arduino and Raspberry Pi

![Animation](docs/Animation.gif)

![Images](docs/Images.jpg)

![Stop-motion](docs/Stop-motion.gif)

## Key Features

- **Fully motorized:** Camera angle, sample position, magnification and focus can be adjusted precisely using six stepper motors.
- **Modular:** Stages and modules can be arranged in any configuration depending on the application.
- **Versatile:** Uniform illumination guarantees high quality imaging for a variety of samples with reflective or transparent surfaces.  
- **Wide magnification range:** Samples with features from several centimeters to several micrometers can be imaged without changing the objective lens.
- **Low-cost:** The whole assembly costs from $200 to $400 depending on the features and the vendors of the electronic components.  
- The microscope uses a **Raspberry Pi** mini-computer with an **8MP camera** to capture images and videos. Stepper motors and the illumination are controlled using a circuit board comprising an **Arduino microcontroller**, six **stepper motor drivers** and a **high-power LED driver**. All functions can be controlled from a keyboard connected to the Raspberry Pi or a separate custom-built Arduino joystick connected to the mainboard. **LEGO bricks** are used to construct the main body of the microscope to achieve a modular and easy-to-assemble design concept.

![Diagram](docs/Diagram.jpg)

## Assembly instructions

|       [Video (YouTube)](https://youtu.be/PBSYnk9T4o4)        |     [Instructions (PDF)](Instructions.pdf)     |
| :----------------------------------------------------------: | :--------------------------------------------: |
| [![YouTube](docs/YouTube.jpg)](https://youtu.be/PBSYnk9T4o4) | [![](docs/Instructions.jpg)](Instructions.pdf) |
|  **[Circuit assembly (PDF)](/Circuit/CircuitAssembly.pdf)**  | **[Raspberry Pi HQ camera test](/HQ-camera)**  |
| [![Circuit](docs/Circuit.jpg)](/Circuit/CircuitAssembly.pdf) | [![HQ-camera](docs/HQ-camera.jpg)](/HQ-camera) |

## Operation principle

The microscope has a simple operation principle based on changing the magnification and the focus by adjusting the relative distances between a **camera**, a single **objective lens** and a **sample**. Briefly, two linear stages with stepper motors are used to adjust these distances for a continuous and wide magnification range. Four additional stepper motors **tilt** the camera module and change the **X-Y position** and **rotation** of the sample. A **uniform light source** illuminates the sample either from an angle *(reflected light)* or from the bottom of the sample *(transmitted light)*. The system can also be used as a *digital water contact angle goniometer* by taking cross-section images of droplets. 

![Operation](docs/Operation.jpg)

## Assembly steps

- [Enjoy the YouTube video and get a general idea about the assembly of the microscope.](https://youtu.be/PBSYnk9T4o4) 

- [Follow the detailed instructions provided in the PDF document.](Instructions.pdf)

- [3D print the design files.](#3D-printing)

- [Build the electronic board.](#Electronics)

- [Upload the Arduino code.](#Uploading-the-Arduino-code)

- [Assemble the microscope.](#Final-assembly)

- [Run the Python code.](#Python-Raspberry-Pi)

- [Try different operation modes and enjoy the microscope.](#Basic-operation-modes)

- [Check these instructions if you would like to test the new hiqh quality (HQ) camera](/HQ-camera)

  

## 3D printing

I assembled the main body of the microscope using individually-purchased [LEGO bricks](https://www.lego.com/en-us/page/static/pick-a-brick). Instead of using motors and gears from LEGO Technic, I designed custom actuators using [FreeCAD](https://www.freecadweb.org/) software and printed them using my personal [3D printer](https://www.creality3d.shop/products/creality3d-ender-3-pro-high-precision-3d-printer). This approach not only lowered the cost of the microscope but also gave me some flexibility in the design and implementation of precise linear and rotary actuators. In principle, the whole structure could be 3D-printed without using any LEGO parts but that would be less modular and more time consuming.  

All STL files for 3D printing and the original FreeCAD files for editing are available in this [folder](https://github.com/IBM/MicroscoPy/tree/master/3D-design-files). You may need to install [FreeCAD Gear workbench](https://wiki.freecadweb.org/Macro_FCGear) to edit the gears. 

:warning: A good quality printing depends on many factors. I optimized the designs after several iterations of printing. If the parts do not match well, some minor modification in the original design file (e.g. enlarging the holes matching to LEGO studs) or polishing/drilling may be required. More information on the printer and slicer settings is given in the [PDF document](Instructions.pdf) (page #72). 

![3Dprinting](docs/3Dprinting.jpg)

## Electronics  

:warning: **This part requires some basic knowledge on electronic circuit design and Arduino.**

All design and Gerber files of printed circuit boards (PCBs) are available in this [folder](/Circuit). I designed the PCBs using [DesignSpark PCB software](https://www.rs-online.com/designspark/pcb-software). The list of all components can be found in the [PDF document](Instructions.pdf) (page #71)  

There is also a separate [instruction manual](/Circuit/CircuitAssembly.pdf) giving more details about the assembly of the circuit boards.

The operation of the electronics is straight-forward. I used two Arduino microcontrollers, one for the *mainboard* (essential) and one for the joystick *controller* (optional), to control the stepper motors and the LED illumination of the microscope. In principle, everything could be controlled directly from the Raspberry Pi without using any Arduino microcontroller but I decided to leave testing this option for another time.

:bulb: The joystick controller is optional bec

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Unknown (no standard manifest detected)** (manifests: none detected; scanned in UPSTREAM_CLONE)
- Top-level source layout: `3D-design-files/`, `Arduino/`, `Circuit/`, `HQ-camera/`, `Image-examples/`, `Python/`
- Snapshot size: **56 files**, **901 lines of code** (measured; see Benchmarks)
- Primary languages: `.fcstd` (16), `.stl` (13), `.jpg` (9), `.pdf` (6), `.ino` (2), `.md` (2)
- Upstream commit pinned for this packaging: `afc20d1d74053fe1d923274ad4d8b0caf470d1ef`

---

## Installation

- [Upload the Arduino code.](#Uploading-the-Arduino-code)

- [Assemble the microscope.](#Final-assembly)

- [Run the Python code.](#Python-Raspberry-Pi)

- [Try different operation modes and enjoy the microscope.](#Basic-operation-modes)

- [Check these instructions if you would like to test the new hiqh quality (HQ) camera](/HQ-camera)

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

![Electronics](docs/Electronics.jpg)

I preferred [Adafruit ItsyBitsy 32u4 5V](https://learn.adafruit.com/introducting-itsy-bitsy-32u4) but any Arduino board with enough number of I/O pins should work. If you want to use the joystick controller, the Arduino boards should support serial (UART) communication because they cannot communicate with each other via their USB ports. 

The Arduino on the *controller* circuit reads the status of three [thumb joysticks](https://www.sparkfun.com/products/9032) (for six stepper motors) and a potentiometer (for the LED intensity) via its analog inputs. The data is sent to the Arduino on the *mainboard* via UART (RX, TX) serial communication. An OLED display on the *controller* can be used to display useful information, like the PWM (pulse-width modulation) intensity of the LED. The Arduino on the *mainboard* receives and processes the incoming data and sends stepper motor signals to the corresponding stepper motor via its respective [motor driver](https://www.adafruit.com/product/3297). Six motor drivers share the same signal pins but only one driver is activated at a time using the *enable* *(EN)* or the *sleep* *(SLP)* pin of the driver. This implementation requires only 10 I/O pins *(4 signal + 6 enable)* instead of 24 *(4 signal x 6 motors)*. It also prevents the heating of the motors when they are idle and limits the current consumption by allowing only one motor running at a time. Alternatively, a motor driver with a built-in indexer with STEP/DIRECTION control can be used to reduce the number of I/O pins but such drivers are more expensive. The data is sent only if there is a change in the joystick position is detected to avoid continuous communication. 

The *mainboard* can be powered from an external 5V wall charger or directly from the USB port of the Raspberry Pi. The latter also allows USB communication between the *mainboard* and the Raspberry Pi to control the stepper motors and the LED intensity from a keyboard. The intensity of the LED is controlled by PWM using a dedicated pin on the Arduino. I recommend keeping the LED off while the Raspberry Pi is booting and then gradually increasing the intensity. The [LED driver](https://www.digikey.com/products/en?keywords=945-1818-5-ND) and the [high-power LED](https://www.digikey.com/products/en?keywords=1672-1161-ND) used in this project required more than 6V for a rated operation. I initially used an external 12V power adapter for the LED but later generated 12V directly from the USB port of the Raspberry Pi using a step-up [DC-DC converter](https://www.banggood.com/DC-DC-Boost-Buck-Adjustable-Step-Up-Step-Down-Automatic-Converter-XL6009-Module-p-1087346.html?rmmds=search&cur_warehouse=CN). In this case, the 5V power adapter should be able to supply enough current for the Raspberry Pi, stepper motors and the LED. I tested the system using a single 5V / 3A supply (original Raspberry Pi 4 power supply or a wall charger). Different configurations may require different power ratings. For example,  if the display is also powered from the same source, then a more powerful 5V source would be needed. [Here](https://www.digikey.com/products/en?keywords=709-GST60A05-P1J) is a good one.  

:warning: The high-power LED gets hot after some time, be cautious. I used a standard aluminum [heat sink](https://www.adafruit.com/product/3083) to help cooling a little bit.

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

- **Versatile:** Uniform illumination guarantees high quality imaging for a variety of samples with reflective or transparent surfaces.  
- **Wide magnification range:** Samples with features from several centimeters to several micrometers can be imaged without changing the objective lens.
- **Low-cost:** The whole assembly costs from $200 to $400 depending on the features and the vendors of the electronic components.  
- The microscope uses a **Raspberry Pi** mini-computer with an **8MP camera** to capture images and videos. Stepper motors and the illumination are controlled using a circuit board comprising an **Arduino microcontroller**, six **stepper motor drivers** and a **high-power LED driver**. All functions can be controlled from a keyboard connected to the Raspberry Pi or a separate custom-built Arduino joystick connected to the mainboard. **LEGO bricks** are used to construct the main body of the microscope to achieve a modular and easy-to-assemble design concept.

![Diagram](docs/Diagram.jpg)

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Unknown (no standard manifest detected) |
| Manifests detected | none |
| Files in snapshot | 56 |
| Lines of code | 901 |
| Dependency references | 0 |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

- **Versatile:** Uniform illumination guarantees high quality imaging for a variety of samples with reflective or transparent surfaces.  
- **Wide magnification range:** Samples with features from several centimeters to several micrometers can be imaged without changing the objective lens.
- **Low-cost:** The whole assembly costs from $200 to $400 depending on the features and the vendors of the electronic components.  
- The microscope uses a **Raspberry Pi** mini-computer with an **8MP camera** to capture images and videos. Stepper motors and the illumination are controlled using a circuit board comprising an **Arduino microcontroller**, six **stepper motor drivers** and a **high-power LED driver**. All functions can be controlled from a keyboard connected to the Raspberry Pi or a separate custom-built Arduino joystick connected to the mainboard. **LEGO bricks** are used to construct the main body of the microscope to achieve a modular and easy-to-assemble design concept.

![Diagram](docs/Diagram.jpg)

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `MICROSCOPY` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
      otherwise, or (ii) ownership of fifty percent (50%) or more of the
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `MICROSCOPY` (category: SCIENTIFIC LAB)
- **Upstream URL:** https://github.com/IBM/MicroscoPy
- **Pinned commit (SHA):** `afc20d1d74053fe1d923274ad4d8b0caf470d1ef`
- **Branch:** master
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`60073c6482f7c06f32190d416382b1a12f6e746813dbcd284a24e32fad819bba`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

