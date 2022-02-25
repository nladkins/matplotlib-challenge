# Matplotlib Homework - The Power of Plots

## Background

The purpose of this code is to run an analysis of hypothetical drug studies on mice for the hypothetical company Pymaceuticals Inc. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens.  The code included here performs an analysis of study data as well as metadata on the mice.  The example provided here is a screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

## Tasks

The following tasks were performed:

  1. Data Cleansing:  Drop Null values, check data for any mouse ID with duplicate time points and remove data associated with that mouse ID.
  2. Generate a summary statistics table consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen.

  Result:

    The mean tumor volume of all mice is: 50.448411
    The median tumor volume of all mice is: 48.951421
    The variance of the tumor volume for all mice is from 22.050126 to 78.567014
    The standard deviation of all mice tumors: 8.904752
    The standard error of all mice tumors: 0.204937

  3. Generate a bar plot using both Pandas's `DataFrame.plot()` and Matplotlib's `pyplot` that shows the total number of timepoints for all mice tested for each drug regimen throughout the course of the study.

  Result:

  ![Number of Timepoints per Drug](https://github.com/nladkins/matplotlib-challenge/blob/master/figs/timepointsperdrug.png?raw=true)

  4. Generate a pie plot using both Pandas's `DataFrame.plot()` and Matplotlib's `pyplot` that shows the distribution of female or male mice in the study.

  Result:

  ![Distribution of Female and Male Mice per Study](https://github.com/nladkins/matplotlib-challenge/blob/master/figs/sex_distribution.png?raw=true)

  5. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Calculate the quartiles and IQR and quantitatively determine if there are any potential outliers across all four treatment regimens.
  
  Result:

    The lower quartile of Capomulin in tumor values is 45.00
    The upper quartile of Capomulin in tumor values is 56.32
    The interquartile range of Capomulin in tumor values is 11.32
    Values below 28.01 are Capomulin outliers.
    Values above 73.31 are Capomulin outliers.
    --------------------------------------------------------------
    The lower quartile of Ramicane in tumor values is 45.00
    The upper quartile of Ramicane in tumor values is 56.32
    The interquartile range of Ramicane in tumor values is 11.32
    Values below 28.01 are Ramicane outliers.
    Values above 73.31 are Ramicane outliers.
    --------------------------------------------------------------
    The lower quartile of Infubinol in tumor values is 45.00
    The upper quartile of Infubinol in tumor values is 56.32
    The interquartile range of Infubinol in tumor values is 11.32
    Values below 28.01 are Infubinol outliers.
    Values above 73.31 are Infubinol outliers.
    --------------------------------------------------------------
    The lower quartile of Ceftamin in tumor values is 45.00
    The upper quartile of Ceftamin in tumor values is 56.32
    The interquartile range of Ceftamin in tumor values is 11.32
    Values below 28.01 are Ceftamin outliers.
    Values above 73.31 are Ceftamin outliers.
    -------------------------------------------------------------

  6. Using Matplotlib, generate a box and whisker plot of the final tumor volume for all four treatment regimens and highlight any potential outliers in the plot by changing their color and style.

  Result:

  ![Box and Whisker plot of the Final Tumor Volume for all Four Treatment Regimens](https://github.com/nladkins/matplotlib-challenge/blob/master/figs/tumorvolume_by_drug.png?raw=true)


  7. Select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.

  Result:

  ![Mouse ID s185 Tumor Volume and Timepoint](https://github.com/nladkins/matplotlib-challenge/blob/master/figs/timepointsperdrug_1mouse.png?raw=true)

  8. Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.
  9. Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. Plot the linear regression model on top of the previous scatter plot.

  Result:

  ![Correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment](https://github.com/nladkins/matplotlib-challenge/blob/master/figs/capomulin_linear_regression.png?raw=true)


  10. Look across all previously generated figures and tables and write at least three observations or inferences that can be made from the data. Include these observations at the top of notebook.

## Observations (also included at the top of the code)

### 1) For the drugs Capomulin and Ramicane "appear" to be the most effective treatments as the tumor volume and metastic sites were the lowest, even under longer timepoints.

### 2) However, the drugs Capomulin and Ramicane had the lightest average weights for their mice which seems to play a significant role in the tumor volume and how that could be interepreted.

### 3) Aside from the mice weight skewing the Capomulin and Ramicane results, there was a good balance on the count of timepoints for each drug tested as well as a good balance in the number of male mice and female mice that were used in the study.