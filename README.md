# Fl4shMiner

Fl4shMiner is a GPU miner for NVIDIA CUDA and AMD OpenCL devices. It supports Windows and HiveOS and is designed for compatibility with existing mining pools and HiveOS flight sheets.

## Supported Algorithms

* [FusionHash (FXL)](#fusionhash-fxl)
* [Cryptix-OX8 (CPAY)](#cryptix-ox8-cpay)

## Supported GPUs

### NVIDIA

* GTX 10 Series
* GTX 16 Series
* RTX 20 Series
* RTX 30 Series
* RTX 40 Series
* RTX 50 Series
* NVIDIA CMP Mining GPUs
* NVIDIA Workstation GPUs

### AMD

* RX 400 Series
* RX 500 Series
* RX Vega Series
* RX 5000 Series
* RX 6000 Series
* RX 7000 Series
* AMD Workstation GPUs

## Features and Improvements

* Native CUDA builds optimized for Pascal, Turing, Ampere, Ada Lovelace, and Blackwell GPUs.
* Automatic per-GPU launch tuning for improved out-of-the-box performance.
* Optimized CUDA kernels.
* Faster parallel initialization for multi-GPU rigs.
* HiveOS dashboard statistics support.
* Compatibility with existing mining pools and HiveOS flight sheets.
* NVIDIA CUDA and AMD OpenCL support.

---

## FusionHash (FXL)

### Tested Performance

| GPU         |    Hashrate | Core Clock Offset | Locked Core Clock |       Memory Clock | Power Limit |
| ----------- | ----------: | ----------------: | ----------------: | -----------------: | ----------: |
| GTX 1080 Ti |   ~2.3 kH/s |          +150 MHz |          1800 MHz |   Default 5000 MHz |       215 W |
| RTX 3060 Ti |   ~2.8 kH/s |          +200 MHz |          1800 MHz | Locked at 5001 MHz |       160 W |
| RTX 3070    |   ~3.2 kH/s |          +175 MHz |          1800 MHz | Locked at 5001 MHz |       175 W |
| RTX 3080    |   ~4.8 kH/s |          +175 MHz |          1750 MHz | Locked at 5001 MHz |       270 W |
| RTX 3080 Ti |   ~5.6 kH/s |          +175 MHz |          1750 MHz | Locked at 5001 MHz |       290 W |
| RTX 4090    | ~10.0+ kH/s |          +200 MHz |          2400 MHz | Locked at 5001 MHz |       360 W |

Pool shares were accepted with zero rejected shares during testing.

> Performance may vary depending on GPU model, silicon quality, driver version, operating system, cooling, and overclock settings.

### Developer Fee

FusionHash mining includes a **2% developer fee**.

### HiveOS Flight Sheet / Custom Miner Setup

| Field                      | Value                                                                                       |
| -------------------------- | ------------------------------------------------------------------------------------------- |
| Miner name                 | `fl4shminer`                                                                                |
| Installation URL           | `https://github.com/Fl4sh9174/Fl4shMiner/releases/download/v1.0.0/fl4shminer-v1.0.0.tar.gz` |
| Hash algorithm             | `---`                                                                                       |
| Wallet and worker template | `%WAL%.%WORKER_NAME%`                                                                       |
| Pool URL                   | `wss://us-east.coin-miners.info:8443`                                                       |
| Pass                       | Leave blank                                                                                 |
| Extra config arguments     | Leave blank                                                                                 |

<img width="844" height="873" alt="Fl4shMiner FusionHash HiveOS configuration" src="https://github.com/user-attachments/assets/ece3fed8-c0a6-4a50-83b7-fc39b572a498" />

[Back to Supported Algorithms](#supported-algorithms)

---

## Cryptix-OX8 (CPAY)

Cryptix-OX8, also known as Cryptix, is supported on both NVIDIA and AMD GPUs.

### Command-Line Example

```bash
-a cryptix -pool stratum+tcp://cytx.baikalmine.com:9010 -w %WAL%.%WORKER_NAME% -pass x
```

### Tested Performance

| GPU               |    Hashrate | Core Clock Offset | Locked Core Clock |       Memory Clock | Power Limit |
| ----------------- | ----------: | ----------------: | ----------------: | -----------------: | ----------: |
| Radeon RX 5700 XT |  ~48.2 MH/s |               N/A |          1850 MHz |              1 MHz |       135 W |
| GTX 1080 Ti       |  ~54.0 MH/s |          +150 MHz |          1825 MHz |          -2000 MHz |       200 W |
| RTX 3060 Ti       | ~106.0 MH/s |          +200 MHz |          1825 MHz | Locked at 5001 MHz |       140 W |
| RTX 3070          | ~123.5 MH/s |          +200 MHz |          1750 MHz | Locked at 5001 MHz |       155 W |
| RTX 3080          | ~177.5 MH/s |          +200 MHz |          1725 MHz | Locked at 5001 MHz |       250 W |
| RTX 3080 Ti       | ~210.2 MH/s |          +175 MHz |          1710 MHz | Locked at 5001 MHz |       260 W |
| RTX 4090          | ~616.6 MH/s |          +200 MHz |          2700 MHz | Locked at 5001 MHz |       399 W |

Pool shares were accepted with zero rejected shares during testing.

> Performance may vary depending on GPU model, silicon quality, driver version, operating system, cooling, and overclock settings.

### Developer Fee

Cryptix-OX8 mining includes a **1% developer fee**.

### HiveOS Flight Sheet / Custom Miner Setup

| Field                      | Value                                                                                       |
| -------------------------- | ------------------------------------------------------------------------------------------- |
| Miner name                 | `fl4shminer`                                                                                |
| Installation URL           | `https://github.com/Fl4sh9174/Fl4shMiner/releases/download/v1.1.0/fl4shminer-v1.1.0.tar.gz` |
| Hash algorithm             | `cryptix`                                                                                   |
| Wallet and worker template | `%WAL%.%WORKER_NAME%`                                                                       |
| Pool URL                   | `stratum+tcp://cytx.baikalmine.com:9010`                                                    |
| Pass                       | Leave blank                                                                                 |
| Extra config arguments     | Leave blank                                                                                 |

<img width="845" height="871" alt="Fl4shMiner Cryptix-OX8 HiveOS configuration" src="https://github.com/user-attachments/assets/2bb01c26-22a2-4e4c-8c16-f7fbb5203f88" />

[Back to Supported Algorithms](#supported-algorithms)
