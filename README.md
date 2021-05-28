# police-misconduct-complaints-analysis

By [Christine Zhang](mailto:christine.zhang@ft.com)

This analysis of police misconduct complaints data was conducted for the May 28, 2021, Financial Times story ["Small share of police draw third of complaints in big US cities"](https://www.ft.com/content/141182fc-7727-4af8-a555-5418fa46d09e). Read the findings and the computer code that drove the analysis at [analysis.ipynb](https://github.com/Financial-Times/police-misconduct-complaints-analysis/blob/main/analysis.ipynb).

## Data

The data for this analysis came from:

- **The Invisible Institute** (Chicago): The Invisible Institute filed a series of FOIA requests to the Chicago Police Department as part of its [Citizen Police Data Project](https://invisible.institute/police-data). The FT downloaded the datasets from the Invisible Institute's [GitHub repo](https://github.com/invinst/chicago-police-data/), and saved them to the [`input/chicago`](https://github.com/Financial-Times/police-misconduct-complaints-analysis/tree/main/input/chicago) directory. The code used to load and pre-process the data can be found at [`cleaning/chicago.ipynb`](https://github.com/Financial-Times/police-misconduct-complaints-analysis/blob/main/cleaning/chicago.ipynb).

- **The New York Civil Liberties Union** (NYC): The NYCLU filed a series of FOIA requests to NYC's Civilian Complaint Review Board to obtain its [NYPD Misconduct Complaint Database](https://www.nyclu.org/en/campaigns/nypd-misconduct-database). The FT downloaded the dataset from the NYCLU's [GitHub repo](https://github.com/new-york-civil-liberties-union/NYPD-Misconduct-Complaint-Database-Updated), and saved it to the [`input/nyc`](https://github.com/Financial-Times/police-misconduct-complaints-analysis/tree/main/input/nyc) directory. The code used to load and pre-process the data can be found at [`cleaning/nyc.ipynb`](https://github.com/Financial-Times/police-misconduct-complaints-analysis/blob/main/cleaning/nyc.ipynb).

- **OpenDataPhilly** and **Sam Learner** (Philadelphia): The Philadelphia Police Department releases data publicly on a trailing 5-year basis, meaning older data is overwritten by newly-released data. Data for 2016 onwards is from [OpenDataPhilly](https://www.opendataphilly.org/dataset/police-complaints), the city's open data website, and data for 2015 is from Sam Learner, who previously collected it for [another project](https://github.com/sdl60660/philly_police_complaints). The FT downloaded and saved the data to the [`input/philly`](https://github.com/Financial-Times/police-misconduct-complaints-analysis/tree/main/input/philly) directory. The code used to load and pre-process the data can be found at [`cleaning/philly.ipynb`](https://github.com/Financial-Times/police-misconduct-complaints-analysis/blob/main/cleaning/philly.ipynb).

The cities' data cannot be directly compared because each municipality records and investigates misconduct complaints differently, and the scope of the data obtained for each city is different. Below is a tabular representation of the differences in the raw data from each city:

| City 	| Most recent complaint recorded 	| Includes pending complaints 	| Includes complaints investigated by Internal Affairs 	| Includes complaints made by other officers 	| Multiple officers can be named under a single complaint 	| The same officer be named in multiple allegations under a single complaint 	| Each row in the data is a separate allegation 	|
|-	|-	|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|
| Chicago 	| March 2018 	| x 	| x 	| x 	| x 	|  	| x 	|
| NYC 	| February 2021 	|  	|  	|  	| x 	| x 	| x 	|
| Philadelphia | March 2021 	| x 	| n/a* 	|  	| x 	| x 	| x 	|

For more information, see the "Notes on the raw data" section in the notebooks for each city in the [`cleaning/`](https://github.com/Financial-Times/police-misconduct-complaints-analysis/tree/main/cleaning) directory. The cleaned data are saved in the [`output/`](https://github.com/Financial-Times/police-misconduct-complaints-analysis/tree/main/output) directory.

## Analysis

The FT's calculations for this story were done in R and are available at [analysis.ipynb](https://github.com/Financial-Times/police-misconduct-complaints-analysis/blob/main/analysis.ipynb).


## Licensing

All code in this repository is available under the GNU General Public License v3.0. The data in the [`input/`](https://github.com/Financial-Times/police-misconduct-complaints-analysis/tree/main/input) directory has been made public by the entities described above.
