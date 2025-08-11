# fhe-ckks-lwe-lab-encrypted-ml



**Privacy-preserving logistic regression using fully homomorphic encryption (CKKS, Ring-LWE)**

## Overview

This repository contains the lab project for the “Machine Learning on Encrypted Data” course at Uni Bonn. The focus is on implementing and analyzing a fully-homomorphic encrypted logistic regression pipeline using the CKKS scheme [[Cheon et al., ASIACRYPT 2017]](https://eprint.iacr.org/2016/421](https://eprint.iacr.org/2016/421)), a fully-homomorphic encryption (FHE) scheme on approximate numbers, with its security based on the hardness assumption of Ring Learning With Errors (Ring-LWE) problem.&#x20;

The bootstrapping technique was initially suggested in this paper [[Gentry, STOC 2009]](https://dl.acm.org/doi/10.1145/1536414.1536440) which suggest the construction of FHE (which allows homomorphic addition and multiplication). With the rescaling of CKKS scheme, CKKS scheme has a manageable error size. With the paper Bootstrapping for Approximate Homomorphic Encryption [[Cheon et al., EUROCRYPT 2018]](https://eprint.iacr.org/2017/652), CKKS schemes extends to a FHE.

## References

- **Cheon et al., ASIACRYPT 2017**: Cheon, Jung Hee; Kim, Andrey; Kim, Miran; Song, Yongsoo. "Homomorphic Encryption for Arithmetic of Approximate Numbers." Springer, Lecture Notes in Computer Science, vol. 10624, 2017. (https://eprint.iacr.org/2016/421)
- **Gentry, STOC 2009**: Gentry, Craig. "Fully Homomorphic Encryption Using Ideal Lattices." Proceedings of the 41st Annual ACM Symposium on Theory of Computing (STOC), 2009. (https://dl.acm.org/doi/10.1145/1536414.1536440)
- **Cheon et al., EUROCRYPT 2018**: Cheon, Jung Hee; Kim, Andrey; Kim, Miran; Song, Yongsoo. "Bootstrapping for Approximate Homomorphic Encryption." Proceedings of the 37th Annual International Conference on the Theory and Applications of Cryptographic Techniques (EUROCRYPT), 2018. (https://eprint.iacr.org/2018/153)

## Knowledge Demonstrated

- **Lattice-based Cryptography:** Hands-on implementation of LWE and Ring-LWE concepts.
- **Learning With Errors (LWE):** hardness assumption for post-quantum cryptography
- **Ring-LWE:** Efficient polynomial-ring variant of LWE, reducing key sizes and improving performance.
- **Module-LWE:** A generalization of LWE and Ring-LWE, offering a flexible trade-off between efficiency and security.
- **CKKS (approximate FHE):** Enables arithmetic of approximate numbers on encrypted data, ideal for ML tasks.
- **Fully-Homomorphic Encryption:** Practical CKKS integration for logistic regression. Choices of parameters which requires understanding of ring-LWE and CKKS scheme.
- **Performance Benchmarking:** Recorded and analyzed accuracy and per-epoch runtimes and compared with the metrics from logistic regression with plaintexts.
- **Documentation & Reproducibility of Code:** Clear reporting and presentation, code structure, inline explanations, and sample datasets.

## Core Contributions

- LWE, Ring-LWE, CKKS: Learned and documented LWE, Ring-LWE, and CKKS.
- CKKS (Ring-LWE) Parameter Selection: Studied security parameters (polynomial modulus degree, coeff modulus, scale) matching educational benchmarks.
- **CKKS Encryption Pipeline:** Encoded data, encrypted feature vectors, and executed encrypted gradient & weight updates.
- **Jupyter Notebook with Results:** A self-contained Jupyter notebook (`notebooks/ckks_lwe_logreg.ipynb`) that showcases the progress and results.

## Repository Structure

```
fhe-ckks-lwe-lab-encrypted-ml/
├── jupyter_notebooks/                # Jupyter notebook with end-to-end pipeline, results
│   └── ckks_encrypted_logistic_regression.ipynb
├── datasets/                     # datasets
│   ├── framingham.csv
│   ├── LogReg_sample_dataset.csv
│   ├── HRF_sample_small.csv
│   └── HRF_samples_big.csv
├── report_latex/                  #latex files for the report
│   ├── main.tex
│   ├── ......
└── slides_and_report/                  # PDF report & presentation slides
    ├── Crypto_Lab_Report.pdf
    └── Crypto_Lab_Presentation.pdf

```

## Quick Usage

1. Clone the repo.
2. Run `notebooks/ckks_lwe_logreg.ipynb` in Jupyter Lab/Notebook to see parameter choices, encryption, training, and results.

## Highlights

- Review of LWE, Ring-LWE, which are also related to post-quantum cryptography.
- Review of fully-homomorphic encryption (CKKS) with explanation.
- End-to-end encrypted ML workflow.
- Detailed performance metrics for academic evaluation.

## Next Steps

- **Parallelization:** Optimize batching and multi-thread execution.
- **Vectorization:** Implement CKKS batching and vector packing to process multiple data points in parallel, aligning with techniques discussed in the lab report.

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE) for details.

