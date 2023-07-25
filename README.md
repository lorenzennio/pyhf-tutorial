# pyhf-tutorial

Here we have three notebooks that are independent of each other, which will teach you different things about statistical inference with [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#) and convenience packages such as [cabinetry](https://cabinetry.readthedocs.io/en/latest/index.html).

The different notebooks include the following:
* [**01-histogram-fits**](01-histogram-fits.ipynb): This introduces the basics of [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#), how the model building works and how to include uncertainties. **We encourage you to start with this notebook.**
* [**02-B2Kpi**](02-B2Kpi.ipynb): This notebook is a realistic example of how to build a statistical model for the $B^+ \to K^+ \pi^0$ decay. We use reconstructed MC in combination with [cabinetry](https://cabinetry.readthedocs.io/en/latest/index.html) to build our [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#) model. Additionally, tracking efficiency and PID systematics are included in the model. The [**02-pid-weights**](02-pid-weights.ipynb) notebook can be studied as an extension, but is not required (access to KEKCC is necessary to access the ntuples to run this notebook).
* [**03-hypothesis-testing**](03-hypothesis-testing.ipynb): This notebook goes beyond the basics in [pyhf](https://pyhf.readthedocs.io/en/v0.7.2/#), and introduces advanced methods of statistical inference, such as hypothesis testing on a very simple model.

