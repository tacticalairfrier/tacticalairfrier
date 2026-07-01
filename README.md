# Chinmay Tupkari

First-year ECE undergrad @ IIIT Nagpur, building toward VLSI/ASIC design roles. I go C golden model → RTL → verification → synthesis, and I try to take everything to gate level, not just simulation.

## What I've built

**AES-128 crypto core** — Encrypt, InvCipher, and EqInvCipher datapaths, verified against 2000 NIST test vectors using a self-written C golden model (which caught an InvSBox bug the official vectors missed). Synthesized in Vivado for Basys3 (Artix-7), with ROM inference confirmed for SBox/InvSBox. Hardware bring-up in progress via ILA/VIO.

**SPI master/slave controller** — Taken through the full OpenLane 2 / Sky130 flow to GDS2. My most complete open-source silicon flow to date.

**UART TX/RX** — 8E1 framing, 16x oversampling, verified on real Basys3 hardware against an Arduino testbench.

**Foundational RTL** — Johnson counter, JK-based binary counter with parallel load, universal shift register, traffic light FSM, 16-bit parameterizable ALU. All in Verilog with testbenches, synthesized through Yosys.

**Infra** — Dedicated Debian laptop running the OpenLane/Sky130 flow via Nix; Fedora as my daily driver.

## Where this is going

Long-term target: a security coprocessor SoC — **RV32I + AES-128 + SHA-256 + HMAC + CSRNG** — with [OpenTitan Darjeeling](https://opentitan.org/) as an architectural reference, aiming at a Sky130 MPW tapeout. Interface strategy: AXI-lite for the SoC, ILA/VIO for FPGA-side bring-up.

Immediate roadmap:
- Finish AES-128 hardware bring-up on Basys3
- RV32I golden model (C first, as always) alongside an NPTEL RTL-to-GDS2 course
- Start integrating crypto blocks toward the SoC goal

## Toolchain

`iverilog` · `GTKWave` · `Yosys` · `OpenLane 2` · `Sky130 PDK` · `Vivado`

---
📍 Pune / Nagpur, India — open to VLSI internships
