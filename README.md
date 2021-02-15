# Covid-Blog-Post
Blog post for Udacity 'Write A Data Science Blog Post' assignment.

<h2> Motiviations </h2>

We've lived with covid for about a year now. As disastrous as it has been, it has also demonstrated the power of data in responding to real world situations. Our ability to fight covid has depended as much on our ability to collect and understand relevant data, using it to inform our actions, as it has on our health systems. This seemed like a natural place then to start a data science journey. Plus it fits the relevancy criteria laid out for being a good blog post. The questions I posed were simply the ones I thought would be interesting and doable with the time and data available to me.

<h2> Files </h2>

The repo contains three csv files containing relevant data, sourced as described below.

The main body of work is a Jypiter notebook. This contains the code used to answer the three questions posed in the blog post. The methods used were essentially inbuilt, but there are functions written to simplify some tasks and allow for experimenation. Most notably is pipe, this takes

* a DataFrame
* a target variable, target=str
* a list of predictor variables, predictors=[str]
* a list of categories to include historical data for, trailing =[str] - This should be a sublist of predictors
* a furthest day from which to include data either one integer or one per category, trail_n=int or [int]
* a closest day from which to include data either one integer or one per category, trail_to=int or [int]
* a smoothing level - if non-zero replace the target data with the n day trailing average, smooth=int
* a date range to work on, cutoffs=(date,date) - used with an loc call on dateTime index must be in an appropriate format

In spits out, in this order:
* Target and prediction data combined as a DataFrame
* Prediction variables
* Target data
* Predicted values
* a linear model

The repo also includes the markdown and images for the blog post for completeness but it renders poorly in Github's reader.

<h2> Packages </h2>

All the packages used come in a standard coda installation, besides adjustText. This is available via pip, or you can find the repo 
[here](https://github.com/Phyla/adjustText/).


<h2> Data Acknowledgments </h2>

The covid data all comes from [Our World in Data](https://ourworldindata.org/coronavirus).
The population density is courtesy of the [World Bank](https://data.worldbank.org/indicator/EN.POP.DNST).
Data on population weighted density comes from the European Commision's [Joint Research Centre](https://data.jrc.ec.europa.eu/dataset/jrc-luisa-udp-pwd-ref2016).





