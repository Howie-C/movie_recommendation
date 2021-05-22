# UTS_42903_Assignment_3
UTS - 42903 - Social and Information Analysis
This is the programming part of the assignment 3.

## Author
Yihao Chen

## Project Dataset
MovieLens dataset will be provided for this project.
For more details or downloading, please refer to: [MovieLens](https://grouplens.org/datasets/movielens/)

## Files Overview:
Please use Python 3 to excecute the programs.

### movie_recommend.py
This is the program that builds predicting model by implementing the cosine similarity algorithms to estimate the ratings.  
Make sure souce datafile 'ratings.csv' is exisiting as input.

### movie_visual.py
This is the program that visualize the datafile, giving pie and bar charts as visualization results.  
Make sure souce datafile 'movies.csv' is existing as input.

## How to run the program?

### Run movie_recommend.py
Open file movie_recommend.py.  
Change the variables 'top_N' and 'k' (cosine similarity) values in row 321 and row 329 respectively.  
Execute the Python3 script.  

```python

def task():

	# Filter top 500 movies by rating frequency, generate a new file for further modelling
	find_top_N(500)           # Row 321

	create_rating_table()

	randomize_and_split()

	target_movie = select_and_filter_out_invalid_users_on_target_prediction_movie()

	k = 10                    # Row 329

	generate_results(target_movie, k)

	get_accuracy()

if __name__ == '__main__':

	task()
```

### Run movie_visual.py
Open file movie_visuald.py.  
Change the variables 'top_num' (number of top nth most frequent) value in row 162.  
Execute the Python3 script.  

```python
def main():

	top_num = 10              # Row 162

	year_distribution_pie(top_num)

	year_distribution_bar(top_num)

	genres_distribution_pie(top_num)

if __name__ == '__main__':

	main()
```

## Imported External Libraries
All the modelues imported and the coresponding format is listed as below.
```python
import pandas as pd
import numpy
import math
from tqdm import tqdm
import itertools
from itertools import groupby
import matplotlib.pyplot as plt
```


## Installation
For Windows:  
Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the external libriaires listed above.

```bash
pip install pandas
pip install numpy
pip install python-math
pip install tqdm
pip install itertools-s
pip install matplotlib
```
