
df.pivot(columns='grouping_variable_col', values='value_to_aggregate', index='grouping_variable_row')

df.pivot_table(values, index, aggfunc={'value_1': np.mean,'value_2': [min, max, np.mean]})

