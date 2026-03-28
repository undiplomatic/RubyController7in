# Open Source 7" FPV Controller with Display for RubyFPV

>[!NOTE]
>This is not a production ready controller, it may contain design faults. I am **not an engineer** and cannot vouch for its safety.
>Ergonomics are still very basic. Uses a low cost screen, with plans to update for a high brightness outdoor screen once testing completes.
>Updates to the controller will depend on demand. If there's demand, I'll update it. If no demand, you take it as it is.

>[!TIP]
>Although designed for RubyFPV, no reason it cant be used for other systems such as OpenHD.

![Main View](https://github.com/undiplomatic/RubyController7in/blob/main/Images/MainView.jpg)

## Why RubyFPV
As of late 2025, RubyFPV has matured into a stable digital FPV and link system. Users report it operates flawlessly without stutters or break-ups. In my home testing, Ruby achieves approximately 75% of the range of DJI O4. As of early 2026, the project is working on integrating specialist FPV modules which will further improve the link. These upcoming modules will provide a more stable link, more range, and lower latency across multiple frequencies. They will support multiple frequency bands, a first for digital FPV, including traditional 5.8GHz and low-frequency bands for long range.

Open source FPV eliminates the "vendor lock-in" and privacy concerns associated with closed systems. For example, DJI has been shown to have back doors in their hardware, require activation, and restrict certain features for non-DJI drones. Because RubyFPV is open, it can be fully customised for industrial, academic, or developer applications. It also handles video, telemetry, and control signals over a single link and supports advanced features like signal relaying and antenna trackers.

## Why This Controller
This 3D-printed controller includes features missing on commercial systems, such as a six-position switch specifically for Ardupilot flight modes, along with a high number of assignable switches. Because RubyFPV supports multiple concurrent links across different frequencies, this controller has the internal space to house multiple transceiver modules simultaneously.

## Features
| Feature | Description | |
| :--- | :--- | :--- |
| 7 inch screen | Good size screen, reasonably priced | ✅ |
| Screen and controller in one | No need for a separate control link such as ELRS | ✅ |
| Raspberry Pi / Radxa Rock based |  | ✅ |
| Open source joystick controller | Uses highly configurable FreeJoy HID controller, allowing large number of switches and pots | ✅ |
| Radiomaster AG1 Hall Sensor Gimbals | Beware: the hall sensor wires on Radiomaster are mis-coloured, remove wires and check polarity printed on sensors | ✅ |
| Built in open source patch antennas | Low profile, low cost, perfect radiation beam for long range | ✅ |
| Diversity omni antennas | V shaped antennas to reduce blind spots | ✅ |
| RTL EU2 Wifi chips with heat sinks | Transceivers mount on integrated heat sinks | ✅ |
| Active cooling | Two large fans | ✅ |
| Rotary switch | Rotary switches support large number of positions, suitable for flight modes on Ardupilot etc | ✅ |
| Power switch guard | Knock guard protects against accidental on/off | ✅ |
| Mini nav stick | Used to navigate through RubyFPV menus. Spare nav stick for screen control. | ✅ |
| LCD Screen | Used for aux display on RubyFPV | ✅ |
| External USB port | Used to update firmware | ✅ |
| High brightness outdoor screen | 2000 nit screen coming soon | ⏳ |
| Ergonomics | Improved ergonomics coming soon | ⏳ |

>[!NOTE]
>Files created in FreeCAD for easy updating.
>STL files in multiple parts to fit typical 3D printers.

![Rear View](https://github.com/undiplomatic/RubyController7in/blob/main/Images/RearView.jpg)
Wiring looks complex: it's not, the switches and gimbal wiring create that illusion.

>[!NOTE]
>The RTL chips get hot. Heat sinks are glued into the board, and the RTL modules are attached to the sinks using thermal adhesive tape.
>The board you see creates two levels inside the controller. The bottom level houses the screen, wiring and gimbals. The top level houses the Radxa/Raspberry, batteries, HID joystick controller, and RTL modules.

![Rear View](https://github.com/undiplomatic/RubyController7in/blob/main/Images/Level2Board.jpg)

## Part List

| | Part | Description |
| :--- | :--- | :--- |
| ![Main View](https://github.com/undiplomatic/RubyController7in/blob/main/Images/Screen.jpg) | Screen | Generic Raspberry Pi HDMI display, 7 inch. Find this **exact** screen to ensure a fit. |
| | SoC Computer | Raspberry Pi or Radxa Rock |
| | Gimbals | Radiomaster AG01 gimbals |
| | RTL WiFi modules | Two RTL8812EU-CG Long Distance drone modules act as transceivers |
| | Blue Pill STM32 | Low cost device that is flashed with FreeJoy. Solder all the hall sensors, switches, and pots to it. |
| | BEC or Voltage Regulators | 5.0v. Beware, many are 5.2v which isn't ideal, though still in tolerance for some 5v devices. But check voltage is no higher! I run TWO regulators, one powers the SoC and one RTL WiFi module. The other powers the fans and second RTL module. This is recommended so that a short in the fans doesn't cause outage. |
| ![HMDI Cable Left-Straight 15cm](https://github.com/undiplomatic/RubyController7in/blob/main/Images/HDMILeftStraight.png) | HDMI Cable | 15cm left plug and straight plug other end |
| | Battery holder | Three 18650 cell holder |
| ![Kycon socket](https://github.com/undiplomatic/RubyController7in/blob/main/Images/KPJXDCSocket.png) ![DIN Connector](https://github.com/undiplomatic/RubyController7in/blob/main/Images/DINConnector.png)| DC Socket | Kycon KPJX Straight DC Socket, part KPJX-PM-4S. These are not cheap, but are the only 4 pin DC plugs I can find. Male end is more common, often called a DIN plug even though not DIN compatible. Real DIN plugs have thinner pins and not suitable for DC charging. |
| | Patch Antennas x2 | Triple feed patch antenna, low cost, open source design. You also need 50 ohm SMA terminals for them to work properly. |
| | Omni Antennas x2 | SMA Antennas |
| | Fans x2 | 4010 5v fans. Wire to second voltage regulator for safety. |
| | Slide Switch | 6amp switch for main power, 27.5mm hole spacing +/- 1mm. Typically marked "6a 125v/3a 240v". Product title often states 3 amps, but specs show 6 amp at lower voltages. |
| | Toggle switches | MTS series generic toggle switches |
| | Rotary switch | SR16 |
| | Heat sinks | 30x30mm alu |
| | SMA U.FL Connectors | Two male SMAs for the omni antennas and two females for the patch antennas |
| ![Mini Nav Switch](https://github.com/undiplomatic/RubyController7in/blob/main/Images/NavStick.png)| Mini Nav switch | Five Way Switch SMD DIP 6Pin Multi Directional Mobile Navigation Switch Touch Reset Key 7.5x7.5 |
| | LCD Display | Optional 0.96" I2C OLED Display Module |
| | LEDs | 6mm hole, 5v. I suggest using 12/24v LED for the power LED to keep brightness low. |
| | M2 brass inserts | |
| ![USB Plug](https://github.com/undiplomatic/RubyController7in/blob/main/Images/USBPlug.png) | USB plugs | Self solder type, male and one female |
| | Silicone wire | 30 AWG |
| | 1.25mm Connectors | Small, JST like connectors such as Molex PicoBlade or MX 1.25 |
| | 18650 Li-Ion Cells | |

... and other misc items: thermal adhesive tape, resistors for rotary switch and three position switches, and probably more things I've forgotten about.

## Charging Lead

The controller uses a 4-pin DC plug as a balance lead, with pins wired to each junction of the three battery cells. Due to space constraints, there is no dedicated main power socket. Since most chargers do not support charging  via the balance lead alone, you can use a breakout lead (an XT30 plug connected to the two outer junctions). While this is electrically the same as a standard charging setup, the power is "tapped" from  balance wires, therefore, you must charge at a low current to prevent issues.

```
DC PLUG PIN:(1)         (2)         (3)         (4)
             |           |           |           |
             +--[Cell1]--+--[Cell2]--+--[Cell3]--+
             |  (3.7V)      (7.4V)      (11.1V)  |
             |                                   |
 XT30:  NEG (-)                             POS (+)
```

![Charge Lead](https://github.com/undiplomatic/RubyController7in/blob/main/Images/ChargeLead.jpg)

## USB and hall sensor wiring

* __Tightly__ twist the USB data wires and keep them as short as possible
* __Lightly__ twist the hall sensor wires and keep them as short as possible
* WiFi transceivers should take power direct from the voltage regulators. USB power is insufficient at high outputs.

## Three position switches

* These should be wired to an analogue terminal on the Joystick Blue Pill STM32 controller.
* Two 5k resistors from centre terminal to outer terminals.
* Power and Ground from the joystick controller to the switch outer terminals.
* Centre switch terminal to analogue pin

```
SWITCH PIN: (GND)   (Analogue Pin)    (3.3v)
                |          |          | 
                +---[R1]---+---[R1]---+
                [#### SWITCH BODY ####]

```

## Rotary switch

* Small resistors between the terminals create a "voltage ladder" (Google it).
* The total resistance should sum to ~10 kOhms
* Wire to an analogue pin on the Joystick HID Blue Pill STM32 controller

Ardupilot flight mode channel is a pain as the switch boundaries are not configurable, so each notch on the switch may not move the flightmode by one setting. Thankfully, FreeJoy *axes curves* can fix this. The image shows how to configure a six position switch.

![Axes curve to fix switch boundaries in Ardupilot](https://github.com/undiplomatic/RubyController7in/blob/main/Images/RotarySwitchAxesCurve.png)
