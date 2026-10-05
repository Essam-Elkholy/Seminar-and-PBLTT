# Module research notes

Before implementation, search the web and GitHub to understand your assigned module and previous uses of it. Prefer official documentation and inspect both reference RTL and its testbench.

Create an English note named after the module, for example `uart.md`, `fifo.md`, `memory.md`, `sobel.md` or `vga.md`.

## Note template

1. Module purpose and operating principle.
2. Role and data flow in our project.
3. Useful documentation and previous implementations, with links.
4. Reference code studied and how its data/control paths work.
5. Proposed interface and timing assumptions.
6. Changes needed for our board and architecture.
7. Verification plan and expected results.
8. Open questions to discuss with Essam and neighboring module owners.

## Search examples

- `UART RX TX Verilog FPGA testbench`
- `synchronous FIFO Verilog full empty testbench`
- `FPGA dual port RAM frame buffer Verilog read latency`
- `Sobel FPGA Verilog line buffer 3x3 window`
- `VGA controller Verilog pixel clock hsync vsync`

Study asynchronous FIFO designs if the selected architecture crosses clock domains. Record which reference ideas are reused and retain the required attribution.
