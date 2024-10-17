# pyhf-tutorial

Here we have three notebooks that are independent of each other, which will teach you different things about statistical inference with [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#) and convenience packages such as [cabinetry](https://cabinetry.readthedocs.io/en/latest/index.html).

The different notebooks include the following:
* [**00-Intro-and-Simple-Model.ipynb**](./00-Intro-and-Simple-Model.ipynb): This introduces the basics of [HistFactory](https://cds.cern.ch/record/1456844/files/CERN-OPEN-2012-016.pdf) and [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#) from the ground up, how the workspaces and models can be built, as well as handling patchsets, and understanding how uncertainties work. This is a more pedagogical introduction than the next corresponding notebook.
* [**01-histogram-fits**](./01-histogram-fits.ipynb): This introduces the basics of [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#), how the model building works and how to include uncertainties. **We encourage you to start with this notebook.**
* [**02-hypothesis-testing**](./02-hypothesis-testing.ipynb): This notebook goes beyond the basics in [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#), and introduces advanced methods of statistical inference, such as hypothesis testing on a very simple model.
* [**03-bayesian-pyhf**](./03-bayesian-pyhf.ipynb): This builds the bridge to performing a Bayesian analysis, using a pyhf model. We will learn to understand how to translate the HistFactory likelihood to an expression that allows us to extract the posterior of our parameters. Further we will use advanced sampling methods to obtain a posterior of a simple model and compare the results to the ones obtained from a ferquentist fit. If you want to explore further, take a look at the [**03-bayesian-pyhf-eos**](./03-bayesian-pyhf-eos.ipynb) notebook. Here we use the phenomenology package [eos](https://eos.github.io/) to infer from the pyhf model, with the possibility of including the pyhf likelihood into a more global picture.

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


# Timing

Below is just a quick documentation of how fast it is to get things set up from scratch:

```
$ docker run -it --rm python:3 bash
root@50f672dec6b6:/# time git clone -b belle2-physics-week https://github.com/lorenzennio/pyhf-tutorial.git
Cloning into 'pyhf-tutorial'...
remote: Enumerating objects: 221, done.
remote: Counting objects: 100% (79/79), done.
remote: Compressing objects: 100% (52/52), done.
remote: Total 221 (delta 53), reused 52 (delta 27), pack-reused 142 (from 1)
Receiving objects: 100% (221/221), 23.08 MiB | 13.57 MiB/s, done.
Resolving deltas: 100% (125/125), done.

real	0m2.565s
user	0m0.707s
sys	0m0.755s

root@50f672dec6b6:/# time curl -fsSL https://pixi.sh/install.sh | bash
This script will automatically download and install Pixi (latest) for you.
Getting it from this url: https://github.com/prefix-dev/pixi/releases/latest/download/pixi-aarch64-unknown-linux-musl.tar.gz
######################################################################## 100.0%
The 'pixi' binary is installed into '/root/.pixi/bin'
Updating '/root/.bashrc'
Please restart or source your shell.

real	0m2.885s
user	0m0.376s
sys	0m0.454s

root@50f672dec6b6:/pyhf-tutorial# time pixi run nb
Pixi task (nb): jupyter notebook
[I 2024-10-16 07:47:28.838 ServerApp] jupyter_lsp | extension was successfully linked.
[I 2024-10-16 07:47:28.840 ServerApp] jupyter_server_terminals | extension was successfully linked.
[I 2024-10-16 07:47:28.842 ServerApp] jupyterlab | extension was successfully linked.
[I 2024-10-16 07:47:28.843 ServerApp] notebook | extension was successfully linked.
[I 2024-10-16 07:47:28.844 ServerApp] Writing Jupyter server cookie secret to /root/.local/share/jupyter/runtime/jupyter_cookie_secret
[I 2024-10-16 07:47:29.331 ServerApp] notebook_shim | extension was successfully linked.
[I 2024-10-16 07:47:29.347 ServerApp] notebook_shim | extension was successfully loaded.
[I 2024-10-16 07:47:29.348 ServerApp] jupyter_lsp | extension was successfully loaded.
[I 2024-10-16 07:47:29.348 ServerApp] jupyter_server_terminals | extension was successfully loaded.
[I 2024-10-16 07:47:29.349 LabApp] JupyterLab extension loaded from /pyhf-tutorial/.pixi/envs/default/lib/python3.12/site-packages/jupyterlab
[I 2024-10-16 07:47:29.349 LabApp] JupyterLab application directory is /pyhf-tutorial/.pixi/envs/default/share/jupyter/lab
[I 2024-10-16 07:47:29.349 LabApp] Extension Manager is 'pypi'.
[I 2024-10-16 07:47:29.355 ServerApp] jupyterlab | extension was successfully loaded.
[I 2024-10-16 07:47:29.357 ServerApp] notebook | extension was successfully loaded.
[C 2024-10-16 07:47:29.357 ServerApp] Running as root is not recommended. Use --allow-root to bypass.

real	0m44.216s
user	0m25.426s
sys	0m27.235s
```

total time: `49.666s`
