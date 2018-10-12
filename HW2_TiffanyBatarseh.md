# EE282

# Homework 2

Tiffany Batarseh

1. You are organizing your new bioinformatics project, create a directory with your project name and subdirectories within it called data and protocols. You realize you do need the protocols directory in a different directory called experiments in your home directory.

Answer: 
```
mkdir Project
cd Project
mkdir Data
mkdir Protocols
rmdir Protocols
cd ../
mkdir Experiments
cd Experiments
mkdir Protocols
```

2.  Let's explore the best methods to extract information from a matrix vs. a data frame. You have a data frame (mlbsubset loaded in previously) loaded into your R workspace. Create a small matrix in your workspace. Get the second column in the matrix. Now, get only the second column in the data frame, represented as a column. What happens if you try to get the second column out of the data frame with double brackets or with the same syntax/code as you did with the matrix? How would you get a single value from the matrix?

Answer:

```
> mymatrix
     [,1] [,2] [,3] [,4]
[1,]    1    4    7   10
[2,]    2    5    8   11
[3,]    3    6    9   12
> mymatrix[,2]
[1] 4 5 6
> mlbsubset[2]
  Team
1  BAL
2  BAL
3  BAL
4  BAL
5  BAL
6  BAL
# This extracts and keeps it as a column if it is a data frame
> mlbsubset[,2]
[1] BAL BAL BAL BAL BAL BAL
30 Levels: ANA ARZ ATL BAL BOS CHC CIN CLE COL CWS DET FLA HOU ... WAS
>mlbsubset[[2]]
[1] BAL BAL BAL BAL BAL BAL
30 Levels: ANA ARZ ATL BAL BOS CHC CIN CLE COL CWS DET FLA HOU ... WAS
# These methods extracts a vector representing the column unlike the single brackets that returns the column or multiple columns at once
> mymatrix[[2]]
[1] 2
#Double brackets in a matrix will extract a singular value out of the matrix in the position specified
```

3. You need to share a single file with a colleague. The file is in a directory that is in your home directory that we assume is already created. What permissions of your home directory, directory containing the file, and the file itself do you need to change in order to make the file readable to your colleague (he is not part of your group on your cluster)?

Answer:
```
chmod o+x /homedirectory
chmod o+x /homedirectory/directorywithfile
chmod o+r /homedirectory/directorywithfile/file
```


