# Coinfection & Spatial Scaling 🦠 🗺️

*This repository is a live repository where there will be ongoing development of the neighbourhood analysis technique for detecting coinfection interactions. If you are looking for the archived work reported in our current pre-print, please see find that [here](https://github.com/shaunkeegan/coinfection_spatial_scaling_paper).*

# **Overview 📄** 

This code base takes data from trapping grids and calculates neighbourhood prevalence relative to each individual on the grid. It does this by itteratively identifying each individual in the population as the focal individual, and each other as a neighbour, with a distance to the focal individual calculated. Then prevalence is calculated for each user defined neighbourhood around the focal individual. This is then able to be used as a response variable in a statistical model as an explanatory factor for the infection state of the focal individual.

# Data Requirements 💿

The core function `parasite.function.vary.time.R` takes input data with the following format requirements:

-   X and Y coordinates

-   Temporal data in YYYY-MM-DD format

-   Presence/absence infection data

User selections required:

-   Minimum and maximum X and Y coordinates

-   Distance between trapping format

# **Functions 🕹️** 

`prop.on.grid` This function calculates the proportion of each neighbourhood that is within the defined trapping grid.

`exppoints` This function calculates the number of expected points on the grid for a given neighbourhood radius.

`make.dist.vector`

`parasite.function.vary.time` This function calculates the prevalence of a target parasite in each neighbourhood around each individual.

# **Required Packages 📦**

`gtools` for 'permutations' function to create list of all possible neighbourhood sizes
