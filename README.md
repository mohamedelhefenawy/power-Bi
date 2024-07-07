# Pizza Sales Analysis

## Overview

### Total Sales and Quantity

- `Total Quantity: 49,574 units`
- `Total Price: 249.38K (30.49%)`
- `Cost: 817.86K`

### Pizza Sizes Distribution

- `L (Large): Most common size`
- `M (Medium)`
- `S (Small)`
- `XL (Extra Large)`
- `XXL (Extra Extra Large)`

### Sales by Day of the Week

- `Friday: Highest sales`
- `Thursday`
- `Saturday`
- `Wednesday`
- `Tuesday`
- `Monday`
- `Sunday: Lowest sales`

### Ingredients Usage

- `Garlic: Most used ingredient`
- `Tomatoes`
- `Red Onions`
- `Red Peppers`
- `Mozzarella`
- `Pepperoni`
- `Spinach`
- `Mushrooms`
- `Chicken`
- `Capocollo`

## For Extracting the ingredients we use 
- #### pandas
- #### collector
```bash
import pandas as pd
from collections import Counter
```
### 1- Split and Flatten the Ingredients List
Split each ingredient string by commas and flatten the list.
```bash
ingredient = [x.strip() for y in data['pizza_ingredients'].str.split(',') for x in y]
```
### 2- Count Ingredient Frequencies
Use Counter from the collections module to count the occurrences of each ingredient.
```bash
count_ingredient = Counter(ingredient)
```
### 3- Create a DataFrame of Counts
Convert the counts to a DataFrame.
```bash
df=  pd.DataFrame(count_ingredient.items(),columns=['ingredient','count'])
```
### 4- Sort the Counts in Descending Order
Sort the DataFrame by the count column in descending order.
```bash
df = df.sort_values(['count'],ascending=False).reset_index(drop=True)
```

### Sales by Month

- `July: Highest sales`
- `May`
- `March`
- `November`
- `January`
- `April`
- `August`
- `June`
- `February`
- `December`
- `September`
- `October`
