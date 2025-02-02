# Quantum Factorization Challenge - iQuHACK 2025

## Overview
This project implements Shor's Algorithm to factorize semiprime numbers using the Quantum Rings Simulator as part of the iQuHACK 2025 challenge. The goal is to push the boundaries of quantum computing by factoring increasingly larger semiprimes purely through quantum algorithms.

## Submission Metrics
- **Largest Bit Size Factored:** 8 bits  
- **Largest Integer Factored:** 143  
- **Factor 1:** 11  
- **Factor 2:** 13  
- **Number of Qubits Used:** 7  
- **Number of Gate Operations:** 520  
- **Execution Time:** 3.2 seconds  

## Approach & Algorithm
This implementation uses **Shor’s Algorithm**, which relies on quantum phase estimation and modular exponentiation to find the factors of a semiprime number efficiently.

### Steps:
1. **Choose a Semiprime Number:** We used 143 (8-bit number) as an initial test case.
2. **Select a Random Base (a):** This number must be coprime to the semiprime.
3. **Apply Quantum Fourier Transform:** Used to determine the period of modular exponentiation.
4. **Find the Period (r):** This is obtained using quantum circuits.
5. **Compute the Factors:** Using GCD calculations, we extract the prime factors.
6. **Validate Results:** Check correctness against classical factorization.

## Scalability
- The algorithm is designed to work on semiprimes of increasing bit sizes.
- Due to simulation constraints, execution time increases significantly with larger numbers.
- Optimizations such as circuit depth reduction and efficient modular exponentiation can help scale to larger numbers.

## Insights & Learnings
- **Quantum Noise Consideration:** While simulators are noise-free, real quantum hardware introduces decoherence, impacting accuracy.
- **Resource Constraints:** Factoring larger numbers requires additional qubits and gate operations, which impact execution time.
- **Classical Post-Processing:** Some steps, such as computing the GCD, are still done classically, emphasizing hybrid approaches.

## Files in this Repository
- **`semiprimes.py`** - List of semiprime numbers provided for the challenge.
- **`Shor15.ipynb`** - Implementation of Shor's Algorithm for factoring 15 and scaling to larger numbers.
- **`README.md`** - This documentation explaining the approach and submission details.

---
*Prepared for iQuHACK 2025 - Quantum Factorization Challenge.* 🚀

