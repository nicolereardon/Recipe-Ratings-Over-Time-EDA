<h1>Exploration of Recipe Ratings Over Time</h1>
<h4 id="creators">By: Lina Battikha & Nicole Reardon </h4>


<h5><em> The datasets that were used throughout this project can be found here: <a href = "https://dsc80.com/project3/recipes-and-ratings/food.com">food.com</a></em></h5>

<h1> Introduction </h1>
** Still need to include introduction **
<h1>Question: What is the relationship between change in time and rating?<h1>

<h4><em>Original Dataframe with Average Rating Column</em></h4>

This is a part of the dataframe that we used that has all the recipes and their respective average ratings. 

<table border="1" class="dataframe" id = "combined_avg_rating">
  <thead>
    <tr style="text-align: right;">
      <th>name</th>
      <th>id</th>
      <th>minutes</th>
      <th>contributor_id</th>
      <th>submitted</th>
      <th>tags</th>
      <th>nutrition</th>
      <th>n_steps</th>
      <th>steps</th>
      <th>description</th>
      <th>ingredients</th>
      <th>n_ingredients</th>
      <th>average_rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1 brownies in the world    best ever</td>
      <td>333281</td>
      <td>40</td>
      <td>985201</td>
      <td>2008-10-27</td>
      <td>['60-minutes-or-less', 'time-to-make', 'course', 'main-ingredient', 'preparation', 'for-large-groups', 'desserts', 'lunch', 'snacks', 'cookies-and-brownies', 'chocolate', 'bar-cookies', 'brownies', 'number-of-servings']</td>
      <td>[138.4, 10.0, 50.0, 3.0, 3.0, 19.0, 6.0]</td>
      <td>10</td>
      <td>['heat the oven to 350f and arrange the rack in the middle', 'line an 8-by-8-inch glass baking dish with aluminum foil', 'combine chocolate and butter in a medium saucepan and cook over medium-low heat , stirring frequently , until evenly melted', 'remove from heat and let cool to room temperature', 'combine eggs , sugar , cocoa powder , vanilla extract , espresso , and salt in a large bowl and briefly stir until just evenly incorporated', 'add cooled chocolate and mix until uniform in color', 'add flour and stir until just incorporated', 'transfer batter to the prepared baking dish', 'bake until a tester inserted in the center of the brownies comes out clean , about 25 to 30 minutes', 'remove from the oven and cool completely before cutting']</td>
      <td>these are the most; chocolatey, moist, rich, dense, fudgy, delicious brownies that you'll ever make.....sereiously! there's no doubt that these will be your fav brownies ever for you can add things to them or make them plain.....either way they're pure heaven!</td>
      <td>['bittersweet chocolate', 'unsalted butter', 'eggs', 'granulated sugar', 'unsweetened cocoa powder', 'vanilla extract', 'brewed espresso', 'kosher salt', 'all-purpose flour']</td>
      <td>9</td>
      <td>4.0</td>
    </tr>
    <tr>
      <td>1 in canada chocolate chip cookies</td>
      <td>453467</td>
      <td>45</td>
      <td>1848091</td>
      <td>2011-04-11</td>
      <td>['60-minutes-or-less', 'time-to-make', 'cuisine', 'preparation', 'north-american', 'for-large-groups', 'canadian', 'british-columbian', 'number-of-servings']</td>
      <td>[595.1, 46.0, 211.0, 22.0, 13.0, 51.0, 26.0]</td>
      <td>12</td>
      <td>['pre-heat oven the 350 degrees f', 'in a mixing bowl , sift together the flours and baking powder', 'set aside', 'in another mixing bowl , blend together the sugars , margarine , and salt until light and fluffy', 'add the eggs , water , and vanilla to the margarine / sugar mixture and mix together until well combined', 'add in the flour mixture to the wet ingredients and blend until combined', 'scrape down the sides of the bowl and add the chocolate chips', 'mix until combined', 'scrape down the sides to the bowl again', 'using an ice cream scoop , scoop evenly rounded balls of dough and place of cookie sheet about 1 - 2 inches apart to allow for spreading during baking', 'bake for 10 - 15 minutes or until golden brown on the outside and soft &amp; chewy in the center', 'serve hot and enjoy !']</td>
      <td>this is the recipe that we use at my school cafeteria for chocolate chip cookies. they must be the best chocolate chip cookies i have ever had! if you don't have margarine or don't like it, then just use butter (softened) instead.</td>
      <td>['white sugar', 'brown sugar', 'salt', 'margarine', 'eggs', 'vanilla', 'water', 'all-purpose flour', 'whole wheat flour', 'baking soda', 'chocolate chips']</td>
      <td>11</td>
      <td>5.0</td>
    </tr>
    <tr>
      <td>412 broccoli casserole</td>
      <td>306168</td>
      <td>40</td>
      <td>50969</td>
      <td>2008-05-30</td>
      <td>['60-minutes-or-less', 'time-to-make', 'course', 'main-ingredient', 'preparation', 'side-dishes', 'vegetables', 'easy', 'beginner-cook', 'broccoli']</td>
      <td>[194.8, 20.0, 6.0, 32.0, 22.0, 36.0, 3.0]</td>
      <td>6</td>
      <td>['preheat oven to 350 degrees', 'spray a 2 quart baking dish with cooking spray , set aside', 'in a large bowl mix together broccoli , soup , one cup of cheese , garlic powder , pepper , salt , milk , 1 cup of french onions , and soy sauce', 'pour into baking dish , sprinkle remaining cheese over top', 'bake for 25 minutes or until cheese is lightly browned', 'sprinkle with rest of french fried onions and bake until onions are browned and cheese is bubbly , about 10 more minutes']</td>
      <td>since there are already 411 recipes for broccoli casserole posted to "zaar" ,i decided to call this one  #412 broccoli casserole.i don't think there are any like this one in the database. i based this one on the famous "green bean casserole" from campbell's soup. but i think mine is better since i don't like cream of mushroom soup.submitted to "zaar" on may 28th,2008</td>
      <td>['frozen broccoli cuts', 'cream of chicken soup', 'sharp cheddar cheese', 'garlic powder', 'ground black pepper', 'salt', 'milk', 'soy sauce', 'french-fried onions']</td>
      <td>9</td>
      <td>5.0</td>
    </tr>
    <tr>
      <td>millionaire pound cake</td>
      <td>286009</td>
      <td>120</td>
      <td>461724</td>
      <td>2008-02-12</td>
      <td>['time-to-make', 'course', 'cuisine', 'preparation', 'occasion', 'north-american', 'desserts', 'american', 'southern-united-states', 'dinner-party', 'holiday-event', 'cakes', 'dietary', 'christmas', 'thanksgiving', 'low-sodium', 'low-in-something', 'taste-mood', 'sweet', '4-hours-or-less']</td>
      <td>[878.3, 63.0, 326.0, 13.0, 20.0, 123.0, 39.0]</td>
      <td>7</td>
      <td>['freheat the oven to 300 degrees', 'grease a 10-inch tube pan with butter , dust the bottom and sides with flour , and set aside', 'in a large mixing bowl , cream the butter and sugar with an electric mixer and add the eggs one at a time , beating after each addition', 'alternately add the flour and milk , stirring till the batter is smooth', 'add the two extracts and stir till well blended', 'scrape the batter into the prepared pan and bake till a cake tester or knife blade inserted in the center comes out clean , about 1 1 / 2 hours', 'cool the cake in the pan on a rack for 5 minutes , then turn it out on the rack to cool completely']</td>
      <td>why a millionaire pound cake?  because it's super rich!  this scrumptious cake is the pride of an elderly belle from jackson, mississippi.  the recipe comes from "the glory of southern cooking" by james villas.</td>
      <td>['butter', 'sugar', 'eggs', 'all-purpose flour', 'whole milk', 'pure vanilla extract', 'almond extract']</td>
      <td>7</td>
      <td>5.0</td>
    </tr>
    <tr>
      <td>2000 meatloaf</td>
      <td>475785</td>
      <td>90</td>
      <td>2202916</td>
      <td>2012-03-06</td>
      <td>['time-to-make', 'course', 'main-ingredient', 'preparation', 'main-dish', 'potatoes', 'vegetables', '4-hours-or-less', 'meatloaf', 'simply-potatoes2']</td>
      <td>[267.0, 30.0, 12.0, 12.0, 29.0, 48.0, 2.0]</td>
      <td>17</td>
      <td>['pan fry bacon , and set aside on a paper towel to absorb excess grease', 'mince yellow onion , red bell pepper , and add to your mixing bowl', 'chop garlic and set aside', 'put 1tbsp olive oil into a saut pan , along with chopped garlic , teaspoons white pepper and a pinch of kosher salt', 'bring to a medium heat to sweat your garlic', 'preheat oven to 350f', 'coarsely chop your baby spinach add to your heated pan , stir frequently for approximately 5 min to wilt', 'add your spinach to the mixing bowl', 'chop your now cooled bacon , and add it to the mixing bowl', 'add your meatloaf mix to the bowl , with one egg and mix till thoroughly combined', 'add your goat cheese , one egg , 1 / 8 tsp white pepper and 1 / 8 tsp of kosher salt and mix till thoroughly combined', 'transfer to a 9x5 meatloaf pan , and cook for 60 min or until the internal temperature is at least 160f', 'let stand for 5min', 'melt 1tbsp unsalted butter into a frying pan , and cook up to three eggs at a time', 'crack each egg into a separate dish , in order to prevent egg shells from reaching the pan , then add salt and pepper to taste', 'wait until the egg whites are firm looking , but slightly runny on top before flipping your eggs', 'after flipping , wait 10~20 seconds before removing each egg and placing it over your slices of meatloaf']</td>
      <td>ready, set, cook! special edition contest entry: a mediterranean flavor inspired meatloaf dish. featuring: simply potatoes - shredded hash browns, egg, bacon, spinach, red bell pepper, and goat cheese.</td>
      <td>['meatloaf mixture', 'unsmoked bacon', 'goat cheese', 'unsalted butter', 'eggs', 'baby spinach', 'yellow onion', 'red bell pepper', 'simply potatoes shredded hash browns', 'fresh garlic', 'kosher salt', 'white pepper', 'olive oil']</td>
      <td>13</td>
      <td>5.0</td>
    </tr>
  </tbody>
