# Evaluating CrySL and CogniCrypt for Non-Cryptographic API Misuse Detection

This repository contains the materials and findings from my Bachelor's thesis titled **"Testing and Evaluation of CogniCrypt and CrySL in the Context of Non-Cryptography-related API Misuses"**, submitted in April 2021 at the University of Paderborn.

> 📄 **Published Work**: This thesis formed the basis for the peer-reviewed paper  
> [**"Extending CrySL for the Detection of API Misuses Beyond Cryptographic APIs"**](https://ieeexplore.ieee.org/document/9825763),  
> presented at the *2022 IEEE 29th International Conference on Software Analysis, Evolution and Reengineering (SANER)*.

## 📚 Abstract

While cryptographic APIs are notoriously difficult to use correctly, research has shown that non-cryptographic APIs are also prone to misuse. This thesis evaluates whether **CrySL** (a domain-specific language for specifying secure API usage) and the static analysis tool **CogniCrypt**, originally developed for cryptographic APIs, can be applied to detect **non-cryptographic API misuses**.

To support this, we developed a comprehensive **classification framework of API usage constraints**, based on an extensive literature review and 88 real-world API misuses. We then systematically assessed CrySL’s expressiveness and CogniCrypt’s detection capabilities for these misuses.

## 🔍 Research Questions

1. What is a precise and practical definition of API misuse?
2. What types of API usage constraints can be used to classify misuses?
3. Can CrySL and CogniCrypt handle non-crypto API misuse detection?
4. How effective is CogniCrypt in terms of precision and recall on non-crypto APIs?
5. How can CrySL be extended to improve its applicability to other domains?

## 🧪 Key Contributions

- **Definition and taxonomy** of API usage constraints tied to parts of method calls.
- **Evaluation of 88 non-crypto API misuses**, demonstrating limited applicability of CrySL without modifications.
- **Identification of gaps** in CrySL’s expressiveness for exception handling, null checks, and conditional method calls.
- **Proposals for extending CrySL**, enabling CogniCrypt to cover a broader range of misuses.

## ⚙️ Methodology

- Built a **classification framework** to localize constraints (e.g., on method calls, receivers, arguments).
- Mapped real-world misuse examples from known datasets.
- Systematically tested CrySL/CogniCrypt against categorized misuses.
- Analyzed precision, recall, and limitations.

## 🧩 Findings

- **CrySL lacks expressiveness** for many non-crypto APIs.
- **CogniCrypt cannot detect** many common misuses outside of its original domain.
- With minor **language extensions**, CrySL could support many typical non-crypto usage patterns.

## 📁 Repository Contents

- `specs/`: CrySL specifications created or adapted
- `examples/`: Sample Java code used for evaluation
- `docs/`: Thesis document and supporting materials

## 📄 Citation

If you use this work, please cite the IEEE paper:

> Steffen Sassalla, Eric Bodden.  
> *Extending CrySL for the Detection of API Misuses Beyond Cryptographic APIs.*  
> In: Proceedings of the 2022 IEEE 29th International Conference on Software Analysis, Evolution and Reengineering (SANER).  
> DOI: [10.1109/SANER53432.2022.00057](https://doi.org/10.1109/SANER53432.2022.00057)

## 📬 Contact

For questions or collaboration, feel free to reach out: [steffen.sassalla@outlook.de]

---

**Keywords**: API misuse detection, static analysis, CrySL, CogniCrypt, Java, software security, developer tools, SANER 2022