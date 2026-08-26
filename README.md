<p align="center">
  <a href="https://discord.gg/8wPbSHUYXs">
    <img src="https://img.shields.io/badge/Discord-Join%20the%20Community-5865F2?logo=discord&logoColor=white" alt="Join the Fl4shMiner Discord">
  </a>
</p>
<img width="1254" height="1254" alt="01_fl4shminer_original_red_gold_dark_background" src="https://github.com/user-attachments/assets/fc85a95e-2138-4d34-9b48-444066f411a1" />

Fl4shMiner is a GPU miner for NVIDIA CUDA and AMD OpenCL devices. It supports Windows and HiveOS and is designed for compatibility with existing mining pools and HiveOS flight sheets.

## Supported Algorithms

- [PearlHash (PRL)](#pearlhash-prl)
- [Cryptix-OX8 (CPAY)](#cryptix-ox8-cpay)
- [SHA256d (CSD)](#sha256d-csd)
- [FusionHash (FXL)](#fusionhash-fxl)
- [Parano1d / Poseidon2b (NOID)](#parano1d--poseidon2b-noid)

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

> **PearlHash support:** RTX 30 Series (Ampere) and RTX 40 Series (Ada Lovelace). Additional NVIDIA architectures are planned for future releases.
>
> **Parano1d / NOID support:** RTX 30 Series (SM86), RTX 40 Series (SM89), and RTX 50 Series (SM120).

### AMD (FXL and CPAY)

- RX 400 Series
- RX 500 Series
- RX Vega Series
- RX 5000 Series
- RX 6000 Series
- RX 7000 Series
- AMD Workstation GPUs

## Features and Improvements

- Native CUDA builds optimized for Pascal, Turing, Ampere, Ada Lovelace, and Blackwell GPUs.
- PearlHash CUDA kernels optimized for Ampere and Ada Lovelace GPUs.
- Poseidon2b (NOID) CUDA kernels optimized for SM86, SM89, and SM120 GPUs.
- Automatic per-GPU launch tuning for improved out-of-the-box performance.
- Optimized CUDA kernels.
- Faster parallel initialization for multi-GPU rigs.
- HiveOS dashboard statistics support.
- Compatibility with existing mining pools and HiveOS flight sheets.
- NVIDIA CUDA and AMD OpenCL support.

---

---

## PearlHash (PRL)

Fl4shMiner supports PearlHash mining for Pearl (PRL) on NVIDIA RTX 20 Series, RTX 30 Series, RTX 40 Series GPUs and RTX 50 Series GPUs.

### Command-Line Example

```bash
-a pearlhash -pool stratum+tcp://br.pearl.herominers.com:1200 -w %WAL%.%WORKER_NAME% -pass x
```

Replace `%WAL%` with your PRL wallet address and `%WORKER_NAME%` with the desired name for your mining rig.

### Tested Performance

Hashrates below used Fl4shMiner v1.2.1.

| GPU | Hashrate | Core Clock Offset | Locked Core Clock | Memory Clock | Power Limit |
|---|---:|---:|---:|---:|---:|
| RTX 3060 Ti | ~68.00 TH/s | +225 MHz | 1825 MHz | Locked at 5001 MHz | 168 W |
| RTX 3070 | ~75.00 TH/s | +250 MHz | 1650 MHz | Locked at 5001 MHz | 175 W |
| RTX 3080 | ~108.54 TH/s | +250 MHz | 1605 MHz | Locked at 5001 MHz | 262 W |
| RTX 3080 Ti | ~128.00 TH/s | +250 MHz | 1605 MHz | Locked at 5001 MHz | 295 W |
| RTX 4090 | ~316.00 TH/s | +300 MHz | 2505 MHz | Locked at 5001 MHz | 398 W |

Pool shares were accepted with zero rejected shares during testing.

> Performance may vary depending on GPU model, silicon quality, driver version, operating system, cooling, and overclock settings.

### Developer Fee

PearlHash mining for PRL includes a **1.5% developer fee**.

### HiveOS Configuration

[View or download the PearlHash (PRL) HiveOS configuration](configs/hiveos/fl4shminer-prl.json)

Import `fl4shminer-prl.json` into HiveOS to create the preconfigured flight sheet.

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
| GTX 1080 Ti | ~1.90 GH/s | +150 MHz | 1911 MHz | Locked at 810 MHz | 205 W |
| RTX 3060 Ti | ~1.90 GH/s | +200 MHz | 1825 MHz | Locked at 810 MHz | 100 W |
| RTX 3070 | ~2.17 GH/s | +200 MHz | 1825 MHz | Locked at 810 MHz | 115 W |
| RTX 3080 | ~3.43 GH/s | +200 MHz | 1800 MHz | Locked at 810 MHz | 299 W |
| RTX 3080 Ti | ~4.07 GH/s | +200 MHz | 1800 MHz | Locked at 810 MHz | 220 W |
| RTX 4090 | ~9.60 GH/s | +200 MHz | 2800 MHz | Locked at 5001 MHz | 389 W |

Pool shares were accepted with zero rejected shares during testing.

> Performance may vary depending on GPU model, silicon quality, driver version, operating system, cooling, and overclock settings.

### Developer Fee

SHA256d mining for CSD includes a **1% developer fee**.

### HiveOS Configuration

[View or download the SHA256d (CSD) HiveOS configuration](configs/hiveos/fl4shminer-csd.json)

Import `fl4shminer-csd.json` into HiveOS to create the preconfigured flight sheet.

[Back to Supported Algorithms](#supported-algorithms)

---

## FusionHash (FXL)

### Command-Line Example

```bash
-a fusionhash -pool wss://us-east.coin-miners.info:8443 -w %WAL%.%WORKER_NAME% -pass x
```

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

## Parano1d / Poseidon2b (NOID)

Fl4shMiner supports Poseidon2b mining for NOID on NVIDIA RTX 30 Series, RTX 40 Series, and RTX 50 Series GPUs. Native CUDA kernels are provided for SM86, SM89, and SM120, with automatic architecture dispatch and workload tuning.

Supported algorithm aliases are `noid`, `no1d`, `parano1d`, and `poseidon2b`. The implementation includes full 128-bit nonce handling with CPU/GPU result verification.

### Command-Line Example

```bash
-a noid -pool https://pool.ariabrain.com/noid-rpc/ -w "%WALLET%.%WORKER%" -pass x
```

Use your NOID wallet address as the login and payout address. Optional worker names use the `wallet.worker` format.

### Tested Performance

| GPU | Hashrate | Core Clock | Memory Clock | Power | Efficiency |
|---|---:|---:|---:|---:|---:|
| RTX 3080 Ti | ~26.97 MH/s | 1605 MHz | 5001 MHz | 148.71 W | 0.181 MH/s/W |
| RTX 4090 | ~73.02 MH/s | 2730 MHz | 10251 MHz | 256.13 W | 0.285 MH/s/W |
| RTX 5080 | ~50.29 MH/s | 2865 MHz | 14801 MHz | 178.31 W | 0.282 MH/s/W |

> NOID figures above are fixed-work engineering measurements. Live pool results may be lower during normal node proof-preparation gaps.
>
> Performance may vary depending on GPU model, silicon quality, driver version, operating system, cooling, and overclock settings.

### Developer Fee

Poseidon2b mining for NOID includes a **3% developer fee**, calculated from completed work.

### AriaPool Integration

Fl4shMiner supports [AriaPool NOID](https://pool.ariabrain.com/noid.html) directly.

- Endpoint: `https://pool.ariabrain.com/noid-rpc/`
- Your NOID wallet address is your login and payout address.
- Optional worker names use `wallet.worker`.

[Back to Supported Algorithms](#supported-algorithms)
