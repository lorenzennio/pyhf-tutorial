# Fitting tutorial with `pyhf` and `cabinetry`

Here we have three notebooks that are independent of each other, which will teach you different things about statistical inference with [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#) and convenience packages such as [cabinetry](https://cabinetry.readthedocs.io/en/latest/index.html).

The different notebooks include the following:
* [**00-Intro-and-Simple-Model.ipynb**](./00-Intro-and-Simple-Model.ipynb): This introduces the basics of [HistFactory](https://cds.cern.ch/record/1456844/files/CERN-OPEN-2012-016.pdf) and [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#) from the ground up, how the workspaces and models can be built, as well as handling patchsets, and understanding how uncertainties work. This is a more pedagogical introduction than the next corresponding notebook.
* [**01-histogram-fits**](./01-histogram-fits.ipynb): This introduces the basics of [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#), how the model building works and how to include uncertainties. **We encourage you to start with this notebook.**
* [**02-hypothesis-testing-CLs**](./02-frequentist_CLs_limit_with_pyhf.ipynb): This notebook goes beyond the basics in [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#), and introduces advanced methods of statistical inference, such as hypothesis testing on a very simple model. 
* [**03-bayesian-pyhf**](./03-bayesian-pyhf.ipynb): This builds the bridge to performing a Bayesian analysis, using a pyhf model. We will learn to understand how to translate the HistFactory likelihood to an expression that allows us to extract the posterior of our parameters. Further we will use advanced sampling methods to obtain a posterior of a simple model and compare the results to the ones obtained from a ferquentist fit. If you want to explore further, take a look at the [**03-bayesian-pyhf-eos**](./03-bayesian-pyhf-eos.ipynb) notebook. Here we use the phenomenology package [eos](https://eos.github.io/) to infer from the pyhf model, with the possibility of including the pyhf likelihood into a more global picture.
* [**03-hypothesis-testing**](./03-hypothesis-testing.ipynb): This notebook goes beyond the basics in [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#), and introduces advanced methods of statistical inference, such as hypothesis testing on a very simple model.

## Getting started

First, download this repository and branch:

```
git clone -b belle2-physics-week https://github.com/lorenzennio/pyhf-tutorial.git
```

then proceed to installing your dependencies with `pip` manually or using `pixi` (see below).

### pip

```
python3 -m venv venv
source venv/bin/activate
python3 -m pip install -U pip
python3 -m pip install -r requirements.txt
```

### pixi

If you do not have [pixi](https://pixi.sh/latest/) installed, it would be easy to get it working like so:

```
curl -fsSL https://pixi.sh/install.sh | bash
exec bash
```

then simply running `pixi run nb` or `pixi run nb <a notebook file>` will get you up and running in less than a minute!

## References

### pyhf
* [Documentation](https://pyhf.readthedocs.io/en/v0.7.2/#)
* [Overview slides](https://indico.belle2.org/event/12273/contributions/79573/)
* [`pyhf` tutorial](https://pyhf.github.io/pyhf-tutorial/introduction.html)

### HistFactory and asymptotic formulae
* [HistFactory paper](https://cds.cern.ch/record/1456844/files/CERN-OPEN-2012-016.pdf)
* [Asymptotic formulae for likelihood-based tests of new physics](https://arxiv.org/pdf/1007.1727.pdf)

### Cabinetry
* [Documentation](https://cabinetry.readthedocs.io/en/latest/index.html)
* [`Cabinetry` tutorial](https://github.com/cabinetry/cabinetry-tutorials/blob/master/example.ipynb)
* [Tutorial from Belle II `pyhf` workshop](https://github.com/alexander-held/Belle-II-cabinetry/blob/main/talk.ipynb)

