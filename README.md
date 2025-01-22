# MoviePlotsGenre
#Overview

This repository contains the implementation of Project 2 for the Practical Machine Learning class. The project involves clustering movie plot data using two unsupervised learning methods: OPTICS and BIRCH. The goal is to explore patterns and group movies based on plot similarities, analyze the results, and compare them to known genres.

#Dataset

The dataset used in this project is the Wikipedia Movie Plots dataset. This dataset contains information about movies such as:

Release Year

Title

Origin/Ethnicity

Director

Cast

Genre (used as labels for interpretability)

Plot (used for clustering)


#Objectives

Cluster movies based on plot similarities using:

OPTICS

BIRCH

Use two different feature representations:

Text-based feature representation derived from the Plot column.

Numeric/tabular feature representation derived from Release Year, Origin/Ethnicity, Director, etc.

Compare the clustering results with:

Random chance baselines.

A supervised baseline model.

Interpret the results to understand cluster characteristics and align them with movie genres.
