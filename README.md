# ATLAS TopWTagger GBM
This package is intended to show-case what modern ML tols can do compared to the tools used in the HEP community. 
As a use case, the ATLAS tagging on _t_ and _W_ was attempted. The current implementation includes _top_-tagging only, but it is easily extendable to _W_. 

The final performance curves show that one can achieve the same performance as the nominal GBM tagger trained using TMVA. However, the big gain ocmes in training time. **LightGBM model with optimised parameters is trained typically within ~1 min, whereas the TMVA training time is of the order of 1 hour**: ![GBM training time from ATL-PHYS-PUB-2017-004](https://atlas.web.cern.ch/Atlas/GROUPS/PHYSICS/PUBNOTES/ATL-PHYS-PUB-2017-004/fig_02b.png)

The notebook also provides additional features:
- Selection of the most sensitive variables based on LightGBM feature importance evaluation.
- Hyper-parameter optimisation with cross-validation
- Early stopping in hyper-parameter tune to avoid overtraining.

To get going, you will need a machine with conda/anaconda installation. 
Let's create a conda environment and install required packages (instructions are for Linux/MacOS, on a Windows machine you will not need `source`):
```
# atlas_JSS_tagging_2018 is a custom name, you are free to choose whatever you fancy
conda create -n atlas_JSS_tagging_2018 python=3.6
source activate atlas_JSS_tagging_2018
conda install --yes pytables numpy pandas jupyter ipykernel seaborn matplotlib scikit-learn lightgbm
```
Now you have all relevant packages installed and are almost ready to go.
You can contact Misha Lisovyi or Ece Akilli to get inputs in `HDFS` format.
