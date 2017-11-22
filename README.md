# SweepNet (WIP)

This is an early forlk of [chuckyee's](https://chuckyee.github.io/cardiac-segmentation/) dilated densenet implimentation for cardiac segmentation.

My intention if to ammend it for forced meaningfuly comparative attention on two images/slices. 

So much will change (eventually)...


## Installation

The main code is written as a Python package named `rvseg'. After cloning this
repository to your machine, install with:

```bash
cd cloned/path
pip install .
```

You should then be able to use the package in Python:

```python
import matplotlib.pyplot as plt
from rvseg import patient, models

p = patient.PatientData("RVSC-data/TrainingSet/patient01")
# Explore p.images, p.endocardium_masks, etc.
```

## Running models

Scripts for model training and evaluation are located under /scripts/.

```bash
python -u scripts/train.py defaults.config
```

Note: this package is written with the Tensorflow backend in mind -- (batch,
height, width, channels) ordered is assumed and is not portable to Theano.
