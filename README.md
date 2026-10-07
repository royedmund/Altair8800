# Altair 8800 simulator

Roy Antaw's fork of [David Hansel's Arduino Altair 8800 simulator](https://github.com/dhansel/Altair8800). Original authorship and licensing are retained.

## Start here

- [Project and hardware overview](https://www.hackster.io/david-hansel/arduino-altair-8800-simulator-3594a6)
- [Simulator manual (PDF)](Documentation.pdf)
- [Editable manual (Word)](Documentation.docx)
- [Upstream community discussion](https://groups.google.com/forum/#!forum/altair-duino)

## Build the desktop simulator

The included [Makefile](Makefile) builds the PC version with a C++ compiler, Make, ncurses and pthreads. From the repository root on Linux:

```bash
git clone https://github.com/royedmund/Altair8800.git
cd Altair8800
make
./Altair8800
```

Use the manual for simulator operation and configuration. Building the desktop simulator does not install Arduino firmware. For the Arduino version, start with [Altair8800.ino](Altair8800.ino) and the hardware instructions in the manual.

## Repository layout

| Location | Purpose |
| --- | --- |
| Root `.cpp` / `.h` files and `Altair8800.ino` | Simulator, CPU cores, peripherals and host implementations |
| [Arduino/](Arduino/) | Arduino compatibility code used by the desktop build |
| [disks/](disks/) | Supplied disk images |
| `Makefile` / `Altair8800.vcxproj` | Desktop build definitions |
| `Documentation.pdf` / `Documentation.docx` | User and hardware documentation |
| [LICENSE](LICENSE) | Project licence |

The flat source layout matches the existing build definitions. Keep it intact unless the Makefile, Visual Studio project and Arduino workflow are updated together. Desktop object directories and executables are already ignored by Git.

For problems specific to this fork, [open an issue here](https://github.com/royedmund/Altair8800/issues) and include the revision, platform and build output. Use the upstream discussion group for general simulator questions.
