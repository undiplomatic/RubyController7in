# Open Source 7" FPV Controller with Display for RubyFPV

>[!NOTE]
>This is not a production ready controller, it may contain design faults. I am not an engineer and cannot vouch for its safety.
>Ergonomics are currently very basic. Uses a low cost screen, with plans to update for a high brightness outdoor screen once testing completes.
>Updates to the controller will depend on demand. If there's demand, I'll update it. If no demand, you take it as it is.

>[!TIP]
>Although designed for RubyFPV, no reason it cant be used for other systems such as OpenHD.

![Main View](https://github.com/undiplomatic/RubyController7in/blob/main/Images/MainView.jpg)

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
| RTL EU2 Wifi chips with heat sinks |  | ✅ |
| Active cooling |  | ✅ |
| Rotary switch | Rotary switches support large number of positions, suitable for flight modes on Ardupilot etc | ⏳ |
| Power switch guard | Knock guard protects against accidental on/off | ✅ |
| Mini nav stick | Used to navigate through RubyFPV menus. Spare nav stick for screen control. | ✅ |
| LCD Screen | Used for aux display on RubyFPV | ✅ |
| External USB port | Used to update firmware | ✅ |
| High brightness outdoor screen | 2000 nit screen coming soon | ⏳ |
| Ergonomics | Improved ergonomics coming soon | ⏳ |

>[!NOTE]
>CAD Files done in FreeCAD for easy updating.
>STL files in multiple parts to fit typical 3D printers.

![Rear View](https://github.com/undiplomatic/RubyController7in/blob/main/Images/RearView.jpg)

>[!NOTE]
>The RTL chips get hot. Heat sinks are glued into the board, and the RTL modules are attached to the sinks using thermal adhesive tape.
>The board you see creates two levels inside the controller. The bottom level houses the screen, wiring and gimbals. The top level houses the Radxa/Raspberry, batteries, HID joystick controller, and RTL modules.

![Rear View](https://github.com/undiplomatic/RubyController7in/blob/main/Images/Level2Board.jpg)

## Part List

| | Part | Description |
| :--- | :--- | :--- |
| ![Main View](https://github.com/undiplomatic/RubyController7in/blob/main/Images/Screen.jpg) | Screen | Generic Raspberry Pi HDMI display, 7 inch |
| | SoC Computer | Raspberry Pi or Radxa Rock |
| | Gimbals | Radiomaster AG01 gimbals |
| | RTL WiFi modules | Two RTL8812EU-CG Long Distance drone modules |
| | Blue Pill STM32 | Low cost device that is flashed with FreeJoy. Solder all the hall sensors, switches, and pots to it. |
| | BEC or Voltage Regulators | 5.0v. Beware, many are 5.2v which isn't ideal, though still in tolerance. I run TWO regulators, one powers the SoC and one RTL WiFi module. The other powers the fans and second RTL module. This is recommended so that a short in the fans doesn't cause outage. |
| ![HMDI Cable Left-Straight 15cm](https://github.com/undiplomatic/RubyController7in/blob/main/Images/HDMILeftStraight.png) | HDMI Cable | 15cm left plug and straight plug other end |
| | Battery holder | Three 18650 cell holder |
| ![Kycon socket](https://github.com/undiplomatic/RubyController7in/blob/main/Images/KPJXDCSocket.png) ![DIN Connector](https://github.com/undiplomatic/RubyController7in/blob/main/Images/DINConnector.png)| DC Socket | Kycon KPJX Straight DC Socket, part KPJX-PM-4S. These are not cheap, but are the only 4 pin DC plugs I can find. Male end is more common, often called a DIN plug even though not DIN compatible. |
| | Patch Antennas x2 | Triple feed patch antenna, low cost, open source design. You also need 50 ohm SMA terminals for them to work properly. |
| | Omni Antennas x2 | SMA Antennas |
| | Fans | Two 4010 5v fans |
| | Slide Switch | 3amp/6amp switch for main power, 27.5mm hole spacing |
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

... and other misc items: thermal adhesive tape
