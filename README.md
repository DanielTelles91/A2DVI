# A2DVI - Apple II Digital Video

This is a project for a digital DVI/HDMI Apple II video card.
It directly produces a digital video stream from Apple II's memory content.
The signal is output via an HDMI connector, connecting the Apple II to modern displays with HDMI (or DVI) inputs.
No more analog signal conversion required.

The project is a collaboration with Thorsten Brehm. His related firmware project is here: https://github.com/ThorstenBr/A2DVI-Firmware

For the DVI output to be active, the new firmware developed by Thorsten should be used.

The card also has an alternative analog VGA connector.
For the VGA output to be active, the [VGA firmware](https://github.com/markadev/AppleII-VGA) developed by Mark Aikens should be used.

The card can produce either an analog VGA or a digital HDMI signal, but not both simultaneously.
To switch between modes, a firmware update is required and opening/closing connections.


![Captura de tela 2024-10-10 230457](https://github.com/user-attachments/assets/a54eeb28-824a-4d6d-ac8d-f013b28bb772)
![Captura de tela 2024-10-10 230504](https://github.com/user-attachments/assets/77b93df3-cf70-4fb8-b49c-9a99998398f9)
![Captura de tela 2024-10-10 230522](https://github.com/user-attachments/assets/5457b145-a199-492c-894b-bebeb66caf3d)
![Captura de tela 2024-10-10 230530](https://github.com/user-attachments/assets/09620d8a-bc85-41d5-b054-c491fe9b5da9)




## Dual-Language Support
The pin on the v1.5 and later boards is for AltChr connection, supported by A2DVI firmware for switching between alternative character sets on non-US versions of Apple II ("Euro-machines").


# Hardware
* Based on the PICO controller board.
* Provides a DVI video stream via an HDMI connector.
* Low power/heat dissipation: less than 70mA@5V = 0.35W in operation.
* Uses 4x 74LV245 bus transceivers for 5V/3.3V signal conversion of the Apple II bus.
* Separate ALTCHR input pin for dual-language support: pin needs to be wired separately to the "language switch" of Euro-Apple IIs (optional).

# Thanks
This is a project based on:

* the AppleII-VGA project by Mark Aikens - https://github.com/markadev/AppleII-VGA

* the PicoDVI project by Luke Wren - https://github.com/Wren6991/PicoDVI

* Thorsten Brehm for firmware development and board design considerations

* Oliver Schmidt on original idea discussions and design considerations

# License
Board design by Ralle Palaveev (c) 2024.

All rights reserved.

Redistribution and use in source, binary, and manufactured forms, with or without
modification, are permitted provided that the following conditions are met:
1. Redistributions of source code and design files must retain the above copyright
   notice, this list of conditions and the following disclaimer.
2. Redistributions in binary or manufactured form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in the
   documentation and/or other materials provided with the distribution.
3. All advertising materials mentioning features or use of this software
   or hardware must display the following acknowledgement:
   This product includes software or hardware developed by Ralle Palaveev.
4. Neither the name of Ralle Palaveev nor the
   names of its contributors may be used to endorse or promote products
   derived from this software or hardware without specific prior written permission.

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
