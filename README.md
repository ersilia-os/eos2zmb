# Inhibition of HDAC1

Prediction of the inhibition of the Human Histone Deacetylase 1 to revert HIV latency. The dataset is composed of all available pIC50 values from ChEMBL target 325 using two cut-offs, pIC50 7 (0.1uM) and 8 (10nM), and the model has been developed using Ersilias LazyQsar package (AUROCs of 0.89 and 0.91 over a 5-fold crossvalidation)

This model was incorporated on 2023-09-27.Last packaged on 2025-11-20.

## Information
### Identifiers
- **Ersilia Identifier:** `eos2zmb`
- **Slug:** `hdac1-inhibition`

### Domain
- **Task:** `Annotation`
- **Subtask:** `Activity prediction`
- **Biomedical Area:** `Cancer`, `AIDS`
- **Target Organism:** `Homo sapiens`
- **Tags:** `HIV`, `Human`, `HDAC1`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `2`
- **Output Consistency:** `Fixed`
- **Interpretation:** Probability of inhibition of HDAC1 at cut-offs pIC50 7 (0.1uM) and 8 (10nM)

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| hdac1_pic50_7 | float | high | Classification score of HDAC1 inhibition based on a pIC50 cutoff of 7 |
| hdac1_pic50_8 | float | high | Classification score of HDAC1 inhibition based on a pIC50 cutoff of 8 |


### Source and Deployment
- **Source:** `Local`
- **Source Type:** `Internal`
- **DockerHub**: [https://hub.docker.com/r/ersiliaos/eos2zmb](https://hub.docker.com/r/ersiliaos/eos2zmb)
- **Docker Architecture:** `AMD64`, `ARM64`
- **S3 Storage**: [https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos2zmb.zip](https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos2zmb.zip)

### Resource Consumption
- **Model Size (Mb):** `19`
- **Environment Size (Mb):** `7610`
- **Image Size (Mb):** `7527.14`

**Computational Performance (seconds):**
- 10 inputs: `65.74`
- 100 inputs: `58.41`
- 10000 inputs: `649.67`

### References
- **Source Code**: [https://github.com/ersilia-os/lazy-qsar](https://github.com/ersilia-os/lazy-qsar)
- **Publication**: [https://www.ebi.ac.uk/chembl/target_report_card/CHEMBL325/](https://www.ebi.ac.uk/chembl/target_report_card/CHEMBL325/)
- **Publication Type:** `Other`
- **Publication Year:** `2023`
- **Ersilia Contributor:** [GemmaTuron](https://github.com/GemmaTuron)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [GPL-3.0-or-later](LICENSE) license.

**Notice**: Ersilia grants access to models _as is_, directly from the original authors, please refer to the original code repository and/or publication if you use the model in your research.


## Use
To use this model locally, you need to have the [Ersilia CLI](https://github.com/ersilia-os/ersilia) installed.
The model can be **fetched** using the following command:
```bash
# fetch model from the Ersilia Model Hub
ersilia fetch eos2zmb
```
Then, you can **serve**, **run** and **close** the model as follows:
```bash
# serve the model
ersilia serve eos2zmb
# generate an example file
ersilia example -n 3 -f my_input.csv
# run the model
ersilia run -i my_input.csv -o my_output.csv
# close the model
ersilia close
```

## About Ersilia
The [Ersilia Open Source Initiative](https://ersilia.io) is a tech non-profit organization fueling sustainable research in the Global South.
Please [cite](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff) the Ersilia Model Hub if you've found this model to be useful. Always [let us know](https://github.com/ersilia-os/ersilia/issues) if you experience any issues while trying to run it.
If you want to contribute to our mission, consider [donating](https://www.ersilia.io/donate) to Ersilia!
