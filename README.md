# Optimized Miner for FXL

Experimental CUDA-optimized FusionHash miner for NVIDIA GPUs, with HiveOS support and full compatibility with existing pools and HiveOS flight sheets.

## Supported GPUs

- GTX 10 Series
- RTX 20 Series
- RTX 30 Series
- RTX 40 Series
- RTX 50 Series

## Improvements

- Added native CUDA builds optimized for Pascal, Turing, Ampere, Ada Lovelace, and Blackwell GPUs.
- Added automatic per-GPU launch tuning for better out-of-the-box performance.
- Improved CUDA kernel performance.
- Added faster parallel initialization for multi-GPU rigs.
- Fixed HiveOS dashboard statistics.
- Preserved compatibility with existing pools and HiveOS flight sheets.

## Tested Performance

| GPU | Hashrate | Core Clock Offset | Lock Core Clock | Memory Clock | Power Limit |
|---|---:|---:|---:|---:|---:|
| GTX 1080 Ti | ~2.3 kH/s | +150 | 1800 MHz | Default 5000 MHz | 215 W |
| RTX 3060 Ti | ~2.8 kH/s | +200 | 1800 MHz | Lock 5001 MHz | 160 W |
| RTX 3070 | ~3.2 kH/s | +175 | 1800 MHz | Lock 5001 MHz | 175 W |
| RTX 3080 | ~4.8 kH/s | +175 | 1750 MHz | Lock 5001 MHz | 270 W |
| RTX 3080 Ti | ~5.6 kH/s | +175 | 1750 MHz | Lock 5001 MHz | 290 W |
| RTX 4090 | ~10.0+ kH/s | +200 | 2400 MHz | Lock 5001 MHz | 360 W |

Pool shares were accepted with zero rejected shares during testing.

## Developer Fee

- Includes a 2% developer fee.
