# Inhibition of HDAC1

Prediction of the inhibition of the Human Histone Deacetylase 1 to revert HIV latency. The dataset is composed of all available pIC50 values from ChEMBL target 325, and the model has been developed using Ersilia's LazyQsar package (MorganBinaryClassifier)

## Identifiers

* EOS model ID: `eos2zmb`
* Slug: `hdac1-inh`

## Characteristics

* Input: `Compound`
* Input Shape: `Single`
* Task: `Classification`
* Output: `Probability`
* Output Type: `Float`
* Output Shape: `List`
* Interpretation: Probability of inhibition of HDAC1 at cut-offs pIC50 7 (0.1uM) and 8 (10nM)

## References

* [Publication](https://www.ebi.ac.uk/chembl/target_report_card/CHEMBL325/)
* [Source Code](https://github.com/ersilia-os/lazy-qsar)
* Ersilia contributor: [GemmaTuron](https://github.com/GemmaTuron)

## Ersilia model URLs
* [GitHub](https://github.com/ersilia-os/eos2zmb)
* [AWS S3](https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos2zmb.zip)
* [DockerHub](https://hub.docker.com/r/ersiliaos/eos2zmb) (AMD64)

## Citation

If you use this model, please cite the [original authors](https://www.ebi.ac.uk/chembl/target_report_card/CHEMBL325/) of the model and the [Ersilia Model Hub](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff).

## License

This package is licensed under a GPL-3.0 license. The model contained within this package is licensed under a GPL-3.0 license.

Notice: Ersilia grants access to these models 'as is' provided by the original authors, please refer to the original code repository and/or publication if you use the model in your research.

## About Us

The [Ersilia Open Source Initiative](https://ersilia.io) is a Non Profit Organization ([1192266](https://register-of-charities.charitycommission.gov.uk/charity-search/-/charity-details/5170657/full-print)) with the mission is to equip labs, universities and clinics in LMIC with AI/ML tools for infectious disease research.

[Help us](https://www.ersilia.io/donate) achieve our mission!