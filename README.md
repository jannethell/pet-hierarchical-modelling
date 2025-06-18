# pet-hierarchical-modelling
R Markdown scripts for Bayesian modelling of PET data using SiMBA

# Hierarchical Modelling of PET Data – SiMBA Analysis with [11C]PBR28

This repository contains R Markdown scripts used in a master's thesis project focused on the hierarchical modelling of positron emission tomography (PET) data to quantify neuroinflammation using the radioligand [¹¹C]PBR28. The modelling approach is based on Bayesian hierarchical modelling using the SiMBA framework.

---

## 📂 Repository structure

### `.Rmd`  
Preprocessing and BIDS conversion of Dataset 1 using `dcm2niix`, `PET2BIDS`, and other supporting scripts. Outputs are structured to comply with the PET-BIDS standard.

### `.Rmd`  
Same as above, but for Dataset 2. Minor changes exist between the two due to structural or file-specific inconsistencies in the original datasets.

### `Modelling.Rmd`  
Main modelling script for running full SiMBA analysis using `brms`, including:
- Stan model definition (2TCM and variants)
- Prior specification
- Model fitting
- Post-processing steps (summaries, diagnostics, etc.)

---

## 🔐 Data Access Notice

The code in this repository references PET data and arterial input functions that are **stored locally and not included** due to patient confidentiality and research data agreements.  
**This means you will not be able to execute the code without providing your own data in a compatible structure.**

However, the code logic is fully preserved and can be adapted to:
- Simulated data
- Public PET datasets from [OpenNeuro](https://openneuro.org/) or other BIDS-compliant sources

---

## 🛠 Requirements

- R (≥ 4.0)
- Key packages: `brms`, `rstan`, `tidyverse`, `kinfitr`, `pet2bids`, `simba`

All required libraries are listed at the beginning of each `.Rmd` file.

---

## ⚠️ Notes

- Some typos and Swedish/English mix may occur in comments or code chunks.
- This code is primarily shared for **transparency** and **reproducibility**, and to support future adaptation using similar PET datasets.
- No model outputs or fitted objects are included.

---

## 📄 License

This code is shared under the **MIT License** – see [LICENSE](LICENSE) for details.
