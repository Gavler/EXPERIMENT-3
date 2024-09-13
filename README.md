# EXPERIMENT-3

Name: Ramirez, Gav Wrangler A.

Section: 2ECE-A

# PROBLEM 1:
Using knowledge obtained from the experiment and demonstrations:

# A. Load the corresponding .csv file into a data frame named cars using pandas.
> To use panda, we call out pandas as pd.

    import pandas as pd

> To use the file that was downloaded, we call out pd.read_csv('file name'), assign it to a variable, and print it.

    cars = pd.read_csv('cars.csv')
    cars
# OUTPUT
 
 >  ![image](https://github.com/user-attachments/assets/45b0cca3-9edf-4c4d-8ecc-9e38c96fd155)

# B. Display the first five and last five rows of the resulting cars.

> We call out .head to only read the first 5 rows of the Excel file. Then we print the output.

    x = cars.head()

    print('First Five rows of Cars: ')
    x
    
 > To read only the last 5 rows of the file, we use .tail() and call it out.

    y = cars.tail()

    print('Last Five rows of Cars: ')
    y
    
# OUTPUT
 First Five rows of Cars: 
> 
> ![image](https://github.com/user-attachments/assets/6dd3eadf-ee49-4dcd-a856-63d09b255a2d)


 Last Five rows of Cars: 
> 
> ![image](https://github.com/user-attachments/assets/f0104581-f5ed-4b57-8a66-77e7a643e82e)



# PROBLEM 2:
Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and
indexing operations:

# A. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars.
    import pandas as pd


> To read the file we use pd.read_csv() and assign the value.

    cars = pd.read_csv('cars.csv')
    cars

> To display the odd-numbered columns, we start at 1 with increments of 2 to include only those rows with odd indexes.

    c = cars[1::2]

> Then we display the first 5 odd numbered rows only and print the output.

    print('A. The first five rows with odd-numbered columns of cars.')
    c.head()

  # OUTPUT
 A. The first five rows with odd-numbered columns of cars.
> 
>  ![image](https://github.com/user-attachments/assets/3f9c6fac-a2c7-4f25-b495-9da60100ce3f)


# B. Display the row that contains the ‘Model’ of ‘Mazda RX4’.
> To display only the column of the 'model' of Mazda RX4, we use .loc[] to locate the index.

    a = cars.loc[cars['Model']=='Mazda RX4']

> Print the output.

     print('B. The row that contains the ‘Model’ of ‘Mazda RX4.')
     a
# OUTPUT

 B. The row that contains the ‘Model’ of ‘Mazda RX4.
> 
> ![image](https://github.com/user-attachments/assets/486592ce-5c43-4f8f-b0be-445d937cfc6d)


# C. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?

> To find the 'model' of Camaro Z28, we use .loc[], and we also specify what column should be displayed.

    y = cars.loc[cars['Model']=='Camaro Z28', ['Model', 'cyl']]

> Print the output.

    print('C.The number of cylinders(cyl) the Camaro Z28 have.')
    y

# OUTPUT
 C. The number of cylinders(cyl) the Camaro Z28 has.
> 
> ![image](https://github.com/user-attachments/assets/c6fcf149-49b5-4413-b9bf-d2c339fd4fa9)

# D. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.

> Find the location of of multiple 'Model' cars we use .isin([]) and only print the ['Model', 'cyl', 'gear'] of the column.

    g = cars.loc[cars['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']),   ['Model', 'cyl', 'gear']]

> Print the output.

    print('D. The number of cylinders(cyl) and gear type(gear) the Mazda RX4, Ford Pantera L, Honda Civic have.')
    g

# OUTPUT
 D. The number of cylinders(cyl) and gear type(gear) the Mazda RX4, Ford Pantera L, Honda Civic have.
>
> ![image](https://github.com/user-attachments/assets/1cf9b220-3f3b-456b-a6cf-148ef4f62734)



  

