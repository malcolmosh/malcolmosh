
🎺 💾 🎺 💾 🎺 💾 🎺 💾

Bonjour! I’m a graduate student completing his master’s of science
degree in business intelligence and data science at HEC Montréal. I’ve
helped bring multiple projects to life in the Québec creative and
cultural world for the past few years. Up to August 2021, I was program
manager at Zu Montreal, a creative hub for entertainment and technology.
Music was my first (academic) love - I have a bachelor’s in music from
the University of Montreal (2014), and a master’s in arts management
from HEC Montreal (2016).

Salut ! Je complète actuellement ma maîtrise en intelligence
d’affaires/science des données à HEC Montréal. Je compte traduire ce
petit texte bientôt.

## Recent projects:

### Social distancing calculator (2021)

<mark>**[Repo link here](https://github.com/malcolmosh/OptimisateurSalle_Roomoptimizer)**</mark>

**Language & Packages: Python (mostly NumPy, Pygame)**

This is a heuristic algorithm that optimizes the capacity of a
fixed-seat room with respect to social distancing. It ingests a set of
2D chair coordinates and numbers, and outputs a list of chairs to be
occupied. A GUI helps users import files, set their parameters and then observe the outcome. Data can then be exported from the app. Choosing the optimal number of chairs is an optimization problem. To focus on speed and simplicity, our heuristic strategy is that we loop a great number of times over a given algorithm and improve the initial solution only when the capacity increases. This means we are pretty sure to approximate the best possible result, especially in smaller rooms. 

There are a few parameters to set, including :

-   The social distance to set between each chair (in metres)
-   Whether you want to divide the room into independent sub-groups
-   The number of iterations without improvements the algorithm should run for
-   The maximum time the algorithm should run for (in minutes)
-   The research strategy
    -   The first chair is usually chosen randomly. Its neighbours that become inelegible are removed from play, and different research strategies are implemented to occupy the next chair. 

This group project was assembled for my class on algorithms for
optimization and big data. Contributors:

-   Mahnaz Gol
-   Emanuel Senay-Lussier

------------------------------------------------------------------------

### Hike Finder (2021)

<mark>**[Live version
here](https://osimhan.shinyapps.io/hikeapp/)**</mark>

**Language & Packages: R (mostly Shiny, googlesheets4, googleway,
dplyr)**

This is a proof of concept built in R and Shiny. It allows to choose a
hiking trail in Quebec based on certain conditions, including driving
distance.

The biggest selling point of this tool is that it calculates your
driving distance to all trails and lists the closest ones that match
your filters. The Google autocomplete and geocoding APIs are used to
standardize the address field and then transform it into a set of
coordinates. The googleway package is then used to inferface with the
Google Maps API, mostly to calculate driving distance.

Authentification is done through a .json file and an API key integrated
in the main R file.

The code includes a few secret API keys and so is not immediately
shareable, but I’m happy to share it on request.

------------------------------------------------------------------------

### Book recommender system (WIP - 2021)

**Language & Packages: Python**

This project suggests new books to a user based on their previous
ratings.

We delved into the
[Goobooks-10k](https://github.com/zygmuntz/goodbooks-10k) dataset, that
includes 6M individual reviews and 10 000 different books. The data was
merged with additional tags present in the [Best books ever
dataset](https://zenodo.org/record/4265096#.YY2Zny3pPUI), that contains
50 000 books. Missing descriptions for 1800 books were then scraped
through the Goodreads API, which bizarrely enough still works although
it was announced in December 2020 it would be discontinued. The cleaned
and agregated dataset will be released for public use soon.

A few strategies were applied to build efficient recommendations :

-   A baseline linear regression
-   Content-based filtering with NLP, using each book’s description
    (about 800 characters)
-   Collaborative filtering

Collaborators :

-   Yifan Yin
-   Jingyi Zou

------------------------------------------------------------------------

### Incubator stats : a simple dashboard for incubators (2021)

<mark>**[Live version
here](https://osimhan.shinyapps.io/incubator_dashboard/)**</mark>

**Language & Packages: R (Shiny, ggplot2, dplyr)**

**Link to repo: <https://github.com/malcolmosh/incubator_stats>**

This dashboard displays a few simple metrics and graphs in a readable
interface, with filtering options. The demo is [available
here](https://osimhan.shinyapps.io/incubator_dashboard/). Artificial
data was generated for this project and is stored in a [Google Sheets
here](https://docs.google.com/spreadsheets/d/1WFewCMyHGIhMgSNVD6vfElNVoEvY_duGKipdkK97K0Q/edit?usp=sharing).

Basically, this was an interesting foray into using Google Sheets as a
flexible data source. Multiple graphs are generated with ggplot2.

Note that the interface of this personal project is in French.

------------------------------------------------------------------------

### Tangerinr : a R package for analysing banking data (2021)

**Language & Packages: R (tidyverse, ggplot2)**

**Link to repo: <https://github.com/malcolmosh/tangerinr>**

This is a functional but still limited R package that can be installed
directly from Github. It can import debit statements from Tangerine Bank
(Canada) located in a local folder, aggregate them, and then produce
some simple visualizations.

This project was completed for my class on statistical software.
