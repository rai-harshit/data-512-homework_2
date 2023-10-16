### Overview
This project explores the concept of bias in data by analyzing Wikipedia articles about cities in different US states. The aim is to understand how the coverage of US cities on Wikipedia varies among states and how the quality of articles differs.

### Datasets
- `us_cities_by_state_SEPT.2023.csv`: A dataset listing Wikipedia article pages about US cities from each state.
- `NST-EST2022-POP.xlsx`: Population estimates for every US state.
- `US States by Region - US Census Bureau.xlsx`: Listing of states in each US census regional division.

### Dependencies
- Python 3
- Jupyter Notebook
- Pandas
- Requests

### Steps to Reproduce
1. Data Collection and Preprocessing
   - Gathered data from Wikipedia about cities in each US state. The API call takes about 2 hours to retrieve data for about 20,000+ articles.
   - After the initial city data acquisition, it was found that there were many duplicates. Those were dropped using Pandas' in-built function.
   - Acquired population data from the US Census Bureau for each state.
   - Extracted regional divisions as defined by the US Census Bureau.

2. Article Quality Predictions using ORES
   - Used the ORES machine learning system to obtain quality scores for each Wikipedia article.
   - The quality scores range from "FA" (Featured article) to "Stub" (Stub-class article).
   - The API call for 20,000+ articles took about 5 hours to complete. The initial round of calls produced about 4000 rows with errored predictions.
   - These errors were then resolved in the second round of API calls.

3. Data Integration
   - Combined Wikipedia data, population data, and regional division data using state names as the key.
   - Handled data inconsistencies and discrepancies during this merge.
   - Produced a final consolidated dataset: wp_scored_city_articles_by_state.csv.

4. Analysis
   - Calculated "articles-per-population" and "high-quality-articles-per-population" for each state.
   - Displayed the top 10 and bottom 10 states according to the aforementioned metrics.
   - Defined "high quality" articles as those predicted by ORES to be either "FA" or "GA".

5. Results Visualization
   - Produced tables highlighting states and census divisions based on their coverage and quality on Wikipedia.
   - Top and bottom 10 US states by coverage and quality.
   - Census divisions ranked by coverage and quality.

### Research Implications
Through this analysis, several insights and potential biases were observed. There might exist geographical biases, even in a well-resourced country like the US.

### Reflections on Findings:

1. Potential Biases:
   - Population Bias: This is the most common form of bias, where states or cities with larger populations get more attention and thus more detailed coverage. Conversely, less populated areas might receive fewer articles or lesser-detailed content.

   - Editorial Bias: Wikipedia, being a platform where anyone can contribute, is influenced by its editors' demographics. If certain demographic groups are overrepresented among Wikipedia editors, topics of interest to those groups might be covered more extensively.

   - Historical Bias: Articles might be biased towards events or facts that have received more media attention historically. For example, cities that have been historically significant or have seen major events might have more detailed articles.

   - Geographical Bias: Proximity to media centers or places with higher internet penetration can lead to more articles and more detailed coverage.

   - Temporal Bias: Events or developments that have occurred recently might get more coverage due to their recency, even if their long-term significance is uncertain.

2. Implications of Using Wikipedia as a Data Source:
   - Crowdsourced Knowledge: Wikipedia's strength lies in its vast number of contributors. However, this also means that the data's accuracy and neutrality depend on the contributors' objectivity and knowledge.

   - Vandalism and Misinformation: Given its open nature, Wikipedia is susceptible to vandalism or intentional misinformation, though there are robust systems in place to counteract this.

   - Citation Needed: Not all information on Wikipedia is well-cited. Relying on uncited facts can introduce inaccuracies into research.

   - Language and Cultural Perspective: Wikipedia articles can vary in detail and perspective based on the language or the cultural context of the article's primary contributors.

   - Dynamic Content: Wikipedia is continually updated. This dynamism can be both an advantage (up-to-date information) and a challenge (changing data baseline) for research purposes.

3. Potential Issues in Data Science Research:
   - Reinforcing Stereotypes: Algorithms trained on biased data can perpetuate and even amplify existing biases.

   - Skewed Predictions: Predictive models might produce results that favor overrepresented groups or entities in the dataset.

   - Loss of Trust: If end-users or stakeholders realize that a model's decisions are based on biased data, it can lead to a loss of trust in the model, the process, and the organization.

   - Ethical Implications: Making decisions based on skewed data, especially in critical areas like healthcare or law enforcement, can have severe ethical and societal implications.

   - Resource Misallocation: Decisions on resource allocation, based on skewed data, can lead to inefficiencies and missed opportunities.

4. Situations Where Data Remains Useful:
   - Initial Research: For a broad overview or a starting point in research, Wikipedia provides a comprehensive first look.

   - Trend Analysis: Given its dynamic nature, Wikipedia is great for understanding emerging trends or shifts in public interest.

   - Comparative Analysis: While absolute data might have biases, relative comparisons (e.g., comparing coverage of two cities) can still provide insights.

   - Cultural Insights: The way articles are written, the topics that are covered, and the details that are emphasized can provide cultural or societal insights.

   - Historical Records: Wikipedia often captures events and developments as they happen, serving as a historical record.

### License
This project is licensed under the MIT License. Please see the LICENSE file for more details.

### Acknowledgements
- Wikipedia for the dataset about US cities.
- US Census Bureau for the population and regional division data.
- ORES for providing the article quality predictions.

### Contact Information
For any additional questions or feedback, please contact [Harshit Rai] at [harshit@uw.edu].