</table>





<!-- We merged the Recipes dataframe and the Interaction dataframe to get the average rating for each recipe. We then merged the averages that we attained with the Recipes dataframe, shown below.  -->


**We used this data frame throughout the rest of our exploration and analysis**


<h1>Cleaning and EDA</h1>
** Data cleaning steps in detail **
<h1>Univariate Visualizations</h1>
<h3>Proportion of Average Ratings</h3>
<iframe src="assets/uni_avg_rating_prop.html" width=800 height=600 frameBorder=0></iframe>
<br>
<!-- <h3>Density Average Rating</h3>
<iframe src="assets/uni_density_avg_rating.html" width=800 height=600 frameBorder=0></iframe> -->

<h3>Percentage of Minutes With Outliers</h3>
<iframe src="assets/uni_percent_minutes_with_out" width=800 height=600 frameBorder=0></iframe>
<br>
<h3>Percentage of Minutes without Outliers</h3>
<iframe src="assets/uni_percent_minutes_without_out" width=800 height=600 frameBorder=0></iframe>
<br>
<h3>Percentage of Recipes Each Year</h3>
<iframe src="assets/uni_recipes_per_year.html" width=800 height=600 frameBorder=0></iframe>
<br>
<br>


<h1>Bivariate Visualizations</h1>

