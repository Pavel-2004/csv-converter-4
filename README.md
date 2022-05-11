CSV FILTERING
This easy to implement project allows trade files from different banks to be rearranged into the proper format that it needs to be in.

The goal was to make everything very maintainable and modifiable.

The way that this project works is that every time a user uploads a csv file of their trades, it will convert to a standard format
based on what is selected.


It follows the following steps:
1) It initializes the function based on what type is selected
2) It then converts all the data from the csv into an array
3) Next it checks for errors in the errorCase function. There is an if statement for every type which can have a unique error checking statement
in each. It can either return false or continue based on if the data is valid
4) Then it runs a filtering function for every specific broker in order to manipulate the data and put it into the correct format 
5) It then maps everything into the proper format and downloads it the user
6) For this repository please disregard any options or searching functions. This repository only takes care of mapping the data. 

Adding a new broker
1) Go into init.js and add the broker to the options variable. 
2) Go to the initAll function in submit.js and add a new type with the new broker name. Follow the same pattern.
3) Inside of the errorCase function add an if statement with any custom function that checks if the format of the file is correct. Return false if it the 
format is not correct and return the corresponding filtering function if it is correct.
4) Create a filtering function that filters and manipulates the data by looking at each row not including the header or any of the other rows.
5) Add the mapToProperFormat function and specify how you want to map out this file based on indexes. Each index is of the original row and make it correspond to the final index in the proper format




I hope that this makes sense, I suggest taking a look at the repository with the searching functionality https://github.com/Pavel-2004/csv-converter-5
Please feel free to reach out to me with any questions, concerns, or criticism at halkopavel@gmail.com. 


LOGS
Version 0 - 4/11/22 - Built layout of everything
- built layout
- only one original layout works which is the questrade original layout

Version 0.1 - 4/13/22 - Added RBC AND TD
- Fixed naming of the files 
- Added a selector option into initializing 
- Added RBC and TD filtering system

Version 0.2 - 4/14/22 - Fixes 
- Fixed column names
- Fixed security codes
- prices made more accurate
- TD account number fix
- questrade unit# is now positive
- last row in questrade fixed to appearing as CAD

Version 0.3 - 4/12/28 - further addition of banks and minor fixes
- Currently there is extra search functions which for this repository should be disregarded as this takes care of only mapping the data
- Added 4 other brokers
- Fixed bug that didn't allow files with commas in the field to work properly because of delimiter issues.
- Updated filtering functions that worked around commas to not have to work around them as those commas are now kept inside of the field.


