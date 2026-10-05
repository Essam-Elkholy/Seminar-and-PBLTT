# Seminar and PBL — FPGA Sobel Edge Detector

An E-JUST team project to develop a Verilog RTL image edge detector on FPGA, using Sobel processing, UART RX/TX, FIFO and frame-buffer memory, VGA output, and Python image tools.

## Current status

This repository contains the initial folder structure, documentation and comment-only RTL/testbench placeholders. No hardware implementation or completed verification is included yet. Filenames describe planned responsibilities and may be adjusted after interface review.

## Repository layout

```text
rtl/
  uart/       UART receiver, transmitter and wrapper
  fifo/       Pixel buffering
  memory/     Frame-buffer storage
  sobel/      Line buffers, Sobel arithmetic and core wrapper
  vga/        Display timing and wrapper
  top/        System controller and top-level integration
tb/
  uart/       TX, RX and loopback testbench placeholders
  fifo/       FIFO testbench placeholder
  memory/     Frame-buffer testbench placeholder
  sobel/      Window, arithmetic and core testbench placeholders
  vga/        VGA testbench placeholder
  system/     Integrated system testbench placeholder
python/       Image conversion, golden model and comparison tools
testdata/     Shared test inputs and expected outputs
constraints/ FPGA pin and clock constraints
docs/         Architecture, interfaces, research and verification notes
.github/      Pull request template
```

RTL and testbench files contain instructions only. Replace their comments with the agreed implementation; do not treat a placeholder as a finished module. No simulation launcher scripts or simulator configuration folder are included in this setup.

## Research before implementation

Before writing RTL, each module owner should:

1. Learn the module's purpose, operating principle, ports, timing and parameters using web searches, useful tutorials and official documentation.
2. Explain its role in our image-processing system and its connections to neighboring modules.
3. Study previous FPGA projects using the module.
4. Search GitHub for relevant RTL and testbenches, understand their data path and control logic, and identify assumptions that need adapting.
5. Record findings and source links in a short research note.
6. Agree on interfaces and test expectations with Essam and the relevant module owners before implementation.

See [CONTRIBUTING.md](CONTRIBUTING.md), [the interface worksheet](docs/interfaces.md) and [the research guide](docs/research/README.md).

## Team responsibilities

| Owner | Main responsibility |
| --- | --- |
| Awad | UART RX/TX and local testbenches |
| Rafaat | FIFO, frame-buffer memory and local testbenches |
| Ashraf | Sobel, VGA and local testbenches |
| Baraa | Python image tools, golden model and comparison |
| Essam | Interface agreements, top-level integration, system verification and team coordination |

## Collaboration

Create a branch for each focused task, commit and push your work, and open a pull request targeting `main`. Include the task link, changes, verification evidence and remaining limitations. Essam coordinates review and integration.

Track ownership, dependencies and dates in [our GitHub Project](https://github.com/users/Essam-Elkholy/projects/3). A Project README is separate from this repository README.

## References

- [Bob-youssef / Sobel-Image-Edge-Detector](https://github.com/Bob-youssef/Sobel-Image-Edge-Detector): primary starting reference for Sobel RTL and image conversion.
- [AngeloJacobo / FPGA RealTime and Static Sobel Edge Detection](https://github.com/AngeloJacobo/FPGA_RealTime_and_Static_Sobel_Edge_Detection): system integration, buffering and display reference; `src2` uses static images over UART, while `src1` uses a camera.

Keep attribution and the applicable license notices for any reused material. Document which reference was used and what was changed.
