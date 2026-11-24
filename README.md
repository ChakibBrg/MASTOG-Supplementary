# MASTOG: Supplementary Material

MASTOG is a supervised feature-selection method for multimodal data. It encodes every
modality into a common latent space, applies stochastic gates to the resulting feature
nodes, models intra- and inter-modality interactions with attention, estimates synergies
between features, and returns the features whose gates are the highest.

This repository contains the information that did not fit in the paper's page limit:
the algorithm, the exact construction and preprocessing of the four datasets, and the
hyperparameters used in the experiments.

## Contents

| File | Description |
|---|---|
| `MASTOG_Supplementary_v2.pdf` | Compiled version |

## What the supplementary covers

1. **Algorithm**: pseudocode of MASTOG.
2. **Dataset construction and preprocessing**
   - **XOR (synthetic)**: a dataset with a planted synergistic pair, built so that each
     of the two features is individually uninformative about the label but the pair
     determines it exactly (500, 2000, 3000 and 5000 samples).
   - **PTB-XL+**: myocardial infarction vs. normal. 12-lead ECG waveforms combined with
     ECGDeli features (two modalities).
   - **WESAD**: stress vs. non-stress. Chest and wrist sensors (two modalities).
   - **PAMAP2**: walking vs. running. Three IMUs and heart rate (four modalities).
3. **Hyperparameters**: the settings used for each dataset, including the per-size
   settings for the XOR dataset.

For every real dataset the supplementary gives the label definition, the signal
processing (filtering, resampling, missing-value handling), the normalization, the
windowing, the final array shapes, and the train/test split.

## Datasets

The datasets are **not redistributed** here. They are publicly available from their
original sources; please refer to each page for its license and terms of use.

| Dataset | Source |
|---|---|
| PTB-XL v1.0.3 | <https://physionet.org/content/ptb-xl/1.0.3/> |
| PTB-XL+ v1.0.1 | <https://physionet.org/content/ptb-xl-plus/1.0.1/> |
| WESAD | <https://archive.ics.uci.edu/dataset/465/wesad> |
| PAMAP2 | <https://archive.ics.uci.edu/dataset/231/pamap2+physical+activity+monitoring> |

If you use these datasets, please cite the original publications:

- Wagner et al., *PTB-XL, a large publicly available electrocardiography dataset*,
  Scientific Data, 2020.
- Strodthoff et al., *PTB-XL+, a comprehensive electrocardiographic feature dataset*,
  Scientific Data, 2023.
- Schmidt et al., *Introducing WESAD, a multimodal dataset for wearable stress and
  affect detection*, ICMI, 2018.
- Reiss and Stricker, *Introducing a new benchmarked dataset for activity monitoring*,
  ISWC, 2012.

The XOR dataset is synthetic and fully described in the supplementary.
