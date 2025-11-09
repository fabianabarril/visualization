# Data Visualization

## Assignment 3: Final Project

### Requirements:
- We will finish this class by giving you the chance to use what you have learned in a practical context, by creating data visualizations from raw data. 
- Choose a dataset of interest from the [City of Toronto’s Open Data Portal](https://www.toronto.ca/city-government/data-research-maps/open-data/) or [Ontario’s Open Data Catalogue](https://data.ontario.ca/). 
- Using Python and one other data visualization software (Excel or free alternative, Tableau Public, any other tool you prefer), create two distinct visualizations from your dataset of choice.  
- For each visualization, describe and justify: 

#### FIRST VISUALIZATION:

    > What software did you use to create your data visualization?
    Python (Pandas, Seaborn, Matplotlib)

    > Who is your intended audience? 
    Policy Makers and Comparative Education Researchers. This visualization is for evaluating structural differences in student outcomes.
    Interested parents can also find it useful.

    > What information or message are you trying to convey with your visualization? 
    The visualization compares the central tendency (median) and variability (Interquartile Range) of Grade 3 Reading achievement across different types of school boards (English Public, English Catholic, French). It identifies if a particular board type is associated with a wider spread of outcomes or a consistently higher/lower median.
    
    > What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots? 
    Visualization Type (Box Plot): A Box Plot was chosen over a scatter plot to manage high data volume. It effectively summarizes the distribution of thousands of schools into five key statistics (minimum, 25th percentile, median, 75th percentile, maximum/outliers), ensuring immediate clarity. Integrity (Y-Axis Filter): Filtering the data to remove the suppressed 0% scores and setting the Y-axis to focus on the meaningful range prevents the true distribution from being compressed or hidden.
    
    > How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 
    Reproducible by: using a single, self-contained script that imports the raw Excel file; all steps—from data cleaning (converting non-numeric data to NaN), to the critical data fix (multiplying decimal percentages by 100), to the filtering (removing suppressed scores), and finally, the plotting (using Seaborn's boxplot)—are explicitly coded; anyone running the script on the same raw data file will generate the identical plot, ensuring transparency and verifiability.
    If the Python code were not reproducible it would introduce the potential for human error at every stage (filtering, scaling, aggregation). This would lead to a lack of trust in the results, as external parties (e.g., policy makers, researchers) could not verify the median and quartile values shown in the box plot, undermining the entire analytical conclusion about board type performance.
    
    > How did you ensure that your data visualization is accessible?
    Color and contrast: The Box Plot utilizes a colorblind-safe or pastel-based palette ("Pastel1" in Seaborn) for the different board types, ensuring that the distinctions between the boxes are perceivable even without full color vision.
    Clarity and Layout: the plot uses the Y-axis limits to focus the data range (30% to 100%), preventing visual compression.  
    
    > Who are the individuals and communities who might be impacted by your visualization?
    Policy Makers & Ministry Officials are directly impacted by the Box Plot, which highlights systemic gaps (e.g., the low median of the "Public School Board" category). These results can trigger curriculum reviews and changes to provincial funding formulas aimed at improving equity.
    
    > How did you choose which features of your chosen dataset to include or exclude from your visualization?
    Included: Board Type and the standardized Percentage of Grade 3 Students Achieving the Provincial Standard in Reading. Excluded: Location or individual school identifiers. Justification: Focusing on Board Type allows for a macro-level comparison of the three primary education systems in Ontario (Public, Catholic, French), which is a key structural analysis point.
    
    > What ‘underwater labour’ contributed to your final data visualization product?
    The critical step was standardizing the achievement rates (multiplying decimals by 100) and filtering out suppressed data (5% achievement) to ensure the medians and quartile ranges shown in the box plot are accurate and not skewed by reporting artifacts.


#### SECOND VISUALIZATION:

    > What software did you use to create your data visualization?
    Python (Pandas) to perform the data aggregation, sorting, and filtering into a reproducible source file, and Microsoft Excel to render the final chart

    > Who is your intended audience? 
    Parents and Local School Board Trustees. This audience is primarily interested in the performance of their local board relative to others, making a direct, easy-to-read comparison essential for local decision-making and advocacy.

    > What information or message are you trying to convey with your visualization? 
    The visualization conveys a direct, comparative ranking of foundational literacy performance (Grade 3 Reading) across the ten highest-achieving school boards. The message is to benchmark and highlight heterogeneity in outcomes, allowing the audience to quickly identify high-performing systems.
    
    > What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots?
    Preattentive Attribute: Length - The length of the horizontal bars is the primary visual metric. The difference in bar length directly and accurately reflects the difference in achievement percentages (e.g., an 80% bar is clearly shorter than a 90% bar).
    Aesthetic: Clarity - The horizontal orientation was chosen specifically to ensure that the long Board Name labels are fully legible and prevent text overlap, which maximizes scannability.
    
    > How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 
    The process is reproducible because the data aggregation and filtering logic is fully contained within a Python script. The Excel part is reduced to a simple, manual action of selecting two columns and inserting a chart, which removes the ambiguity of the manual PivotTable process. If I had used Excel to create a pivot table instead, it would not be considered reproducible.

    > How did you ensure that your data visualization is accessible?
    Clarity and layout: Bar Chart - the horizontal orientation is critical because it allows for the full, legible spelling of long categorical labels (e.g., "Public Dist Sch Brd (E/F)"), which is essential for screen readers and users who require larger text.
    Text and Annotations: all axis labels and the main title are large and clear.
    
    > Who are the individuals and communities who might be impacted by your visualization?
    School Board Trustees & Administrators, they are directly compared in the Horizontal Bar Chart. This comparison drives accountability, strategic planning, and local decisions on allocating per-student resources or hiring specialized literacy coaches.
    
    > How did you choose which features of your chosen dataset to include or exclude from your visualization?
    Included Features: Board Name and the Average of Grade 3 Reading Achievement (%).
    Excluded Features: Individual school data, Math/Writing scores, and demographic data.
    Justification: The focus was placed on the Board level because averaging across the board mitigates the issues of data suppression that affected individual school records (as seen in Visualization 1's early attempts). Grade 3 Reading was chosen as a key, less-suppressed foundational literacy metric.
    
    > What ‘underwater labour’ contributed to your final data visualization product?
    Scaling Fix: The critical step was performing the necessary data standardization in Python, where the raw decimal percentage scores (e.g., 0.78) were multiplied by 100 to correctly represent them as percentages (e.g., 78%).Pivot Table Replacement: The main underwater labour was using Python (Pandas) to programmatically replicate and automate the manual work of an Excel PivotTable: calculating the AVERAGE of the achievement scores, sorting the results, and filtering to only the Top 10 boards.





- This assignment is intentionally open-ended - you are free to create static or dynamic data visualizations, maps, or whatever form of data visualization you think best communicates your information to your audience of choice! 
- Total word count should not exceed **(as a maximum) 1000 words** 
 
### Why am I doing this assignment?:  
- This ongoing assignment ensures active participation in the course, and assesses the learning outcomes: 
* Create and customize data visualizations from start to finish in Python
* Apply general design principles to create accessible and equitable data visualizations
* Use data visualization to tell a story  
- This would be a great project to include in your GitHub Portfolio – put in the effort to make it something worthy of showing prospective employers!

### Rubric:

| Component         | Scoring  | Requirement                                                                 |
|-------------------|----------|-----------------------------------------------------------------------------|
| Data Visualizations | Complete/Incomplete | - Data visualizations are distinct from each other<br>- Data visualizations are clearly identified<br>- Different sources/rationales (text with two images of data, if visualizations are labeled)<br>- High-quality visuals (high resolution and clear data)<br>- Data visualizations follow best practices of accessibility |
| Written Explanations | Complete/Incomplete | - All questions from assignment description are answered for each visualization<br>- Explanations are supported by course content or scholarly sources, where needed |
| Code              | Complete/Incomplete | - All code is included as an appendix with your final submissions<br>- Code is clearly commented and reproducible |

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 11/02/2025`
* The branch name for your repo should be: `assignment-3`
* What to submit for this assignment:
    * A folder/directory containing:
        * This file (assignment_3.md)
        * Two data visualizations 
        * Two markdown files for each both visualizations with their written descriptions.
        * Link to your dataset of choice.
        * Complete and commented code as an appendix (for your visualization made with Python, and for the other, if relevant) 
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/visualization/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-3`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
