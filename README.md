# Analysis of immunization from the CDC
For this project we'll be looking at 2017 data on immunizations from the CDC. 

## Step 1
We calculate the proportion of children in the dataset who had a mother with the education levels equal to less than high school (<12), high school (12), more than high school but not a college graduate (>12) and college degree.

## Step 2
Let's explore the relationship between being fed breastmilk as a child and getting a seasonal influenza vaccine from a healthcare provider. We calculate the average number of influenza vaccines for those children we know received breastmilk as a child and those who know did not.

## Step 3
It would be interesting to see if there is any evidence of a link between vaccine effectiveness and sex of the child. We calculate the ratio of the number of children who contracted chickenpox but were vaccinated against it (at least one varicella dose) versus those who were vaccinated but did not contract chicken pox.

## Step 4
A correlation is a statistical relationship between two variables. If we wanted to know if vaccines work, we might look at the correlation between the use of the vaccine and whether it results in prevention of the infection or disease . In this step, we see if there is a correlation between having had the chicken pox and the number of chickenpox vaccine doses given (varicella).

###### 
Some notes on interpreting the answer. If the `had_chickenpox_column` is either `1` (for yes) or `2` for no, and that the `num_chickenpox_vaccine_column` is the number of doses a child has been given of the varicella vaccine, then a positive correlation (e.g. `corr > 0`) would mean that an increase in `had_chickenpox_column` (which means more no) would mean an increase in the `num_chickenpox_vaccine_column` (which means more doses of vaccine). If `corr < 0` then there is a negative correlation, indicating that having had chickenpox is related to an increase in the number of vaccine doses. Also, `pval` refers to the probability the relationship observed is significant. In this case `pval` is very very small (will end in `e-18` indicating a very small number), which means the result unlikely to be by chance.

This is not really the full picture, since we are not looking at when the dose was given. It is possible that children had chickenpox and then their parents went to get them the vaccine.
