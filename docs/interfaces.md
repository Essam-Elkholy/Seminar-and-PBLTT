# Interface agreement worksheet

Status: proposed worksheet. Values marked TBD are not approved specifications.

Owner: Essam coordinates; each module owner contributes and agrees with neighboring owners before RTL implementation.

## System decisions

| Item | Agreed value |
| --- | --- |
| FPGA board and part | TBD |
| Toolchain | TBD |
| Clock frequency and domains | TBD |
| Reset polarity, timing and frame restart behavior | TBD |
| Image width and height | TBD |
| Pixel width and row/column ordering | TBD |
| Frame start/end protocol | TBD |
| UART baud rate and framing | TBD |
| FIFO type, depth and flow control | TBD |
| Memory ports and read latency | TBD |
| Sobel threshold and arithmetic policy | TBD |
| Border policy and output coordinates/count | TBD |
| VGA timing mode | TBD |

## Module worksheet

Complete one entry for each RTL module:

- Module name and owner:
- Purpose and connected modules:
- Port names, directions and widths:
- Clock domain:
- Reset behavior:
- Valid/ready, enable or request/response semantics:
- Data acceptance condition:
- Latency and stall behavior:
- Parameters and supported values:
- Frame/boundary behavior:
- Error conditions and handling:
- Acceptance tests:
- Review date and agreement from affected owners:

For ready/valid interfaces, document when a transfer is accepted and whether data must remain stable while stalled. Align validity with the corresponding data. Advance pixel/address counters on accepted transfers, according to the selected protocol. If different clock domains are used, explicitly define and review the crossing mechanism.
