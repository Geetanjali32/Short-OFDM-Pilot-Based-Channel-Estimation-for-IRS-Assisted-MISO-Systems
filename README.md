# Short-OFDM Pilot-Based Channel Estimation for IRS-Assisted MISO Systems

## Overview

This project develops a low-complexity, short-OFDM pilot-based Least Squares (LS) channel estimation framework for Intelligent Reflecting Surface (IRS)-assisted Multiple-Input Single-Output (MISO) OFDM systems.

The proposed approach estimates both direct and cascaded channel components while reducing training duration through pilot reuse across multiple IRS configurations.

## Objectives

- Develop an LS-based channel estimation framework for IRS-assisted MISO-OFDM systems.
- Reduce pilot overhead using short OFDM training symbols.
- Establish channel identifiability conditions using the rank of the stacked pilot matrix.
- Derive a closed-form LS estimator and analytical Normalized Mean Square Error (NMSE) expression.
- Evaluate the impact of IRS phase design, pilot length, phase quantization, and phase errors.

## Proposed Methodology

1. **System Modeling:** Model the direct BS-user channel and cascaded BS-IRS-user channels under frequency-selective fading.

2. **Pilot Design:** Reuse the same mutually orthogonal pilot sequences across different IRS reflection configurations.

3. **Channel Estimation:** Develop a closed-form LS estimator using a compact matrix representation of the channel.

4. **Identifiability Analysis:** Establish the full-column-rank condition for the stacked pilot matrix, with the minimum pilot length requirement:

   \[
   N_0 \geq L N_t
   \]

5. **Performance Analysis:** Derive the estimation error and NMSE expressions and evaluate the framework under different channel and IRS configurations.

## Key Contributions

- Short-OFDM pilot-based LS channel estimation for IRS-assisted MISO systems.
- Pilot sequence reuse across \(M+1\) IRS configurations.
- Explicit rank conditions for full channel identifiability.
- Analytical NMSE derivation for the proposed estimator.
- Evaluation of DFT-based and random IRS phase configurations.
- Investigation of practical IRS impairments, including phase quantization and phase errors.

## Simulation Setup

| Parameter | Value |
|---|---|
| BS transmit antennas | 10 |
| IRS reflecting elements | 64 |
| Pilot lengths | 320, 384, 448, 512 |
| BS-IRS channel delay spread | 16 |
| IRS-user channel delay spread | 17 |
| Direct channel delay spread | 32 |
| Channel models | Rayleigh and Rician (K = 4) |
| IRS phase errors | 0°, 15°, 30°, 45° |
| Cyclic prefix length | 31 or greater |
| Monte Carlo trials | 10,000 |

## Simulation Results

The framework is evaluated through the following experiments:

- **NMSE vs. SNR:** Comparison of DFT-based and random IRS phase configurations under Rayleigh and Rician fading.
- **Pilot Length Analysis:** Investigation of the effect of pilot length on channel estimation accuracy.
- **Phase Quantization:** Evaluation of estimation performance with different IRS phase-shifter resolutions.
- **IRS Phase Errors:** Analysis of the impact of practical phase-control imperfections on NMSE.

### Key Observations

- DFT-based orthogonal IRS phase configurations achieve lower NMSE than random phase configurations.
- Rician fading performs better than Rayleigh fading in the evaluated scenarios.
- Increasing pilot length improves estimation accuracy but increases training duration.
- Increasing phase quantization resolution improves estimation accuracy at the cost of hardware complexity.
- IRS phase imperfections become more significant at higher SNR values.

## Technologies

- MATLAB
- Digital Signal Processing
- OFDM and MISO Systems
- Intelligent Reflecting Surfaces (IRS)
- Least Squares (LS) Estimation
- Channel Modeling and Simulation
- Normalized Mean Square Error (NMSE) Analysis

## Future Research Directions

- Integrating OMP-based sparse recovery to identify dominant channel taps.
- Reducing estimation complexity through reduced-dimensional LS estimation.
- Exploring more efficient pilot and IRS phase designs.
