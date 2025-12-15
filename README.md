# Efflux pump avoidance in gram-negative bacteria

Using Co-ADD data on E.coli inhibition (WT, TolC efflux deficient and lpxC hyperpermable strains) 73k compounds were classified as inactive, efflux evaders and efflux substrates, based on the relative inhibition of wild-type vs permeable strains. We have used the efflux evaders (186) and efflux substrates (554) data to train a model that predicts the probability of a molecule being an efflux evader.



## Information
### Identifiers
- **Ersilia Identifier:** `eos3lyd`
- **Slug:** `efflux-pump-avoidance-gram-negative`

### Domain
- **Task:** `Annotation`
- **Subtask:** `Activity prediction`
- **Biomedical Area:** `Antimicrobial resistance`
- **Target Organism:** `Escherichia coli`, `Gram-negative bacteria`
- **Tags:** `Antimicrobial activity`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `1`
- **Output Consistency:** `Fixed`
- **Interpretation:** Probability of being an efflux evader

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| efflux_evader_proba | float | high | Probability of the molecule being an efflux evader in E.coli |


### Source and Deployment
- **Source:** `Local`
- **Source Type:** `Internal`

### Resource Consumption


### References
- **Source Code**: [https://github.com/domgurvic/efflux_evaders_and_substrates](https://github.com/domgurvic/efflux_evaders_and_substrates)
- **Publication**: [https://www.nature.com/articles/s44259-024-00023-w](https://www.nature.com/articles/s44259-024-00023-w)
- **Publication Type:** `Peer reviewed`
- **Publication Year:** `2025`
- **Ersilia Contributor:** [miquelduranfrigola](https://github.com/miquelduranfrigola)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [GPL-3.0-or-later](LICENSE) license.

**Notice**: Ersilia grants access to models _as is_, directly from the original authors, please refer to the original code repository and/or publication if you use the model in your research.


## Use
To use this model locally, you need to have the [Ersilia CLI](https://github.com/ersilia-os/ersilia) installed.
The model can be **fetched** using the following command:
```bash
# fetch model from the Ersilia Model Hub
ersilia fetch eos3lyd
```
Then, you can **serve**, **run** and **close** the model as follows:
```bash
# serve the model
ersilia serve eos3lyd
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
