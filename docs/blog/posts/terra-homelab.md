---
title: Building a Compact Homelab
date: 2026-01-03
author: Joe Hawley
description: Documenting the build of a quiet, efficient small-form-factor homelab server using the Fractal Design Terra Jade case and AMD Ryzen 7 9700X for virtualization, containers, development, and network security tasks.
tags: [homelab, pc-build, sffpc, amd-ryzen, fractal-design, hardware]
---

# Building a Compact Homelab: Fractal Terra with Ryzen 7

![How I meditate - Bliss](../../images/builds/jade/bliss.jpg){ alt="Building a Compact Homelab" .float-right width=225 }

This project documents the ongoing build of a small-form-factor (SFF) homelab server housed in the beautiful Fractal Design Terra Jade case (with walnut front panel). The primary goals are a **quiet, power-efficient, always-on system** capable of:

- KVM virtualization
- Docker/Podman containers
- Development work and graduate research
- Network IDS/IPS using Suricata

<!-- more -->

## Build Process Gallery

<div class="grid cards" markdown>

- ![Box of Parts](../../images/builds/jade/00_boxed.jpg){ loading=lazy }
  _Box of parts_

- ![Unboxed Boxes - Core Components](../../images/builds/jade/01_unboxed_boxes.jpg){ loading=lazy }
  _Unboxed boxes - Core components_

- ![Boxes Unboxed - The Fun Begins](../../images/builds/jade/02_boxes_unboxed.jpg){ loading=lazy }
  _Boxes unboxed - The fun begins_

- ![Corsair SF750](../../images/builds/jade/03_unboxed_psu.jpg){ loading=lazy }
  _Corsair SF750_

- ![Noctua NH-L12S](../../images/builds/jade/04_unboxed_cpu_cooler.jpg){ loading=lazy }
  _Noctua NH-L12S_

- ![Noctua NF-A12x25](../../images/builds/jade/05_unboxed_case_fan.jpg){ loading=lazy }
  _Noctua NF-A12x25_

- ![G.SKILL Trident Z5 Neo RGB](../../images/builds/jade/06_unboxed_ram.jpg){ loading=lazy }
  _G.SKILL Trident Z5 Neo RGB_

- ![AMD Ryzen 7 9700X](../../images/builds/jade/07_unboxed_cpu.jpg){ loading=lazy }
  _AMD Ryzen 7 9700X_

- ![MSI MPG B850I Edge](../../images/builds/jade/08_unboxed_mobo.jpg){ loading=lazy }
  _MSI MPG B850I Edge_

- ![CPU Installation](../../images/builds/jade/09_install_cpu.jpg){ loading=lazy }
  _CPU Installation_

- ![RAM Installation](../../images/builds/jade/10_install_ram.jpg){ loading=lazy }
  _RAM Installation_

- ![Cooler Brackets Installation](../../images/builds/jade/11_install_cpu_cooler_brackets.jpg){ loading=lazy }
  _Cooler Brackets Installation_

- ![CPU Cooler Installation](../../images/builds/jade/12_install_cpu_cooler.jpg){ loading=lazy }
  _CPU Cooler Installation_

- ![Core Assembly](../../images/builds/jade/13_core_assembly.jpg){ loading=lazy }
  _Core Assembly_

- ![Test Bench Ready](../../images/builds/jade/14_test_bench_ready.jpg){ loading=lazy }
  _Test Bench Ready_

- ![From Boxes to BIOS](../../images/builds/jade/15_bios.jpg){ loading=lazy }
  _From Boxes to BIOS_

- ![Ubuntu Live!](../../images/builds/jade/16_ubuntu_live.jpg){ loading=lazy }
  _Ubuntu Live!_

- ![T-minus RGB](../../images/builds/jade/17_rgb.jpg){ loading=lazy }
  _T-minus RGB..._

</div>

## Parts List

| # | Component | Details |
|---|-----------|---------|
| 1 | **Case** | Fractal Design Terra Jade (walnut front panel) |
| 2 | **CPU** | AMD Ryzen 7 9700X (8-core/16-thread, 65W TDP) |
| 3 | **CPU Cooler** | Noctua NH-L12S (low-profile, 120mm fan) |
| 4 | **Motherboard** | MSI MPG B850I Edge Ti WiFi (AM5 Mini-ITX) |
| 5 | **RAM** | G.SKILL Trident Z5 Neo RGB 64GB (2×32GB) DDR5-6000 EXPO |
| 6 | **Storage** | Samsung 990 PRO 2TB PCIe Gen4 M.2 |
| 7 | **PSU** | Corsair SF750 (2024) 80+ Platinum SFX |
| 8 | **Case Fans** | 2× Noctua NF-A12x25 PWM (120mm) |
| 9 | **Top Fan Bracket** | 25mm thick Etsy bracket for second intake fan |

## Build Progress So Far

I've received and unboxed the CPU, cooler, motherboard, RAM, PSU, and one case fan. Assembly started with an open-air test bench on cardboard to validate core components before final case installation.

- Installed Ryzen 7 9700X and RAM in slots A2/B2.
- Mounted NH-L12S with standard bars in diagonal orientation for VRM clearance.
- Switched the cooler fan to top position (intake blowing down) to ensure 44mm RAM clearance.
- Connected 24-pin ATX, 8-pin EPS, cooler fan to CPU_FAN header, and one case fan to SYS_FAN.
- First POST successful! :sunglasses:
- Enabled AMD EXPO profile and High-Efficiency Mode in BIOS → Confirmed 6000 MT/s memory speed.
- Booted Ubuntu 24.04 LTS live USB.
- Ran `inxi`, `sensors`, and a 5-minute `stress-ng` (16 threads) test:
  - Peak temperature: **50.6°C** (open air)
  - No thermal throttling or stability issues

The top fan bracket has arrived. Still awaiting the Terra case itself, the Samsung 990 PRO 2TB drive, and the second NF-A12x25 fan for final assembly and full Ubuntu installation.

The core system is now fully validated: stable, remarkably cool, and running at rated specifications on an open-air test bench. I'm excited to move everything into the beautiful Fractal Terra Jade case soon. Final assembly, meticulous cable management, Suricata IDS/IPS configuration, and full noise/power benchmarks are next once the remaining parts arrive.

Stay tuned for the completed build and real-world performance results!

*Joe Hawley*  
Fortune 500 Director | CISSP  
M.S. Cybersecurity Graduate Student @ Georgia Institute of Technology