<h3>Histogram of Minutes Against Steps</h3>
<iframe src="assets/bi_min_steps_hist.html" width=800 height=600 frameBorder=0></iframe>
<br>

<h3>Histogram of Number of Steps Against Recipe Length with Outliers</h3>
<iframe src="assets/bi_step_min_with_out.html" width=800 height=600 frameBorder=0></iframe>
<br>

<h3>Histogram of Number of Steps Against Recipe Length without Outliers</h3>
<iframe src="assets/bi_step_min_without_out.html" width=800 height=600 frameBorder=0></iframe>
<br>
<br>

<h1>Intersting Aggregates</h1>

<h4>We added in a new column that groups ratings that are within a range, rounding down to the nearest rating. </h4>

<!-- WITH THE BINNED AVERAGES -->
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>id</th>
      <th>average_rating</th>
      <th>rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>333281</td>
      <td>4.0</td>
      <td>[4,5] rating</td>
    </tr>
    <tr>
      <td>453467</td>
      <td>5.0</td>
      <td>[4,5] rating</td>
    </tr>
    <tr>
      <td>306168</td>
      <td>5.0</td>
      <td>[4,5] rating</td>
    </tr>
    <tr>
      <td>286009</td>
      <td>5.0</td>
      <td>[4,5] rating</td>
    </tr>
    <tr>
      <td>475785</td>
      <td>5.0</td>
      <td>[4,5] rating</td>
    </tr>
  </tbody>
</table>

<h4>Pivot Table - Aggregating the Mean of Calories per Rating Over Years With Outliers</h4>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>rating</th>
      <th>[1,2) rating</th>
      <th>[2,3) rating</th>
      <th>[3,4) rating</th>
      <th>[4,5] rating</th>
      <th>missing</th>
      <th>average</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th></th>
      <td>422.428191</td>
      <td>421.185000</td>
      <td>411.355490</td>
      <td>416.320136</td>
      <td>526.509973</td>
      <td>418.853056</td>
    </tr>
    <tr>
      <th></th>
      <td>470.127007</td>
      <td>493.232719</td>
      <td>450.831211</td>
      <td>424.058527</td>
      <td>481.331949</td>
      <td>427.918326</td>
    </tr>
    <tr>
      <th></th>
      <td>381.831132</td>
      <td>382.088776</td>
      <td>478.289388</td>
      <td>413.078273</td>
      <td>455.627202</td>
      <td>416.971072</td>
    </tr>
    <tr>
      <th></th>
      <td>353.375510</td>
      <td>403.381667</td>
      <td>465.259790</td>
      <td>453.480130</td>
      <td>516.164807</td>
      <td>454.808992</td>
    </tr>
    <tr>
      <th></th>
      <td>564.124444</td>
      <td>427.792453</td>
      <td>482.936792</td>
      <td>420.192781</td>
      <td>451.114354</td>
      <td>425.329478</td>
    </tr>
  </tbody>
