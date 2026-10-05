# System architecture

## Planned baseline

The project will receive grayscale image data, form 3x3 windows, compute Sobel edges and store/output the result on FPGA. Python will prepare image data and provide a matching reference model.

A candidate data path is:

```text
PC -> UART RX -> input FIFO -> line buffers -> Sobel
   -> output frame buffer -> VGA / UART TX -> PC
```

This is a planning outline, not an implemented or frozen architecture. Frame-buffer port sharing, control sequencing and any clock-domain crossings must be agreed before integration.

## Decisions to confirm

- FPGA board, part and toolchain.
- Image dimensions, grayscale representation and pixel order.
- UART framing, baud rate and frame transfer protocol.
- Clock domains, resets and buffering strategy.
- FIFO depth and overflow/underflow handling.
- Memory ports, read latency and access ownership.
- Window coordinates, border policy and frame boundaries.
- Sobel arithmetic, threshold and pipeline latency.
- VGA mode and placement of the processed image.
- End-of-frame signaling and error handling.

See [interfaces.md](interfaces.md). Complete and review the baseline before introducing optional preprocessing or parameter-search extensions.
