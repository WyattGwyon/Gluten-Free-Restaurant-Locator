# Celiac's guide to restaurants in Madrid
The difficulties of finding reliable restaurant service for people who suffer from Celiacs disease can be stressful. Celiacs is a disease that is very sensitive to trace amounts of gluten (10pm) and requires attention to detail during food preparation. Any product that could have been contaminted with gluten during the preparation could cause the sufferer hours or days of distress.

Gluten is a protein found in wheat that when comes in contact with water forms bonds with other gluten protiens and sticks together creating an elastic structure that allows bread products to expand and stretch during preparation without breaking. It gives all bread products a pleasant chewiness that persists even when soaked in liquid like a soup or when coming into contact with saliva while chewing. 

Unfortunately, wheat flour is found in many other bakery products as a stabalizing ingredient. It can be used to make sauces thicker so sometimes spice mixtures contain small traces of flour for that effect. It can unintentionally get on the surface of products if they are processed on the same surfaces that process wheat or flour which means many nuts and beans can be contaminated unless they are washed well. Snack foods are suceptible to this because they contain spices they may and be produced in locations next to flour containing products. 

In conclusion, it is difficult to find a confident source of food for Celiacs. It requires, first, an awareness of the disease and its affects on the sufferers. 
We want to compile a database of restaurants for Celiacs in Madrid. 

### Checkout the `gf_map2.html` and `chain_price_rating2.html` in the creation folder for the results of our work. <br>The project is presented in `final_project.pdf` and all the work we did is within the Jupyter Notebooks.


# Process
**Step 1: Finding Data**
- A simple Google Map Search for Gluten-Free restaurants and yielded 20 locations. 
 - Using BeautifulSoup to scrape data from other Celiac-dedicated websites we increased our results to around 300 locales.
 - Then, more information was extracted about all the locations we found with a Google API Request.

**Step 2: Pre-Processing Data:**
- Select the precise keys containing the information of interest from API Request results. 
 - Create a pandas DataFrame from the selected information.
 - Various rounds of cleaning and adjusting information to make the data suitable for mapping and graphing.

**Step 3: Visualizing Data:**
- Folium was used to create the map and Markers were placed using geographic information in DataFrame.
 - LayerControl and FeatureGroup provided more selective toogling and popups and tooltips provided info at each Marker.
 - Passed a GeoJSON set of coordinates through Choropleth to define the neighborhoods of Madrid.
 - Using a Plotly Sunburst graphic we were able to clearly demonstrate the relation b/w many aspects at once.

# Next Steps
1. Create richer information in the popups, including photos, correct street address, reviews...

2. Connect a Flask API to a Mongodb in order to access and enter data like reviews. 

3. Modify search results based on your location or selected location.
