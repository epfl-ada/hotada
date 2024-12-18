# ADA Template Website
## Usage
# Does the prevalence of a disease in a region drive the amount and focus of research conducted there?

## WHO database
Up intil now we have done an analysis of the BindingDB database. To carry out an analysis comparing reasearch and disease prevalence, we need data on the prevalence of the diseases researched in the BindingDB data. For this, we will use data from WHO. The data is available at the following link: https://ghoapi.azureedge.net/api/.

After checking the data, we found 8 diseases for which we have data in both databases. These are:
 - Plasmodium Falciparum
 - Human Immunodeficiency Virus
 - Poliovirus
 - Plasmodium vivax
 - Mycobacterium tuberculosis
 - Escherichia coli
 - Hepatitis C
 - Staphylococcus aureus

For each disease, data on the prevalence in different countries is available from WHO. The heatmap below shows the prevalences per capita of these diseases in different regions of the world in proportion to each other:

![alt text](diseases_per_region.png)

We can for example observe that many diseases are more prevalent in regions such as Africa and Eastern Mediterranean, as opposed to the Americas and Western Pacific.

## Prevalence-Research Analysis
Having data on quantity of research and disease prevalence in different countries, we can now analyze the relationship between the two. The question of how the prevalence of a disease in a region drives the amount and focus of research conducted there can be answered by comparing the two datasets.

For each disease, we depict below the prevalence of the given disease against the number of experiments conducted on it:

 - Add all 8 graphs showing prevalence vs research

From the graphs we observe that many countries with high prevalence of a disease do not necessarily have a high number of experiments conducted on it. On the other hand, countries with low prevalence of a disease can have a high number of experiments conducted on it. This makes sense, as many countries with high prevalence of a disease might not have the resources to conduct research on it, while countries with low prevalence might have the resources to conduct research on it.

To better quantify the relationship between prevalence and research, we perform a linear regression analysis on the data. We seek to find how well the prevalence of a disease in a region predicts the number of experiments conducted on it in that region. The results of the linear regression analysis are visualized in the following heatmap:

 - region-region ols heatmap

The numbers and colors shown can be best described as measures of the proportions of research conducted in a region given the proportions of a disease's prevalence in a region. Observing the diagonal, we can in effect observe that the relationship between prevalence and research is in general not very strong within regions. There are however, there are some relationships in between regions that appear to be stronger. For example, the realtionship between prevalence in Western Pacific and research in the Americas seems to be strongly positive. However, we cannot safely make any conclusions from this analysis, as none of the results are statistically significant.

What happens if we look at the relationship between the prevalence of a disease in a region and the number of experiments conducted on it in each individual country? The heatmap below shows the results of the linear regression analysis:

 - country-country ols heatmap

