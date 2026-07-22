# Fl4shMiner

Fl4shMiner is a GPU miner for NVIDIA CUDA and AMD OpenCL devices. It supports Windows and HiveOS and is designed for compatibility with existing mining pools and HiveOS flight sheets.

## Supported Algorithms

- [FusionHash (FXL)](#fusionhash-fxl)
- [Cryptix-OX8 (CPAY)](#cryptix-ox8-cpay)
- [SHA256d (CSD)](#sha256d-csd)

## Supported GPUs

### NVIDIA

- GTX 10 Series
- GTX 16 Series
- RTX 20 Series
- RTX 30 Series
- RTX 40 Series
- RTX 50 Series
- NVIDIA CMP Mining GPUs
- NVIDIA Workstation GPUs

### AMD

- RX 400 Series
- RX 500 Series
- RX Vega Series
- RX 5000 Series
- RX 6000 Series
- RX 7000 Series
- AMD Workstation GPUs

## Features and Improvements

- Native CUDA builds optimized for Pascal, Turing, Ampere, Ada Lovelace, and Blackwell GPUs.
- Automatic per-GPU launch tuning for improved out-of-the-box performance.
- Optimized CUDA kernels.
- Faster parallel initialization for multi-GPU rigs.
- HiveOS dashboard statistics support.
- Compatibility with existing mining pools and HiveOS flight sheets.
- NVIDIA CUDA and AMD OpenCL support.

---

## FusionHash (FXL)

### Tested Performance

| GPU | Hashrate | Core Clock Offset | Locked Core Clock | Memory Clock | Power Limit |
|---|---:|---:|---:|---:|---:|
| GTX 1080 Ti | ~2.3 kH/s | +150 MHz | 1800 MHz | Default 5000 MHz | 215 W |
| RTX 3060 Ti | ~2.8 kH/s | +200 MHz | 1800 MHz | Locked at 5001 MHz | 160 W |
| RTX 3070 | ~3.2 kH/s | +175 MHz | 1800 MHz | Locked at 5001 MHz | 175 W |
| RTX 3080 | ~4.8 kH/s | +175 MHz | 1750 MHz | Locked at 5001 MHz | 270 W |
| RTX 3080 Ti | ~5.6 kH/s | +175 MHz | 1750 MHz | Locked at 5001 MHz | 290 W |
| RTX 4090 | ~10.0+ kH/s | +200 MHz | 2400 MHz | Locked at 5001 MHz | 360 W |

Pool shares were accepted with zero rejected shares during testing.

> Performance may vary depending on GPU model, silicon quality, driver version, operating system, cooling, and overclock settings.

### Developer Fee

FusionHash mining includes a **2% developer fee**.

### HiveOS Configuration

[View or download the FusionHash HiveOS configuration](configs/hiveos/fl4shminer-fxl.json)

Import `fl4shminer-fxl.json` into HiveOS to create the preconfigured flight sheet.

[Back to Supported Algorithms](#supported-algorithms)

---

## Cryptix-OX8 (CPAY)

Cryptix-OX8, also known as Cryptix, is supported on both NVIDIA and AMD GPUs.

### Command-Line Example

```bash
-a cryptix -pool stratum+tcp://cytx.baikalmine.com:9010 -w %WAL%.%WORKER_NAME% -pass x
```

### Tested Performance

| GPU | Hashrate | Core Clock Offset | Locked Core Clock | Memory Clock | Power Limit |
|---|---:|---:|---:|---:|---:|
| Radeon RX 5700 XT | ~50.0 MH/s | N/A | 1850 MHz | 1 MHz | 140 W |
| GTX 1080 Ti | ~58.0 MH/s | +150 MHz | 1825 MHz | -2000 MHz | 200 W |
| RTX 3060 Ti | ~108.0 MH/s | +200 MHz | 1825 MHz | Locked at 5001 MHz | 140 W |
| RTX 3070 | ~125.0 MH/s | +200 MHz | 1750 MHz | Locked at 5001 MHz | 155 W |
| RTX 3080 | ~179.5 MH/s | +200 MHz | 1725 MHz | Locked at 5001 MHz | 250 W |
| RTX 3080 Ti | ~211.0 MH/s | +175 MHz | 1710 MHz | Locked at 5001 MHz | 260 W |
| RTX 4090 | ~460.0 MH/s | +200 MHz | 2700 MHz | Locked at 5001 MHz | 360 W |

Pool shares were accepted with zero rejected shares during testing.

> Performance may vary depending on GPU model, silicon quality, driver version, operating system, cooling, and overclock settings.

### Developer Fee

Cryptix-OX8 mining includes a **1% developer fee**.

### HiveOS Configuration

[View or download the Cryptix-OX8 HiveOS configuration](configs/hiveos/fl4shminer-cryptix.json)

Import `fl4shminer-cryptix.json` into HiveOS to create the preconfigured flight sheet.

[Back to Supported Algorithms](#supported-algorithms)

---

## SHA256d (CSD)

Fl4shMiner supports SHA256d mining for CSD on NVIDIA GPUs.

### Command-Line Example

```bash
-a csd -pool stratum+tcp://csd-us-east.lproute.com:8760 -w 0xYOUR_WALLET_ADDRESS.WORKER_NAME -pass x
```

Replace `0xYOUR_WALLET_ADDRESS` with your CSD wallet address and `WORKER_NAME` with the desired name for your mining rig.

### Tested Performance

| GPU | Hashrate | Core Clock Offset | Locked Core Clock | Memory Clock | Power Limit |
|---|---:|---:|---:|---:|---:|
| GTX 1080 Ti | ~58.0 MH/s | +150 MHz | 1825 MHz | -2000 MHz | 200 W |
| RTX 3060 Ti | ~108.0 MH/s | +200 MHz | 1825 MHz | Locked at 5001 MHz | 140 W |
| RTX 3070 | ~125.0 MH/s | +200 MHz | 1750 MHz | Locked at 5001 MHz | 155 W |
| RTX 3080 | ~179.5 MH/s | +200 MHz | 1725 MHz | Locked at 5001 MHz | 250 W |
| RTX 3080 Ti | ~211.0 MH/s | +175 MHz | 1710 MHz | Locked at 5001 MHz | 260 W |
| RTX 4090 | ~460.0 MH/s | +200 MHz | 2700 MHz | Locked at 5001 MHz | 360 W |

Pool shares were accepted with zero rejected shares during testing.

> Performance may vary depending on GPU model, silicon quality, driver version, operating system, cooling, and overclock settings.

### Developer Fee

SHA256d mining for CSD includes a **1% developer fee**.

### HiveOS Configuration

[View or download the SHA256d (CSD) HiveOS configuration](configs/hiveos/fl4shminer-csd.json)

Import `fl4shminer-csd.json` into HiveOS to create the preconfigured flight sheet.

[Back to Supported Algorithms](#supported-algorithms)
