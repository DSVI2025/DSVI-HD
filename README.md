# DSVI-HD Dataset

This repository provides the synthetic target-domain dataset and the
accompanying mixed-noise definition associated with the study
**“Transfer Learning in Differential Stochastic Variational Inequalities with
History-Dependent Responses.”**

The dataset was generated using the same synthetic data-generation methodology
used for the [DSVI-O Dataset](https://github.com/DSVI2025/DSVI-O) and comprises
a distinct cohort of ten synthetic individuals (users 11–20). It includes
multimodal records from smartwatch sensors, intelligent insoles, electronic
medical records, and individual profiles. All records represent synthetic
individuals.

## Repository contents

- [`data/target/`](data/target/) contains the complete target-domain dataset.
- [`data/README.md`](data/README.md) describes the cohort, directory structure,
  temporal resolution, and record types.
- [`docs/mixed_noise_definition.pdf`](docs/mixed_noise_definition.pdf) gives the
  mathematical definition of the mixed sensor-noise construction.

Large smartwatch and insole CSV files are stored with Git LFS. After cloning,
the complete dataset can be retrieved with:

```bash
git lfs pull
```

## Citation

If you use this dataset or the accompanying mixed-noise definition, please cite
the dataset and the associated study using the metadata in
[`CITATION.cff`](CITATION.cff). The associated study is:

> “Transfer Learning in Differential Stochastic Variational Inequalities with
> History-Dependent Responses.”

## License

The dataset and accompanying documentation are licensed under the
[Creative Commons Attribution 4.0 International License](LICENSE).
