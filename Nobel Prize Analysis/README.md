![image](https://user-images.githubusercontent.com/83639803/222931471-2786cd70-32d0-4135-bd30-c85b74f2707c.png)


# Used Technologies

- Google Colab
- Jupyter Notebook
- Python 
- Seaborn
- Matplotlip 
- Pandas
- Plotly



# Used and Learned:


- Reading Pandas Documentation and gained experience in know-how

- Create a Choropleth to display data on a map.

- Create bar charts showing different segments of the data with plotly.

- Create Sunburst charts with plotly.

- Use Seaborn's .lmplot() and show best-fit lines across multiple categories using the row, hue, and lowess parameters.

- Understand how a different picture emerges when looking at the same data in different ways (e.g., box plots vs a time series analysis).

- See the distribution of our data and visualise descriptive statistics with the help of a histogram in Seaborn.




## Roadmap 

- Write rough algorithm for project idea on paper.

- Read Data Analysis Libraries Documentation and decide proper ones with Chart Models.

- Decide topics of the dataset and collect data properly

- Execute Algorithm.

- Finish Project.
  


  
## Usage Examples

```python
cat_country = df_data.groupby(['birth_country_current', 'category'], 
                               as_index=False).agg({'prize': pd.Series.count})
cat_country.sort_values(by='prize', ascending=False, inplace=True)
cat_country

merged_df = pd.merge(cat_country, top20_countries, on='birth_country_current')
# change column names
merged_df.columns = ['birth_country_current', 'category', 'cat_prize', 'total_prize'] 
merged_df.sort_values(by='total_prize', inplace=True)
merged_df

cat_cntry_bar = px.bar(x=merged_df.cat_prize,
                       y=merged_df.birth_country_current,
                       color=merged_df.category,
                       orientation='h',
                       title='Top 20 Countries by Number of Prizes and Category')

cat_cntry_bar.update_layout(xaxis_title='Number of Prizes', 
                            yaxis_title='Country')
cat_cntry_bar.show()

}
```

  
