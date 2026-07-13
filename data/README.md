# DSVI-HD Dataset

The DSVI-HD dataset contains synthetic multimodal health records for ten
distinct users, identified as 11–20. The data were generated using the same
synthetic data-generation methodology used for the
[DSVI-O Dataset](https://github.com/DSVI2025/DSVI-O), whose users are identified
as 1–10; the two datasets therefore represent distinct user cohorts.

The dataset is organized into ten versions (`v1`–`v10`), each representing a
separate ten-day realization for every user. The wearable and insole time
series are sampled at five-second intervals, yielding 17,280 time points per
day. The version directories do not form a continuous 100-day calendar-time
series; across the ten realizations, each user is represented by 100 day-level
trajectories.

The dataset is fully synthetic. All records represent synthetic individuals
and are intended for methodological research on history-dependent dynamic
systems and transfer learning.

## Directory structure

Each version follows the same layout:

```text
data/target/vN/
|-- user_profiles.csv
|-- medical_records.csv
|-- electronic_medical_records/
|   `-- <user_id>_EMR.csv
|-- health_data/
|   `-- <user_id>_health_data.csv
`-- insole_data/
    `-- <user_id>_insole_data.csv
```

## Record types

- `user_profiles.csv` contains one profile for each user, including the user
  identifier, age, gender, height, weight, and BMI.
- `medical_records.csv` contains cohort-level demographic, laboratory, and
  clinical measurements; `electronic_medical_records/` contains the
  corresponding record for each individual user. Each record contains a user
  identifier and 30 demographic and clinical fields.
- `health_data/` contains five-second wearable health measurements together
  with activity and health-state fields. After the timestamp, each file
  contains 14 wearable and activity variables and the two annotation fields
  `status` and `abnormal_group`.
- `insole_data/` contains five-second plantar-pressure, gait, balance, motion,
  and exercise-related measurements. After the timestamp, each file contains
  17 insole measurement and descriptor fields.

All tabular files are UTF-8 CSV files with a header row. Time-series timestamps
use the format `YYYY-MM-DD HH:MM:SS`. Measurement units are included in the
electronic-medical-record column names where applicable; the remaining variable
names are given directly in the CSV headers.

## Git LFS

The large wearable health and insole CSV files are stored with Git LFS. A clone
without automatic LFS download can retrieve them with:

```bash
git lfs pull
```
