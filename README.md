# Parallel Pipelined FFT OFDM Implementation on GPU

A high-performance **OFDM transmitter and receiver** implemented entirely on NVIDIA GPU using **CUDA** and the **Cooley-Tukey FFT algorithm** from [cuda-fft](https://github.com/roguh/cuda-fft).

## Features
-  Uses radix-2 Cooley-Tukey FFT/IFFT (via `cuda-fft`)
-  Batched parallel processing of 1024+ OFDM symbols
-  QPSK modulation/demodulation with cyclic prefix
-  BER calculation and performance validation
-  Modern CMake + CUDA language support (no legacy FindCUDA)

## 🛠 Build Instructions

```bash
git clone https://github.com/YennetiNitinSreeVenkat/ofdm-cuda-pipelined.git
cd ofdm-cuda-pipelined
mkdir build && cd build
cmake ..
make -j4
./ofdm_project
