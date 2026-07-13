# Target-domain dataset

The target-domain cohort contains synthetic multimodal observations for users
11--20. It comprises ten dataset versions (`v1`--`v10`), with ten days per
version and user and 17,280 observations per day at five-second resolution.

Each version contains:

- individual user profiles;
- electronic medical records;
- smartwatch health measurements; and
- intelligent-insole measurements.

The large smartwatch and insole CSV files are stored with Git LFS. A clone
without automatic LFS download can retrieve them with:

```bash
git lfs pull
```