</table>

<h4>Pivot Table - Aggregating the Mean of Calories per Rating Over Years Without Outliers</h4>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>rating</th>
      <th>[1,2) rating</th>
      <th>[2,3) rating</th>
      <th>[3,4) rating</th>
      <th>[4,5] rating</th>
      <th>missing</th>
      <th>average</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th></th>
      <td>352.739674</td>
      <td>366.274576</td>
      <td>382.124211</td>
      <td>380.881696</td>
      <td>425.104502</td>
      <td>381.695892</td>
    </tr>
    <tr>
      <th></th>
      <td>421.317037</td>
      <td>402.992991</td>
      <td>395.740781</td>
      <td>384.419377</td>
      <td>426.262945</td>
      <td>386.536335</td>
    </tr>
    <tr>
      <th></th>
      <td>381.831132</td>
      <td>382.088776</td>
      <td>396.468132</td>
      <td>377.759070</td>
      <td>414.672513</td>
      <td>379.893378</td>
    </tr>
    <tr>
      <th></th>
      <td>353.375510</td>
      <td>403.381667</td>
      <td>408.561922</td>
      <td>397.985848</td>
      <td>447.135526</td>
      <td>399.634114</td>
    </tr>
    <tr>
      <th></th>
      <td>365.144186</td>
      <td>427.792453</td>
      <td>390.561058</td>
      <td>384.670204</td>
      <td>413.371498</td>
      <td>386.349347</td>
    </tr>
  </tbody>
</table>

<h4>Difference Between the Two Pivot Tables Above</h4>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>rating</th>
      <th>[1,2) rating</th>
      <th>[2,3) rating</th>
      <th>[3,4) rating</th>
      <th>[4,5] rating</th>
      <th>missing</th>
      <th>average</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th></th>
      <td>69.688518</td>
      <td>54.910424</td>
      <td>29.231280</td>
      <td>35.438440</td>
      <td>101.405471</td>
      <td>37.157163</td>
    </tr>
    <tr>
      <th></th>
      <td>48.809970</td>
      <td>90.239728</td>
      <td>55.090430</td>
      <td>39.639150</td>
      <td>55.069004</td>
      <td>41.381991</td>
    </tr>
    <tr>
      <th></th>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>81.821257</td>
      <td>35.319203</td>
      <td>40.954689</td>
      <td>37.077694</td>
    </tr>
    <tr>
      <th></th>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>56.697869</td>
      <td>55.494282</td>
      <td>69.029281</td>
      <td>55.174878</td>
    </tr>
    <tr>
      <th></th>
      <td>198.980258</td>
      <td>0.000000</td>
      <td>92.375735</td>
      <td>35.522577</td>
      <td>37.742856</td>
      <td>38.980131</td>
    </tr>
  </tbody>
</table>



<h1>Assessment of Missingness</h1>
<h4>Missing Completely at Random: Average Rating on Minutes</h4>
<iframe src="assets/mcar_fig_condition_on_minutes.html" width=800 height=600 frameBorder=0></iframe>

<h4>Missing at Random: Average Rating on Year</h4>
<iframe src="assets/mar_fig_condition_on_year.html" width=800 height=600 frameBorder=0></iframe>

<h1>Hypothesis Testing</h1>
<iframe src="assets/fig_hyp.html" width=800 height=600 frameBorder=0></iframe>



<style> 
	table{ 
		table-layout: fixed; 
		border-collapse: collapse;
		width: 150%;
        /*margin-left: auto;
        margin-right: auto;
*/      
/*		word-wrap: break-word;*/

/*        margin-right:auto;*/
        margin-right:60%;
        overflow: scroll;
		/*width: 100; 
		height:350px;*/ 
	 }
	 th{
	 	width:150%;
	 	overflow: scroll;
  	white-space: nowrap;
	 }
     /* tr{
         page-break-inside: avoid;
     } */

	 td{ 
	 	overflow: scroll;
	 	white-space: nowrap;
        word-wrap: break-word;
	 	width: 200%;

	 	/*width:60%;
	 	overflow: hidden;*/
/*    	white-space:nowrap;*/
	  }
	  body{
	  	font-family: Helvetica, Sans-Serif;

	  }
    h1{
      font-family: Helvetica, Sans-Serif;
      color:#4B7A5C;
     }
    h4{
      color:#699A7B;

    }
    #creators{
      color: black;
    }


	/*  .page {
        @include container;
    }*/


</style>


