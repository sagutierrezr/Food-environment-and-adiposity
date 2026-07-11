# Food-environment-and-adiposity

Statistical analysis code for the study "Residential food-related built environment and anthropometric outcomes in five Colombian cities: evidence from the COPEN survey", based on data from the 2022 COPEN (Colombian Study of Nutritional Profiles) survey.

Overview

This repository contains the R code used to evaluate the association between residential food-related built environment (BE) attributes — supermarket/greengrocer density and fast-food restaurant/bakery density — and two anthropometric outcomes, body mass index (BMI) and waist circumference (WC), across Bogotá, Medellín, Cali, Barranquilla, and Bucaramanga.

The analysis uses multilevel linear models to account for the hierarchical structure of the data (individuals nested within shared residential microenvironments, nested within cities), incorporating survey sampling weights.

Data source

Data come from the COPEN survey (2022), a cross-sectional, multistage probabilistic survey representative of adults residing in five major Colombian cities. Due to data protection agreements, the original COPEN microdata are not included in this repository. Access requests should be directed to the COPEN study team.

Software and packages

R (version to be specified)
WeMix — weighted multilevel model estimation incorporating survey expansion factors
dplyr, tidyr, ggplot2, tibble — data handling and visualization
Geospatial processing conducted in QGIS (version 3.34.11); built environment attributes extracted from OpenStreetMap via the ohsome API

Methods summary

Residential addresses were geocoded and used as centroids for circular microenvironments (1,500 m radius). Overlapping microenvironments (>70% shared area) were aggregated to account for shared exposure. Multilevel linear models were fitted separately for each outcome, with random intercepts for microenvironment and city, and random slopes by city for each BE attribute. Full methodological details are available in the associated manuscript.
