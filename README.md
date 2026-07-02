# Optimized Miner for FXL

Experimental CUDA-optimized FusionHash miner for NVIDIA GPUs, with HiveOS support and full compatibility with existing pools and flight sheets.

Supported GPUs:

GTX 10 Series
RTX 20 Series
RTX 30 Series
RTX 40 Series
RTX 50 Series
Improvements:

Added native CUDA builds optimized for Pascal, Turing, Ampere, Ada Lovelace, and Blackwell GPUs.
Added automatic per-GPU launch tuning for better out-of-the-box performance.
Improved CUDA kernel performance.
Added faster parallel initialization for multi-GPU rigs.
Fixed HiveOS dashboard statistics.
Preserved compatibility with existing pools and HiveOS flight sheets.
Tested Performance:

GTX 1080 Ti: approximately 2.3 kH/s per GPU. Core Clock Offset 150, Lock Core Clock 1800, Default Memory Clock 5001, PL 215W
RTX 3060 Ti: approximately 2.8 kH/s per GPU. Core Clock Offset 200, Lock Core Clock 1800, Lock Memory Clock 5001, PL 160W
RTX 3070: approximately 3.2 kH/s per GPU. Core Clock Offset 175, Lock Core Clock 1800, Lock Memory Clock 5001, PL 175W
RTX 3080: approximately 4.8 kH/s per GPU. Core Clock Offset 175, Lock Core Clock 1750, Lock Memory Clock 5001, PL 270W
RTX 3080 Ti: approximately 5.6 kH/s per GPU. Core Clock Offset 175, Lock Core Clock 1750, Lock Memory Clock 5001, PL 290W
RTX 4090: approximately 10.0 kH/s+ per GPU. Core Clock Offset 200, Lock Core Clock 2400, Lock Memory Clock 5001, PL 360W
Pool shares were accepted with zero rejected shares during testing.
Developer Fee:

Includes a 2% developer fee.
