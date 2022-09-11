# Contributing

- [Contributing](#contributing)
  - [General Guidelines](#general-guidelines)
  - [Suggested Questions](#suggested-questions)
    - [🏠 Comparing Outlet Stats](#-comparing-outlet-stats)
      - [Possible Question Settings](#possible-question-settings)
      - [Key Endpoints](#key-endpoints)
    - [🥘 Cuisine Analysis & Saturations](#-cuisine-analysis--saturations)
      - [Possible Question Settings](#possible-question-settings-1)
      - [Key Endpoints](#key-endpoints-1)
    - [🤺 Competitive Hot Spots](#-competitive-hot-spots)
      - [Possible Question Settings](#possible-question-settings-2)
      - [Key Endpoints](#key-endpoints-2)
    - [📍 Site Selection](#-site-selection)
      - [Possible Question Settings](#possible-question-settings-3)
      - [Key Endpoints](#key-endpoints-3)

## General Guidelines

Start with a question you want to answer. Questions can be broadly categorized into three types:
* **Type 1**: Questions that can be answered by "looking up" the data. Ex: *What is the population in Upper West Side, NY*
* **Type 2**: Questions that are clear but the answer requires a "level of infererence". ie, multiple data points need to be combined and a result has to be derived and cannot be approximated as a lookup problem. Ex: *Which branches of a huge chain are underperforming?*
* **Type 3**: Question vague and answer requires question distillation into Type 2 and Type 1. Ex: *Where should a restaurant setup a new location and why?* The question needs to be diluted to simpler questions and metrics need to be created. Such as what does it mean to justify a location choice

## Suggested Questions

Note that these are boilerplate questions can be modified / extended based on the use-case, depth of the study and so on. There is no obligation to stick to these questions. Contributors are encouraged to come up with their own questions. 

### 🏠 Comparing Outlet Stats

#### Possible Question Settings

* Comparative Statistics for all outlets of a particular brand in a city / country
* Metrics across a number of features such as driving time from locations, nearby competition and nearby demographics
* Result can be a ranked list of locations based on location suitability
* Possibly recommend certain locations to shut down

#### Key Endpoints
* [`https://api.dotlas.com/socio-demographics/sales_territory/time`](https://api.dotlas.com/docs#tag/Socio-demographics/operation/sales_territory_time_isochrone_socio_demographics_sales_territory_time_get)
* [`https://api.dotlas.com/socio-demographics/sales_territory/distance`](https://api.dotlas.com/docs#tag/Socio-demographics/operation/sales_territory_distance_isochrone_socio_demographics_sales_territory_distance_get)
* [`https://api.dotlas.com/competition/nearby/{commercial_type}`](https://api.dotlas.com/docs#tag/Competition/operation/nearby_outlets_competition_nearby__commercial_type__get)

### 🥘 Cuisine Analysis & Saturations

#### Possible Question Settings

* Which cuisine occurs the most in a city
* How does the cuisine correlate with outlet rating and locations?
* Are there clustered cuisine hotspots where a certain cuisine is saturating the market?
  * Ex: If a new outlet is setup in a neighbourhood where there are multiple restaurants of a particular cuisine, then what are the odds of success from the marginal contribution of the same cuisine in that restaurant?

#### Key Endpoints
* [`https://api.dotlas.com/competition/nearby/{commercial_type}`](https://api.dotlas.com/docs#tag/Competition/operation/nearby_outlets_competition_nearby__commercial_type__get)
* [`https://api.dotlas.com/competition/insights/categories/{city}/{commercial_type}`](https://api.dotlas.com/docs#tag/Competition/operation/city_categories_stats_competition_insights_categories__city___commercial_type__get)
* [`https://api.dotlas.com/competition/categories/{city}/{commercial_type}`](https://api.dotlas.com/docs#tag/Competition/operation/select_categories_competition_categories__city___commercial_type__get)

### 🤺 Competitive Hot Spots

#### Possible Question Settings

* What are the most competitive areas in a city for a restaurant?
* Where do most restaurants of a particular category or type share locations?
* Mark locations that would not be worth the "bang for buck" under this paradigm

#### Key Endpoints

### 📍 Site Selection

#### Possible Question Settings

* Which city, area and locations are most suitable to setup a restaurant business?

#### Key Endpoints

* All endpoints relevant to perform to a top-down analysis. 