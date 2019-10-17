---
layout: default
title: FAQ
---


### How do we join the tables `vegetationStructure.csv` and `SpeciesID.csv` files?

They can be joined using `tagID` and `crownID` columns as a refernce key.


### The DBH column in `SpeciesIDs.csv` for tagged trees is extremely high?

In the species ID file the tree_ID and DBH columns have the same data copied onto one another.


### What are the most important data sources in the given data set for classification?

The following data sources are useful and listed in order of importance:

* Hyperspectral image data

* LiDAR data & ITC shapefiles

* Ground based Vegetation structure data


### How do we handle and use the hyperspectral data?

Detailed explanation of using such data can be found on www.neonskills.org


### What should I do with the ITC data?

ITC data contains crown boundaires of individual trees which gives data about the crown shape, diameter which combined with hyperspectral signature makes it straightforward to identify what species an individual belongs to.


### What is one identifier that acts as a common point across all data sources?

`crown_ID` is one common identifer for an individual tree, its crown polygon pixels. Therefore it is the common point.
