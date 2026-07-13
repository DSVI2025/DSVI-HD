# DSVI-HD

This repository provides the target-domain dataset and supplementary mixed-noise
definition associated with the study **“Transfer Learning in Differential
Stochastic Variational Inequalities with History-Dependent Responses.”**

The target domain represents ten synthetic elderly-health trajectories with
multimodal observations from smartwatch sensors, intelligent insoles,
electronic medical records, and individual profiles. The dataset is organized
into ten versions and supports the study of history-dependent responses under
distributional variation and heterogeneous sensor perturbations.

## Repository contents

- [`data/target/`](data/target/) contains the complete target-domain cohort.
- [`data/README.md`](data/README.md) describes the dataset organization and
  integrity metadata.
- [`docs/mixed_noise_definition.pdf`](docs/mixed_noise_definition.pdf) gives the
  mathematical definition of the mixed sensor-noise construction.

Large smartwatch and insole CSV files are stored with Git LFS. After cloning,
the complete dataset can be retrieved with:

```bash
git lfs pull
```

This repository contains data and mathematical documentation only. It does not
include experimental implementations or data-generation scripts.
