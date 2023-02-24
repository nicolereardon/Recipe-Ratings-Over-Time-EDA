<h1>Exploration of Recipe Ratings Over Time</h1>
<h4 id="creators">By: Lina Battikha & Nicole Reardon </h4>


<h5><em> The datasets that were used throughout this project can be found here: <a href = "https://dsc80.com/project3/recipes-and-ratings/food.com">food.com</a></em></h5>

<h1> Introduction </h1>
<p>Throughout the rest of the page, you will get a chance to explore different relationships between recipes and their ratings. The datasets that we used throughout this exploratory data analysis includes information about recipes between the years of 2008 and 2018 from the website Recipes.com. The first data frame, Raw Recipes,  contains relevant information about how to make the recipe (such as name, steps, ingredients, number of minutes it will take, etc.) as well as the id of the contributor and the date they submitted the recipe. The second data frame, Raw Interactions, contains information about ratings of the recipes (i.e. date submitted, number rating, and review) as well as the id of the user who wrote it and the id of the recipe it was for.</p>

<p>This dataset is useful for anyone who would like to further explore different factors of recipes and what possible trends may exist. Through our EDA, we were interested in looking at the relationship between recipes’ ratings and time. Such focus on this relationship would allow us to look at possible trends that may exist not only over all recipes but finding trends between the years as well. Given this, the question created to direct our analysis is:</p>

<h1>Question: What is the relationship between change in time and rating?<h1>

<h3>Number of Rows: 83782 rows</h3>
<h3>Relevant Columns: average_rating, minutes, nutrition, n_steps</h3>
<h3>Description of Columns: </h3>
<ul>
<li>average_ rating: average number of minutes for each recipe</li>
<li>minutes: the number of minutes it takes to make the recipe</li>
<li>n_steps: the number of steps in the recipe</li>
</ul>

<h4><em>Raw Recipes</em></h4>
<table border="1" class="dataframe">
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
    </tr>
  </tbody>
</table>


<h4><em>Raw Interactions</em></h4>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>user_id</th>
      <th>recipe_id</th>
      <th>date</th>
      <th>rating</th>
      <th>review</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1293707</td>
      <td>40893</td>
      <td>2011-12-21</td>
      <td>5</td>
      <td>So simple, so delicious! Great for chilly fall evening. Should have doubled it ;)&lt;br/&gt;&lt;br/&gt;Second time around, forgot the remaining cumin. We usually love cumin, but didn't notice the missing 1/2 teaspoon!</td>
    </tr>
    <tr>
      <td>126440</td>
      <td>85009</td>
      <td>2010-02-27</td>
      <td>5</td>
      <td>I made the Mexican topping and took it to bunko.  Everyone loved it.</td>
    </tr>
    <tr>
      <td>57222</td>
      <td>85009</td>
      <td>2011-10-01</td>
      <td>5</td>
      <td>Made the cheddar bacon topping, adding a sprinkling of black pepper. Yum!</td>
    </tr>
    <tr>
      <td>124416</td>
      <td>120345</td>
      <td>2011-08-06</td>
      <td>0</td>
      <td>Just an observation, so I will not rate.  I followed this procedure with strawberries instead of raspberries.  Perhaps this is the reason it did not work well.  Sorry to report that the strawberries I did in August were moldy in October.  They were stored in my downstairs fridge, which is very cold and infrequently opened.  Delicious and fresh-tasting prior to that, though.  So, keep a sharp eye on them.  Personally I would not keep them longer than a month.  This recipe also appears as #120345 posted in July 2009, which is when I tried it.  I also own the Edna Lewis cookbook in which this appears.</td>
    </tr>
    <tr>
      <td>2000192946</td>
      <td>120345</td>
      <td>2015-05-10</td>
      <td>2</td>
      <td>This recipe was OVERLY too sweet.  I would start out with 1/3 or 1/4 cup of sugar and jsut add on from there.  Just 2 cups was way too much and I had to go back to the grocery store to buy more raspberries because it made so much mix.  Overall, I would but the long narrow box or raspberries.  Its a perfect fit for the recipe plus a little extra.  I was not impressed with this recipe.  It was exceptionally over-sweet.  If you make this simple recipe, MAKE SURE TO ADD LESS SUGAR!</td>
    </tr>
  </tbody>
