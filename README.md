# Project Proposal
By James McCutcheon, Emily Tao, Sean Campbell, and Akhila Bhamidipati

## Project Description
-   What is the overarching purpose of your research project, and why is it an important undertaking?
> The overarching purpose for this project is to use sea surface temperature, fishing data, and tourism data to accurately predict when coral reefs in Hawaii might be at risk for bleaching. This will allow Hawaii and its citizens to be better informed and become activists with respect to the health of the ocean ecosystem.

> Coral reefs are underwater structures which are composed of the skeletal remains of corals. They are important in Hawaii because coral reefs protect coastlines from waves and storms. They are a habitat, shelter, and food for many marine organisms. Coral reefs help with carbon and nitrogen fixing, which helps algae survive. They are also very important for living organisms on earth because many land animals feed on marine animals, which means that a healthy marine ecosystem is necessary for survival. When coral reefs start to bleach, they become uninhabitable for various creatures and do not provide benefits to the surrounding ecosystem. It is increasingly important to people to know about the benefits of coral reefs, as the rise of global warming and tourism makes them more vulnerable to bleaching.

-   How does your research fit into the broader problem domain? You should cite  **at least 3 papers**  that help contextualize your research.
> From the UW Library database we found a peer reviewed paper with the title “Global warming, regional trends and inshore environmental conditions influence coral bleaching in Hawaii.” Information in this paper will help us fine tune our features to make our model more predictive. https://onlinelibrary.wiley.com/doi/full/10.1111/j.1365-2486.2004.00836.x

> Another peer reviewed article from the UW library database provides insight into the current measurements taken by NOAA. This research will be invaluable in helping us further understand coral bleaching. https://www-frontiersin-org.offcampus.lib.washington.edu/articles/10.3389/fmars.2018.00057/full

> A research paper written by researchers at the PNAS states that “... most activities of people (e.g., fishing, deforestation, nutrient enrichment, burning of fossil fuels, and use of toxic chemicals) either damage corals directly or damage them indirectly by adversely modifying interactions with their competitors, predators, pathogens, and mutualists.” This shows how our research will be helpful because it shows that even though there has been initial research done on the effects of coral reefs, people do not know the results and cannot act accordingly.
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC33228/

-   What  **specific hypothesis** (hypotheses) are you going to test?
> We will test whether we can use current temperature, tourism, and fishing data to predict whether a given reef is at risk for bleaching.

-   What are the datasets you'll be working with to answer this question? Please include relevant background describing the datasets you identify.
> We will be using data about coral reefs in Hawaii collected from the National Oceanic and Atmospheric Association (NOAA). This data set has time series data from 2001 with LAT/LONG, the water surface temperature, and the amount of bleaching that may be occurring. Additionally, we plan on finding data on tourism trends in Hawaii. The last data set we will utilize will have data about fishing near the reefs in Hawaii.


-   What  **statistical**  and  **machine learning methods** do you plan on using to test your hypothesis?
> We plan on using a random forest approach to predict data since that is a classification model (at risk for bleaching or not) that trains relatively fast. We will use univariate statistical tests to evaluate the various features across all datasets for inclusion in the model.

-   Who is your target audience for the resource you will build? Depending on the domain of your data, there may be a variety of audiences interested in using the dataset. You should hone in on one of these audiences.
> Our target audience is non-experts who are interested in learning more about the effects of coral reefs and how they are susceptible to bleaching. Specifically, we will target Hawaiian citizens and government agencies because hopefully this data will inspire and empower them to work towards saving the coral reefs.

-   What should your audience learn from your resource? Consider specific questions they may want to answer.
> Some questions we would like to answer for our audience are:
> 1. What are coral reefs?
> 2. Why are they important?
> 3. How does bleaching affect the local ecosystem?
> 4. How susceptible are Hawaiian coral reefs to bleaching?
> 5. When will coral reefs be susceptible to bleaching in Hawaii?
> 6. How does fishing affect the coral reefs?
> 7. How does tourism affect reefs in Hawaii?
> 8. (Potential) How does use of sunscreen affect reefs?


## Technical Description
-   What will be the format of your final web resource (Shiny app, HTML page or slideshow compiled with KnitR, etc.)?
> Our final resource will be a Jupyter notebook hosted on Github pages as a static HTML page.

-   Do you anticipate any specific data collection / data management challenges?
> I think one of the biggest challenges for our project will be to find fishing and tourism data that we can join with our coral bleaching and sea surface temperature data. We will need to find data that not only matches the location of our reef(s) of interest, but matches temporally too (at least as close as possible). Another challenge will be to select the right features of interest. Since we are pulling in so many data sets, we need to be careful with what data we use because it could take a long time to download and load data into python. Furthermore, selecting variables to use in our model will be challenging since there are many criteria we can use to assess the suitability of a variable (variation, univariate statistical tests, etc.)

-   What new technical skills will need to learn in order to complete your project?
> Our goal is to predict bleaching events using an algorithm that determines risk for bleaching based on light and heat stress to the coral. The technical skills we will need to learn for this project revolve around learning how to implement the algorithm and use it as a basis for modeling.

> https://www.mdpi.com/2072-4292/10/1/18

-   How will you conduct you analysis? Please include a  **detailed description**  of your intended modeling approach.
> When we say we want to predict bleaching events, we mean that we want to predict whether bleaching will occur or not. This is a classification problem. As such, we will most likely use a two class decision forest (however, we will test a few different models). A decision forest is very similar to a decision tree, but it constructs multiple decision trees at a time and returns the mode or mean prediction of the trees. A decision tree classifies observations based on rules about the values of the variables within the observation learned in testing data. This will work well since we need accuracy and fast model training times so that we can test multiple models and tune hyperparameters.

-   What major challenges do you anticipate?
> As previously discussed, the main challenge will be to find other data sets that we can use in conjunction with our main data set to predict the occurrence of coral bleaching. Another challenge will be to create a new variable as a combination of features. Research papers we have read have made it clear that both light and heat cause coral to bleach, but it will be hard to determine exactly which factors have the highest correlation and can be combined.

Link to Main Data Set: https://coralreefwatch.noaa.gov/satellite/vs/mainhawaiian.php
