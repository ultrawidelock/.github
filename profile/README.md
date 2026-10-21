<p align="center">
<img src="assets/poster.svg" width="880" alt="Walk up. It unlocks. Open-source firmware for a door lock that opens with the digital key in your phone. A phone approaches a door drawn to scale; the lock ranges it with radio pulses along a ticked track and the bolt slides open inside the 1.00 m bound. Below, the seven libraries the lock is built from: tinyble, tinycred, tinyuwb, tinytalk, tinygrid, tinypsa, tinyfota, each with its measured flash size."/>
</p>

<p align="center">
<a href="https://ultrawidelock.com/twin/index.html"><img src="assets/btn-twin.svg" height="44" alt="Try it in your browser"/></a>
<a href="https://ultrawidelock.com/flash/index.html"><img src="assets/btn-flash.svg" height="44" alt="Flash a board"/></a>
<a href="https://github.com/ultrawidelock/ultrawidelock"><img src="assets/btn-firmware.svg" height="44" alt="Read the firmware"/></a>
</p>

**Open-source firmware for a door lock that opens with the digital key in your phone.** Range is radio time of flight, measured on the lock, so a relay can only make the phone look farther away. The bolt moves at 1.00&nbsp;m or less, once three rounds agree. No app, no account, no cloud round trip.

## The lock, in parts

Seven libraries in portable C11, each small enough to read end to end. [tinylock](https://github.com/ultrawidelock/tinylock) builds a door lock from all of them on one 512&nbsp;KB microcontroller.

| Library | Does | Flash / RAM, KB |
|:---|:---|---:|
| [tinyble](https://github.com/ultrawidelock/tinyble) | BLE host for commissioning, raw HCI | 6.7 / 2.5 |
| [tinycred](https://github.com/ultrawidelock/tinycred) | Digital-key reader: BLE, then UWB ranging | 12.7 / 6.6 |
| [tinyuwb](https://github.com/ultrawidelock/tinyuwb) | DW3000 UWB driver and ranging engine | 8.5 / 0.9 |
| [tinytalk](https://github.com/ultrawidelock/tinytalk) | Smart-home accessory node, uncertified | 52.6 / 20.9 |
| [tinygrid](https://github.com/ultrawidelock/tinygrid) | Mesh end device that never routes | 19.3 / 9.9 |
| [tinypsa](https://github.com/ultrawidelock/tinypsa) | Minimal PSA Crypto provider for Zephyr | 17.8 / 1.5 |
| [tinyfota](https://github.com/ultrawidelock/tinyfota) | Signed delta updates over BLE, in place | 4.7 / 1.0 |
| [tinylock](https://github.com/ultrawidelock/tinylock) | All seven on one nRF52833 | **197.9 / 73.3** |

Sizes are LTO release builds, as measured in each repository's README.

## The complete lock

[ultrawidelock](https://github.com/ultrawidelock/ultrawidelock) is the full firmware: UWB and NFC, three boards, a browser twin that runs the real ranging code, and a flasher that works from the browser. Clone it and run `make check` to run the host suite with no board attached. The [guides](https://ultrawidelock.com/docs/index.html) cover adding the key, bring-up on each board, and porting.

<sub>Experimental firmware, provided as is, without warranty of any kind. Not affiliated with, endorsed by, or certified by any company or standards body whose technology these repositories implement.</sub>
