TUC
===

## TUC
> **T**yped **U**se-**C**ase

![tuc-logo](https://github.com/TypedUseCase/TypedUseCase.github.io/raw/master/assets/tuc-logo.png)

It is basically a use case definition, for which this console application can generate [PlantUML](https://plantuml.com/) diagram, where all services are domain specific type safe.

## Motivation
We have a DDD based micro service architecture, where most of the services have an asynchronous communication between them (mostly through event streams) with a domain specific ubiquitous language.

And we need to document the use-cases done by those services.

For now, we use a [PlantUML](https://plantuml.com/) directly, but it is **a lot** of work, so we decided to create a *language* to help us with that - **TUC**.

## Table of Contents
- [Domain](/domain/)
    - [How does it work?](/domain/#how-does-it-work)
    - [Common Types](/domain/#common-types)
    - [Domain example](/domain/#domain-example)
    - [Share types between domains](/domain/#share-types-between-domains)
- [TUC](/tuc/)
    - [Syntax](/tuc/#syntax)
    - [Structure](/tuc/#structure)
    - [Example](/tuc/example.html)
