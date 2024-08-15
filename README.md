# data-science 
# ASSIGNMENT-LAB INTRODUCTION


### ACTIVITY 1:

### 1. Write a Python program to select the 'name' and 'score' columns from the following DataFrame:

       Sample DataFrame:

              exam_data = {'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],

               'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],

              'attempts': [1, 3, 4, 3, 5, 3, 6, 1, 7, 1] } 

 # PROGRAM:
 ```
import pandas as pd
import numpy as np
exam_data = {'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
             'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
             'attempts': [1, 3, 4, 3, 5, 3, 6, 1, 7, 1]}

df = pd.DataFrame(exam_data)
selected_columns = df[['name', 'score']]

print(selected_columns)
```

# OUTPUT:
![output1](https://github.com/user-attachments/assets/af564a26-a4ce-4c52-9867-78ddc11cef4a)

### 2. For the above dataframe, Write a program to select the data who's attempt is greater than 3.

# PROGRAM:
```
import pandas as pd
import numpy as np
exam_data = {'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
             'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
             'attempts': [1, 3, 4, 3, 5, 3, 6, 1, 7, 1]}

df = pd.DataFrame(exam_data)
selected_data = df[df['attempts'] > 3]

print(selected_data)
```

# OUTPUT:
![output2](https://github.com/user-attachments/assets/b6e7eb08-7845-4fc7-9653-bfb442c37518)


### 3. Write python code for indexing rows and columns based on the following conditions:

Assume we have the following dataframe:

data = {'name': ['Alice', 'Bob', 'Charlie', 'Dave'],

        'age': [25, 35, 40, 28],

        'gender': ['F', 'M', 'M', 'M'],

        'salary': [50000, 70000, 60000, 80000]}

df = pd.DataFrame(data)

a. Select rows where age is greater than 30:

b. Select rows where name contains 'e':

c. Select rows where gender is 'M' and salary is greater than 65000:

d. Select columns 'name' and 'age'

# PROGRAM:
```
import pandas as pd

# Create a DataFrame
data = {'name': ['Alice', 'Bob', 'Charlie', 'Dave'],
        'age': [25, 35, 40, 28],
        'gender': ['F', 'M', 'M', 'M'],
        'salary': [50000, 70000, 60000, 80000]}

df = pd.DataFrame(data)

# a. Select rows where age is greater than 30
print("Rows where age is greater than 30:")
print(df[df['age'] > 30])

# b. Select rows where name contains 'e'
print("\nRows where name contains 'e':")
print(df[df['name'].str.contains('e')])

# c. Select rows where gender is 'M' and salary is greater than 65000
print("\nRows where gender is 'M' and salary is greater than 65000:")
print(df[(df['gender'] == 'M') & (df['salary'] > 65000)])

# d. Select columns 'name' and 'age'
print("\nColumns 'name' and 'age':")
print(df[['name', 'age']])
```
# OUTPUT:
![Output3](https://github.com/user-attachments/assets/a1de6846-fbf1-43e4-8c66-9c3799c17e3b)
