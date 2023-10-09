# pyhf-tutorial

Here we have two notebooks that are independent of each other, which will teach you different things about statistical inference with [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#).

The different notebooks include the following:
* [**01-histogram-fits**](./01-histogram-fits.ipynb): This introduces the basics of [pyhf](https://pyhf.readthedocs.io), how the model building works and how to include uncertainties. **We encourage you to start with this notebook.**
* [**02-hypothesis-testing**](./02-hypothesis-testing.ipynb): This notebook goes beyond the basics in [pyhf](https://pyhf.readthedocs.io), and introduces advanced methods of statistical inference, such as hypothesis testing on a very simple model.

## Installation
To install the required packages run
`pip install --user pyhf numpy scipy matplotlib iminuit ipywidgets`

## References
### pyhf
* [Documentation](https://pyhf.readthedocs.io)
* [Overview slides](https://indico.belle2.org/event/8470/contributions/55827/attachments/21257/31463/pyhf.pdf)
* [`pyhf` tutorial](https://pyhf.github.io/pyhf-tutorial/introduction.html)
### HistFactory and asymptotic formulae
* [HistFactory paper](https://cds.cern.ch/record/1456844/files/CERN-OPEN-2012-016.pdf)
* [Asymptotic formulae for likelihood-based tests of new physics](https://arxiv.org/pdf/1007.1727.pdf)

### Cabinetry
* [Documentation](https://cabinetry.readthedocs.io/en/latest/index.html)
* [`Cabinetry` tutorial](https://github.com/cabinetry/cabinetry-tutorials/blob/master/example.ipynb)
* [Tutorial from Belle II `pyhf` workshop](https://github.com/alexander-held/Belle-II-cabinetry/blob/main/talk.ipynb)