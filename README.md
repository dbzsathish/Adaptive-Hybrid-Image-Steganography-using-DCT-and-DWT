📘 Adaptive Hybrid DCT–DWT Image Steganography
Hidden Data Embedding Using PRNG & QIM

This project implements an adaptive hybrid image steganography framework that embeds secret data inside images using a combination of Discrete Cosine Transform (DCT), Discrete Wavelet Transform (DWT), Quantization Index Modulation (QIM), and Pseudo Random Number Generator (PRNG).
It is designed to achieve high imperceptibility, robustness, and maximum embedding capacity while keeping the stego image visually identical to the original.

🔍 Project Overview

This system divides the image into 8×8 blocks and analyzes their characteristics using four metrics:

Entropy

Variance

Mean Square Error (MSE)

Normalized Cross-Correlation (NCC)

Based on these values, the algorithm decides whether each block is better suited for DCT-based or DWT-based embedding.
A PRNG ensures that embedding positions are randomized for enhanced security.
QIM is used to embed each bit with strong robustness against noise and compression.

The framework also includes:
✔ Payload-vs-Quality Graphs (SSIM & PSNR)
✔ Histogram Comparison
✔ RMSE Calculations
✔ Maximum Capacity Estimation
✔ Iterative Repair Mechanism (for bit correction)

✨ Key Features

Hybrid Transform Embedding (DCT + DWT)
Automatically selects the best transform for every block based on image features.

Adaptive Block Analysis
Uses entropy, variance, MSE, and NCC to determine embedding suitability.

High Security via PRNG
Randomized embedding positions ensure resistance to steganalysis.

Robust QIM-Based Embedding
Maintains reliability even after compression and noise.

Performance Metrics Included

SSIM

PSNR

BER

RMSE

Histogram Intersection

Very High Embedding Capacity
Utilizes both DCT and DWT carriers in every block.

📊 Example Results

From a sample 256×256 grayscale image:

Total Carriers: 60,566

Effective Capacity: 57,537 bits

Accuracy: 98.56%

PSNR: 32.77 dB

SSIM: 0.762

Histogram Intersection: ~0.99 (almost identical distributions)

These results confirm that the stego image remains visually unchanged while successfully embedding a large payload.

🚀 How It Works (Pipeline)

Upload cover image

Divide into 8×8 blocks

Extract entropy, variance, MSE, NCC per block

Adaptive selection:

High entropy + variance → DCT

High MSE + NCC → DWT

Generate PRNG sequence for security

Embed bits using QIM in selected frequency coefficients

Reconstruct stego image

Extract & verify message bits

Evaluate quality metrics
