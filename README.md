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
   - Gathered data from Wikipedia about cities in each US state.
   - Acquired population data from the US Census Bureau for each state.
   - Extracted regional divisions as defined by the US Census Bureau.

2. Article Quality Predictions using ORES
   - Used the ORES machine learning system to obtain quality scores for each Wikipedia article.
   - The quality scores range from "FA" (Featured article) to "Stub" (Stub-class article).
   - Ensured a log of articles for which quality scores could not be retrieved.

3. Data Integration
   - Combined Wikipedia data, population data, and regional division data using state names as the key.
   - Handled data inconsistencies and discrepancies during this merge.
   - Produced a final consolidated dataset: wp_scored_city_articles_by_state.csv.

4. Analysis
   - Calculated "articles-per-population" and "high-quality-articles-per-population" for each state.
   - Defined "high quality" articles as those predicted by ORES to be either "FA" or "GA".

5. Results Visualization
   - Produced tables highlighting states and census divisions based on their coverage and quality on Wikipedia.
   - Top and bottom 10 US states by coverage and quality.
   - Census divisions ranked by coverage and quality.

### Research Implications
Through this analysis, several insights and potential biases were observed. There might exist geographical biases, even in a well-resourced country like the US.

### Reflections on Findings:

1. Potential Biases:
   - Initially, an inherent bias towards populous states and major cities was expected.

2. Implications of Using Wikipedia as a Data Source:
   - The results suggest that while Wikipedia is a vast resource, it may not always provide an unbiased representation.
   - It's crucial to approach such data critically and consider potential biases.

3. Potential Issues in Data Science Research:
   - Using this data for certain research scenarios might perpetuate existing biases.

4. Situations Where Data Remains Useful:
   - Despite biases, there are scenarios where this data might be useful.

5. Suggestions for Improvement:
   - A researcher might supplement this dataset with information from local state-based resources or smaller community-driven encyclopedias to address limitations/biases.

### License
This project is licensed under the MIT License. Please see the LICENSE file for more details.

### Acknowledgements
- Wikipedia for the dataset about US cities.
- US Census Bureau for the population and regional division data.
- ORES for providing the article quality predictions.

### Contact Information
For any additional questions or feedback, please contact [Harshit Rai] at [harshit@uw.edu].