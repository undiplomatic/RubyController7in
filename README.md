# Open Source 7" FPV Controller with Display for RubyFPV

>[!NOTE]
>This is not a production ready controller, it may contain design faults. I am not an engineer and cannot vouch for its safety.
>Ergonomics are currently very basic. Uses a low cost screen, with plans to update for a high brightness outdoor screen once testing completes.
>Updates to the controller will depend on demand. If there's demand, I'll update it. If no demand, you take it as it is.

>[!TIP]
>Although designed for RubyFPV, no reason it cant be used for other systems such as OpenHD.

![Main View](https://github.com/undiplomatic/RubyController7in/blob/main/Images/MainView.jpg)

## Features
| Feature | Description |
| :--- | :--- |
| 7 inch screen | Good size screen, reasonably prices | ✅ |
| Screen and controller in one | No need for a separate control link such as ELRS | ✅ |
| Raspberry Pi / Radxa Rock based |  | ✅ |
| Open source joystick controller | Uses highly configurable FreeJoy HID controller, allowing large number of switch and pots | ✅ |
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
