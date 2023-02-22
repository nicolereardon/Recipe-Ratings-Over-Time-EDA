### Recipe-Ratings-Over-Time-EDA
# Introduction
** Still need to include introduction **
## Question: What is the relationship between change in time and rating?

##### Original Dataframe with Average Rating Column

This is a part of the dataframe that we used that has all the recipes and their respective average ratings. 

<iframe id  = "combined_avg_rating" src="assets/combined_avg_rating.html" width = 500 height = 350 frameBorder = 0></iframe>


Interaction Dataframe 
**insert interaction df** 

We merged the Recipes dataframe and the Interaction dataframe to get the average rating for each recipe. We then merged the averages that we attained with the Recipes dataframe, shown below. 


We used this data frame throughout the rest of our exploration and analysis
**inter the df with recipes and average rating** 


# Cleaning and EDA
** Data cleaning steps in detail **
### Univariate Visualizations
Proportion of Average Ratings
<iframe src="assets/uni_avg_rating_prop.html" width=800 height=600 frameBorder=0></iframe>

Density Average Rating
<iframe src="assets/uni_density_avg_rating.html" width=800 height=600 frameBorder=0></iframe>

Percentage of Minutes With Outliers
<iframe src="assets/uni_percent_minutes_with_out" width=800 height=600 frameBorder=0></iframe>

Percentage of Minutes without Outliers
<iframe src="assets/uni_percent_minutes_without_out" width=800 height=600 frameBorder=0></iframe>

Percentage of Recipes Each Year
<iframe src="assets/uni_recipes_per_year.html" width=800 height=600 frameBorder=0></iframe>

### Bivariate Visualizations
Histogram of Minutes Against Steps
<iframe src="assets/bi_min_steps_hist.html" width=800 height=600 frameBorder=0></iframe>

Histogram of Number of Steps Against Recipe Length with Outliers
<iframe src="assets/bi_step_min_with_out.html" width=800 height=600 frameBorder=0></iframe>

Histogram of Number of Steps Against Recipe Length without Outliers
<iframe src="assets/bi_step_min_without_out.html" width=800 height=600 frameBorder=0></iframe>

# Assessment of Missingness
Missing Completely at Random: Average Rating on Minutes
<iframe src="assets/mcar_fig_condition_on_minutes.html" width=800 height=600 frameBorder=0></iframe>

Missing at Random: Average Rating on Year
<iframe src="assets/mar_fig_condition_on_year.html" width=800 height=600 frameBorder=0></iframe>

# Hypothesis Testing
Hypothesis Test
<iframe src="assets/fig_hyp.html" width=800 height=600 frameBorder=0></iframe>


<style>
	#id  = "combined_avg_rating {
      width: 120%;
      height: 70%;
      font-style: Helvetca;
      font-size: 16px;
   }
</style>
