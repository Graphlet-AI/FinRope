# FinRope: Financial Risk Patterns

FinRope is a risk pattern repository for a standard format for business and financial networks. It useds the Open Sanctions property graph format to provide a common schema around which financial institutions and vendors can collaborate to perform KYC, AML and CTF operations.

## Introduction

For an introduction to the project, please see the post [Financial Crime and Corruption Network Motifs](https://blog.graphlet.ai/financial-crime-and-corruption-network-motifs-4cf2e8e10eb5).

## Schema

This project defines risk patterns called network motifs over a property graph model based on a data model for financial crime and corruption investigations called [FollowTheMoney](https://followthemoney.tech/explorer).

> FollowTheMoney (FtM) is a data model for anti-corruption investigations. It contains definitions of the entities relevant in such research (like people or companies) and tools that let you generate, validate, and export such data easily. Entities can reference each other, thus creating a graph of relationships.

FollowTheMoney is a statement graph. Property graphs are a more familiar form for most organizations, so we have mapped the FtM schema to a property graph model. The schema is defined in the [schema/](schema/) directory.

## Pre-Requisites

This project code can be executed with Docker or local Python/

- Docker - you can [install docker](https://docs.docker.com/engine/install/) and then check the [Get Started](https://www.docker.com/get-started/) page if you aren't familiar.

OR

- Python 3 - you can download Anaconda Python here: [https://www.anaconda.com/download](https://www.anaconda.com/download)

Supported operating systems:

- Mac OS X
- Ubuntu Linux
- Windows

## Development Environment Setup

The code for working with the schema is in the [python/](python/) directory.

If you're building software and want to experiment and explore this code and its dependencies, you can load the code in Visual Studio Code or another editor.

### Python Virtual Environment

We use a Python virtual environment to run the code in this repository in a local environment. This will help you avoid conflicts with other Python projects you may have on your system.

#### Anaconda Python

If you are using Anaconda Python, create a new conda environment named `finrope` using the following command:

```bash
conda create -n finrope python=3.11 -y
```

Then activate the environment:

```bash
conda activate finrope
```

To deactivate the environment:

```bash
conda deactivate
```

#### Other Python

You can use a Python venv environment to run the code in this repository. To create a new virtual environment named `finrope`, use the following command:

```bash
python3 -m venv finrope
```

Then activate the environment:

```bash
source finrope/bin/activate
```

### Python Dependency Management

The project uses [Python Poetry](https://python-poetry.org/) for package management.

#### Install Poetry

To install Poetry (see [install docs](https://python-poetry.org/docs/)), you can use [pipx](https://github.com/pypa/pipx) or `curl` a script.

#### Install Poetry Using `curl`

To install using `curl`, just run:

```bash
curl -sSL https://install.python-poetry.org | python3 -
```

#### Install Poetry using `pipx`

To first install `pipx`, on Mac OS X run:

```bash
brew install pipx
pipx ensurepath
sudo pipx ensurepath --global # optional to allow pipx actions with --global argument
```

On Ubuntu Linux, run:

```bash
sudo apt update
sudo apt install pipx
pipx ensurepath
sudo pipx ensurepath --global # optional to allow pipx actions with --global argument
```

Then install Poetry using `pipx`:

```bash
pipx install poetry
```

It will now be outside your virtual environment and available to all your Python projects.

#### Install Dependencies

Now we can use `poetry` to install our Python dependencies. Run the following command:

```bash
poetry install
```
