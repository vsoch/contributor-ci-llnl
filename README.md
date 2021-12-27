# Contributor CI LLNL

![https://raw.githubusercontent.com/vsoch/contributor-ci/main/docs/assets/img/contributor-ci.png](https://raw.githubusercontent.com/vsoch/contributor-ci/main/docs/assets/img/contributor-ci.png)

This repository contains [Contributor CI](https://github.com/vsoch/contributor-ci) results for LLNL, meaning data extracted from
repos and members defined in  [contributor-ci.yaml](contributor-ci.yaml) that are generated and then pushed back to the repository.

> **Note** that automated extractions were paused on 12/26/2021 by @vsoch as it's wasteful to run jobs that are producing results nobody is looking at. If we want to continue, we can un-pause in the future. 

The extractions are done with a GitHub workflow, [.github/workflows/extract.yaml](.github/workflows/extract.yaml)
but you can run the same command locally as follows:

```bash
$ cci --out-dir _cci extract all
```

You will need a `GITHUB_TOKEN` or personal access token exported in the environment. For the
action itself, if you need to get information on users, a traditional `GITHUB_TOKEN` in the action
is not sufficient and you'll need to set a personal access token to `CCI_GITHUB_TOKEN`.
In addition to these data files, eventually there will be contributor friendliness assessments
and visualizations to go along with the data. Please [open an issue](https://github.com/vsoch/contributor-ci-llnl/issues)
if you have a question or point of discussion. 

## Usage

You can update the data with:

```bash
$ pip install contributor-ci
$ cci ui update
```

or generate your own site as follows:

```bash
$ pip install contributor-ci
$ mkdir -p my-cci
$ cd my-cci

# Any of the following work!
$ cci init user:vsoch
$ cci init org:spack
$ cci ui --cfa generate
```

To generate a new CFA:

```bash
$ cci -o cci cfa --terminal https://github.com/LLNL/b-mpi3 > _cfa/cfa-LLNL-b-mpi3.md
```
