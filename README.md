# template-anemoi-dataset

This repository serves as a template for creating Anemoi datasets. The motivation for creating separate repositories for different datasets, as opposed to a single repository containing all dataset recipes, is to maintain clear boundaries between different data sources and their respective processing logic, and to facilitate independent versioning and reproducibility.

# Table of contents
[Using this template](#using-this-template)

# Using this template

Each instantiation of this template targets a **single data source**. The repo is named:

```
<source>-anemoi-dataset
```

For example: `ich1-analysis-anemoi-dataset`, `synop-anemoi-dataset`, `mtg-anemoi-dataset`.

Within one repo, **variants** represent different configurations of the same source: different sets of variables, vertical coordinates, resolutions, time granularity, etc. 

## Granularity boundary: repo vs variant

The boundary rule is:

> **New repo** when the data comes from a different source system.
> **New variant** when the difference is a configuration choice within the same source system.

Use a new repo if *any* of these are true:

- Different data source
- Different data access system
- Different domain knowledge required to process the data

Use a new variant if *all* of these are true:

- Same data source
- Same data access system
- Same domain knowledge required to process the data
- Configs differ mainly in data queries (e.g. which variables, levels, or time ranges are selected) and processing

## Quickstart

* Instantiate this template directly from GitHub (button on the top right).
* Clone your repository, install the python environment with `uv sync`.
* Get started developing and follow the instructions below.

# Development guidelines

## Writing dataset recipes

## Writing plugins

# Versioning guidelines