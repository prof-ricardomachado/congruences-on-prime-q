# base-q-binomial-congruences
SageMath scripts and massive prime datasets (up to 21,000+ digits) corroborating OEIS A080469 through base-q digit-sum constraints.

# Digit-Sum Conditions in Prime-Base Binomial Congruences

This repository contains the supplementary computational material, source code, and full datasets for the paper:
**"Digit-Sum Conditions in Prime-Base Binomial Congruences and Connections with Generalized Wieferich Primes"** by Gabriel Guedes and Ricardo Machado.

## Overview
Our paper establishes a structural reduction for the binomial congruence $\binom{qn}{n} \equiv q^n \pmod n$ for integers of the form $n = q^t p$. We decouple the global congruence into a strictly modular condition and a base-$q$ digit-sum constraint: $s_q((q-1)p) \geq (q-1)t$. 

This repository provides the algorithms used to verify these conditions and the full decimal expansions of the exceptionally large prime factors discovered during our research, which provide heuristic justification for the OEIS conjecture [A080469](https://oeis.org/A080469).

## Repository Structure

* **/src**: Contains the SageMath scripts used for numerical generation and algorithmic verification.
  * `verify_digit_sum.ipynb`: Generates the values for the modular constant $A_t^{(q)}$ and Evaluates prime candidates against the $q$-adic digit-sum condition.
* **/data**: Contains plain text files (`.txt`) with the complete decimal expansions of the exceptionally large prime solutions that were truncated in the paper due to typographical constraints.
  * `solution_q11_t3.txt`
  * `solution_q11_t4.txt` (Contains the full 21,288-digit prime factor)

## Computational Methodology
All numerical generation and algorithmic verifications were executed using **SageMath version 9.5**. 

Due to the massive scale of the modular constants, prime factors provided in the /data directory were extracted using the [Alpertron Generic Integer Factorization suite](https://github.com/alpertron/calculators). With the sole exception of a 21,288-digit probable prime, all candidate factors have been formally certified using Elliptic Curve Primality Proving (ECPP) to ensure absolute mathematical rigor.

## Usage
To run the digit-sum verification on a specific prime from our dataset:
1. Ensure you have SageMath 9.5 (or compatible) installed.
2. Load the prime from the relevant `.txt` file in the `/data` folder.
3. Pass it through the `verify_digit_sum` function defined in the `/src` directory.

## Citation
If you use this code or dataset in your research, please cite our paper:
*(Citation details or arXiv link will be added here upon publication)*

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
