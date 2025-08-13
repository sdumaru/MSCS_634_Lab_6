# Lab 6: Association Rule Mining with Apriori and FP-Growth
**Course:** MSCS 634-B01: Advanced Big Data and Data Mining  

## Purpose of the Lab  
The goal of this lab was to learn how to use Apriori and FP-Growth algorithms to find association rules in a dataset. I worked with a retail transaction dataset, cleaned it, and prepared it for mining. Then, I found frequent itemsets and made association rules. I also used graphs to help understand the results and compared both algorithms.

## Dataset  
I used the **Online Retail Dataset** from the UCI Machine Learning Repository. It has transactions from a UK-based online store. The data includes invoice numbers, product names, quantities, and other details.

## Steps I Did  
1. **Data Preparation**  
   - Loaded the dataset into Python.  
   - Removed cancelled orders and negative quantities.  
   - Changed product names to lowercase for consistency.  
   - Turned the data into a one-hot encoded basket format.  
   - Made a bar plot of the most sold items and a heatmap of items bought together.  

2. **Apriori Algorithm**  
   - Ran Apriori with a set minimum support value.  
   - Found frequent itemsets and showed the top ones in a bar plot.  

3. **FP-Growth Algorithm**  
   - Ran FP-Growth with the same support value as Apriori.  
   - Showed the top frequent itemsets in a bar plot.  

4. **Association Rules**  
   - Created rules from the itemsets found by both algorithms.  
   - Calculated support, confidence, and lift for the rules.  
   - Made a scatter plot to compare confidence and lift.  

5. **Comparison**  
   - Compared the runtime and number of itemsets and rules for both algorithms.  
   - Found that Apriori was faster than FP-Growth for this dataset.  

## Key Findings  
- Some products like decoration items and kitchen items were often bought together.  
- High lift and confidence rules showed strong relations between products.  
- Apriori was faster for this dataset, but usually FP-Growth can be faster on bigger datasets.  

## Challenges  
- The heatmap for all products was too big to read, so I used only the top 20 items.  
- Choosing good `min_support` and `min_confidence` values took a few tries.  
- FP-Growth took more time than Apriori here, which was not what I expected.  
