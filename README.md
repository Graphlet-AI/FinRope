# FinRope: Financial Risk Patterns

FinRope is a risk pattern repository for a standard format for business and financial networks. It useds the Open Sanctions property graph format to provide a common schema around which financial institutions and vendors can collaborate to perform KYC, AML and CTF operations.

## Introduction

For an introduction to the project, please see the post [Financial Crime and Corruption Network Motifs](https://blog.graphlet.ai/financial-crime-and-corruption-network-motifs-4cf2e8e10eb5).

## Schema

This project defines risk patterns called network motifs over a property graph model based on a data model for financial crime and corruption investigations called [FollowTheMoney](https://followthemoney.tech/explorer).

> FollowTheMoney (FtM) is a data model for anti-corruption investigations. It contains definitions of the entities relevant in such research (like people or companies) and tools that let you generate, validate, and export such data easily. Entities can reference each other, thus creating a graph of relationships.

FollowTheMoney is a statement graph. Property graphs are a more familiar form for most organizations, so we have mapped the FtM schema to a property graph model. The schema is defined in the [schema/](schema/) folder.

## Risk Motifs

The risk motifs are defined in the [motifs/](motifs/) folder. Each motif is a YAML file that describes the structure and properties of the motif.

## Python SDK

The Python SDK for the FinRope project is in [python/](python/). It provides a set of tools and utilities to work with the FinRope schema and perform various operations related to financial risk patterns.

For more information, check the [python/README.md](python/README.md).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