</table>


<p>The data frame we used during our analysis consisted of all of the columns of Raw Recipes along with the average rating of those recipes, obtained by calculating it in the Raw Recipes data frame. We will reference this data frame as Combined throughout the rest of this investigation. Before finding the average rating for each recipe, we filled any values with a rating of 0 with NaN. This is because a rating of 0 indicated that no rating of 0. If we were to keep those 0 values, the average rating of each recipe would lowered, thus incorrectly representing the average rating of the recipes.</p>

<h4><em>Original Dataframe with Average Rating Column</em></h4>

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


<h1>Cleaning and EDA</h1>
<p>As we would be referencing the submitted dates of the recipes, we then converted the string-stored dates to the DateTime type. This would allow for easier date manipulations in our analysis.</p>

<p>Another type-conversion we performed was on the nutrition, steps, and ingredient columns. They all appeared to be lists but were stored as strings, containing the macronutrient information, step-by-step explanation, and all needed ingredients, respectively, of each recipe. By converting the strings into actual lists, we were able to confirm that the listed number of steps and ingredients were correct. For the nutrition list, we also expanded the macros into separate columns that would allow us to easily access them individually.</p>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>name</th>
      <th>id</th>
      <th>submitted</th>
      <th>calories (#)</th>
      <th>total fat (PDV)</th>
      <th>sugar (PDV)</th>
      <th>sodium (PDV)</th>
      <th>protein (PDV)</th>
      <th>saturated fat (PDV)</th>
      <th>carbohydrates (PDV)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1 brownies in the world    best ever</td>
      <td>333281</td>
      <td>2008-10-27</td>
      <td>138.4</td>
      <td>10.0</td>
      <td>50.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>19.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <td>1 in canada chocolate chip cookies</td>
      <td>453467</td>
      <td>2011-04-11</td>
      <td>595.1</td>
      <td>46.0</td>
      <td>211.0</td>
      <td>22.0</td>
      <td>13.0</td>
      <td>51.0</td>
      <td>26.0</td>
    </tr>
    <tr>
      <td>412 broccoli casserole</td>
      <td>306168</td>
      <td>2008-05-30</td>
      <td>194.8</td>
      <td>20.0</td>
      <td>6.0</td>
      <td>32.0</td>
      <td>22.0</td>
      <td>36.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <td>millionaire pound cake</td>
      <td>286009</td>
      <td>2008-02-12</td>
      <td>878.3</td>
      <td>63.0</td>
      <td>326.0</td>
      <td>13.0</td>
      <td>20.0</td>
      <td>123.0</td>
      <td>39.0</td>
    </tr>
    <tr>
      <td>2000 meatloaf</td>
      <td>475785</td>
      <td>2012-03-06</td>
      <td>267.0</td>
      <td>30.0</td>
      <td>12.0</td>
      <td>12.0</td>
      <td>29.0</td>
      <td>48.0</td>
      <td>2.0</td>
    </tr>
  </tbody>
</table>


<h1>Univariate Visualizations</h1>
<h3>Proportion of Average Ratings</h3>
<iframe src="assets/uni_avg_rating_prop.html" width=800 height=600 frameBorder=0></iframe>
<p>This histogram reveals that most average ratings of the recipes are on the higher end. This could be explained by the observation that those who enjoyed the recipe are more likely to take the time to write a rating, rather than those who didn’t.</p>

<br><br>
<!-- <h3>Density Average Rating</h3>
<iframe src="assets/uni_density_avg_rating.html" width=800 height=600 frameBorder=0></iframe> -->

<h3>Percentage of Minutes With Outliers</h3>
<iframe src="assets/uni_percent_minutes_with_out" width=800 height=600 frameBorder=0></iframe>
<h3>Percentage of Minutes without Outliers</h3>
<iframe src="assets/uni_percent_minutes_without_out" width=800 height=600 frameBorder=0></iframe>
<p>The above histograms show the outliers that exist in the number of minutes needed to complete the recipe. By removing the largest 1% of recipes by minutes, the distribution of recipes that take roughly 2 hours or less is more easily seen. (The removal of outliers was only performed for the purpose of the visualization, the recipes were included for the remainder of the exploration.)</p>

<br><br>

<h3>Percentage of Recipes Each Year</h3>
<iframe src="assets/uni_recipes_per_year.html" width=800 height=600 frameBorder=0></iframe>
<p>This histogram shows the percentage of recipes that were submitted each year, most of which came in the earlier years and steadily decreased over time.</p>


<br><br>


<h1>Bivariate Visualizations</h1>

<h3>Histogram of Number of Steps Against Recipe Length with Outliers</h3>
<iframe src="assets/bi_step_min_with_out.html" width=800 height=600 frameBorder=0></iframe>
<h3>Histogram of Number of Steps Against Recipe Length without Outliers</h3>
<iframe src="assets/bi_step_min_without_out.html" width=800 height=600 frameBorder=0></iframe>
<p>The scatterplots below show some of the obvious outliers that exist in the number of minutes needed to complete the recipe. By removing the largest 1% of recipes by minutes, the scatter of step count and minutes shows clusters of recipes that occur every 30 minutes or so. (The removal of outliers was only performed for the purpose of the visualization, the recipes were included for the remainder of the exploration.)</p>

<br><br>

<h3>Barchart of the Number of Binned Ratings Per Year</h3>
<iframe src="assets/bi_fig_avg_year.html" width=800 height=600 frameBorder=0></iframe>
<p>This part chart shows that the majority of years have recipes that have ratings of [4,5] stars. Also, it shows that as the years progress, there is less data for each year. </p>
<br>
<br>

<h1>Intersting Aggregates</h1>

<h4>We added in a new column that groups ratings that are within a range, rounding down to the nearest rating. This table was used to make the last bivariate graph above.</h4>

<!-- WITH THE BINNED AVERAGES -->
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>average_rating</th>
      <th>rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1.000000</td>
      <td>[1,2) rating</td>
    </tr>
    <tr>
      <td>2.250000</td>
      <td>[2,3) rating</td>
    </tr>
    <tr>
      <td>3.090909</td>
      <td>[3,4) rating</td>
    </tr>
    <tr>
      <td>4.000000</td>
      <td>[4,5] rating</td>
    </tr>
    <tr>
      <td>5.000000</td>
      <td>[4,5] rating</td>
    </tr>
    <tr>
      <td>NaN</td>
      <td>missing</td>
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
    <tr>
      <th>year</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2008</th>
      <td>422.428191</td>
      <td>421.185000</td>
      <td>411.355490</td>
      <td>416.320136</td>
      <td>526.509973</td>
      <td>418.853056</td>
    </tr>
    <tr>
      <th>2009</th>
      <td>470.127007</td>
      <td>493.232719</td>
      <td>450.831211</td>
      <td>424.058527</td>
      <td>481.331949</td>
      <td>427.918326</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>381.831132</td>
      <td>382.088776</td>
      <td>478.289388</td>
      <td>413.078273</td>
      <td>455.627202</td>
      <td>416.971072</td>
    </tr>
    <tr>
      <th>2011</th>
      <td>353.375510</td>
      <td>403.381667</td>
      <td>465.259790</td>
      <td>453.480130</td>
      <td>516.164807</td>
      <td>454.808992</td>
    </tr>
    <tr>
      <th>2012</th>
      <td>564.124444</td>
      <td>427.792453</td>
      <td>482.936792</td>
      <td>420.192781</td>
      <td>451.114354</td>
      <td>425.329478</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>402.282353</td>
      <td>491.366667</td>
      <td>394.346711</td>
      <td>452.606506</td>
      <td>608.140000</td>
      <td>456.576134</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>571.213636</td>
      <td>532.757143</td>
      <td>478.654348</td>
      <td>469.851454</td>
      <td>548.863636</td>
      <td>478.593804</td>
    </tr>
    <tr>
      <th>2015</th>
      <td>305.150000</td>
      <td>1189.900000</td>
      <td>414.100000</td>
      <td>452.846000</td>
      <td>424.685714</td>
      <td>452.435621</td>
    </tr>
    <tr>
      <th>2016</th>
      <td>514.111111</td>
      <td>201.400000</td>
      <td>288.257143</td>
      <td>578.818301</td>
      <td>448.600000</td>
      <td>538.804902</td>
    </tr>
    <tr>
      <th>2017</th>
      <td>481.220000</td>
      <td>225.800000</td>
      <td>472.330769</td>
      <td>879.210053</td>
      <td>501.486111</td>
      <td>743.518750</td>
    </tr>
    <tr>
      <th>2018</th>
      <td>1905.725000</td>
      <td>1057.900000</td>
      <td>2148.163636</td>
      <td>713.726357</td>
      <td>1380.256818</td>
      <td>979.431746</td>
    </tr>
  </tbody>
</table>
<p>We used this pivot table to see how the average amount of calories per rating bin for each year changed. Just looking at this table, we noticed that 2018 had a significantly greater amount of calories across all ratings compared to other years. Also, it seems like the average amount of calories per year seems to be consistent across the rating bins. </p>
<br><br>


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
    <tr>
      <th>year</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2008</th>
      <td>352.739674</td>
      <td>366.274576</td>
      <td>382.124211</td>
      <td>380.881696</td>
      <td>425.104502</td>
      <td>381.695892</td>
    </tr>
    <tr>
      <th>2009</th>
      <td>421.317037</td>
      <td>402.992991</td>
      <td>395.740781</td>
      <td>384.419377</td>
      <td>426.262945</td>
      <td>386.536335</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>381.831132</td>
      <td>382.088776</td>
      <td>396.468132</td>
      <td>377.759070</td>
      <td>414.672513</td>
      <td>379.893378</td>
    </tr>
    <tr>
      <th>2011</th>
      <td>353.375510</td>
      <td>403.381667</td>
      <td>408.561922</td>
      <td>397.985848</td>
      <td>447.135526</td>
      <td>399.634114</td>
    </tr>
    <tr>
      <th>2012</th>
      <td>365.144186</td>
      <td>427.792453</td>
      <td>390.561058</td>
      <td>384.670204</td>
      <td>413.371498</td>
      <td>386.349347</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>402.282353</td>
      <td>391.578947</td>
      <td>394.346711</td>
      <td>396.973695</td>
      <td>372.864189</td>
      <td>395.907452</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>338.833333</td>
      <td>269.794737</td>
      <td>478.654348</td>
      <td>402.630839</td>
      <td>514.070769</td>
      <td>409.288190</td>
    </tr>
    <tr>
      <th>2015</th>
      <td>305.150000</td>
      <td>223.350000</td>
      <td>414.100000</td>
      <td>415.527935</td>
      <td>424.685714</td>
      <td>413.066887</td>
    </tr>
    <tr>
      <th>2016</th>
      <td>514.111111</td>
      <td>201.400000</td>
      <td>288.257143</td>
      <td>438.507432</td>
      <td>448.600000</td>
      <td>433.447739</td>
    </tr>
    <tr>
      <th>2017</th>
      <td>233.200000</td>
      <td>225.800000</td>
      <td>472.330769</td>
      <td>456.470556</td>
      <td>501.486111</td>
      <td>458.323741</td>
    </tr>
    <tr>
      <th>2018</th>
      <td>1330.666667</td>
      <td>1057.900000</td>
      <td>607.820000</td>
      <td>517.115079</td>
      <td>714.041026</td>
      <td>581.744134</td>
    </tr>
  </tbody>
</table>
<p>After looking into our data, we found that there was an outlier in 2018 that has an extremely high number of calories, which was skewing the results of our dataframe. To fix this, we kept only up until the 99th percentile of the calories and redid the pivot table. Looking at this pivot table, the amount of average calories per rating was still higher for 2018 compared to the other years. </p>
<br><br>

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
    <tr>
      <th>year</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2008</th>
      <td>69.688518</td>
      <td>54.910424</td>
      <td>29.231280</td>
      <td>35.438440</td>
      <td>101.405471</td>
      <td>37.157163</td>
    </tr>
    <tr>
      <th>2009</th>
      <td>48.809970</td>
      <td>90.239728</td>
      <td>55.090430</td>
      <td>39.639150</td>
      <td>55.069004</td>
      <td>41.381991</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>81.821257</td>
      <td>35.319203</td>
      <td>40.954689</td>
      <td>37.077694</td>
    </tr>
    <tr>
      <th>2011</th>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>56.697869</td>
      <td>55.494282</td>
      <td>69.029281</td>
      <td>55.174878</td>
    </tr>
    <tr>
      <th>2012</th>
      <td>198.980258</td>
      <td>0.000000</td>
      <td>92.375735</td>
      <td>35.522577</td>
      <td>37.742856</td>
      <td>38.980131</td>
    </tr>
  </tbody>
</table>
<p>We took the difference between the two pivot tables mentioned above to see how much each value changed once the outliers were removed. This would allow us to see how much each value changed when outliers were removed. </p>
<br><br>

<h1>Assessment of Missingness</h1>
<br>
<h4>Description Columns is NMAR</h4>
<p>The column we believe to be not missing at random is the description column. Given that the description of the recipe is not entirely necessary to make the dish, it is possible that the contributor thought the name of the recipe was sufficient or couldn’t be bothered to write one. An additional column that could explain the missingness would possibly be a difficulty column. Recipes that are easier or more simple would have a lower difficulty rating and we would expect to see the recipes with lower difficulty ratings would have more missing descriptions.</p>
<br><br>


<h4>Missing Completely at Random: Average Rating on Minutes</h4>
<iframe src="assets/mcar_fig_condition_on_minutes.html" width=800 height=600 frameBorder=0></iframe>
<p><strong>We found that the average rating conditional on minutes is Not Missing at Random (MCAR).</strong> We used a permutation test to come to the conclusion and found that the p-value is 0.382, which is greater than 0.05. when the missingness of the average rating was conditional on minutes. 
</p>




<h4>Missing at Random: Average Rating on Year</h4>
<iframe src="assets/mar_fig_condition_on_year.html" width=800 height=600 frameBorder=0></iframe>
<p><strong>We found the average rating conditional on year is Missing at Random (MAR).</strong> 
We used a permutation test to come to the conclusion and found that there was a p-value of 0.00 when the missingness of average rating was conditional on year. </p>

<h5><em>Both of these finds are shown through our permutation tests</em></h5>


<h1>Hypothesis Testing</h1>
<h5> Null Hypothesis: The distribution of rating bins for the year of 2018 is the same as the population distribution between the years of 2008 and 2018.</h5>
<h5>Alternative Hypothesis: The distribution of rating bins for 2018 is different than the distribution of bin ratings during </h5>
<br>
<h5>Choice of Test Statistics : Total Variation Distance (TVD)</h5>
<p>We chose to use this test statistics because we are looking at two groups of categorical data, years and rating bins.</p>
<h5>P-Value = 0.00</h5>
<h5>Conclusion</h5>
<p><storng>Reject the null hypothesis.</storng> This is because the p-value of 0.00 is less than 0.05. There is significant evidence to support the alternative hypothesis that the distribution of rating in 2018 is different from the overall population between the years of 2008-2018.</p>

<iframe src="assets/fig_hyp.html" width=800 height=600 frameBorder=0></iframe>

<p>This hypothesis test allowed us to look at whether the most recent year in the dataset follows the distribution of the populations, which is between the years of 2008-2018. By doing so, we are able to see if there is a significant difference in the distribution of ratings for 2018 compared to the population.</p>


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
	 	overflow: auto;
  	white-space: nowrap;
	 }
     /* tr{
         page-break-inside: avoid;
     } */

	 td{ 
	 	overflow: auto;
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


