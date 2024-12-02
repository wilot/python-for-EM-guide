# Introduction

This guide serves as an introduction to using Python for Electron Microscopy image-analysis. It aims to introduce
features of the language and ecosystem to those unfamiliar with programming, the Python language or the scientific
Python ecosystem.

This guide does not aim to teach the Python programming language. Instead it will make reference to several places
where learning resources can be found. It aims to cover everything else necessary to get started working on EM-specific
tasks. Python is employed in many different fields and a general introduction to programming one might find online
would not set the reader up with the tools necessary for using Python for EM.

For those without any experience in programming, it is recommended to read this guide before learning Python.

For those with programming experience in other languages, read this guide and find a quick guide online for the Python
language.

For those with Python experience this guide can be abridged to can be abridged to:

- Use `Anaconda` (or `miniconda`) not pip
- Use `hyperspy` to read EM files
- Use `hyperspy` and the rest of the general scientific python ecosystem (`numpy`, `skimage`, `matplotlib`) to process
EM data
- Use `ase` and `abTEM` to model atoms and perform multislice simulations respectively

## Contents

A brief overview of the Python language is covered in [Python Language](./language.md). This focuses on
the details necesary for programming rather than teaching the Python language. It incldes a description of 
packages/libraries, environments and package-managers.

Finally a brief overview of the scientific Python ecosystem is explored, setting out the lay-of-the-land. It lists
the major Python libraries needed for almost every project and describes what can be found where.
