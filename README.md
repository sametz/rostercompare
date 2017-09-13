# rostercompare

## A Jupyter python notebook to compare two Canvas grade rosters and detect changes in registration.

The notebook assumes that two .csv grade rosters are present in the same folder, in the same format as that produced by a Canvas gradebook export. The old_roster_filename and new_roster_filename are edited to the names of the older and newer .csv roster, respectively, and then all cells are run. The notebook will output any adds, drops and switches between sections.

Different institutions may have different default formats, so some editing may be required. At my institution, the order of columns in the .csv roster are:

- student name
- three columns of different ID numbers (the script uses the last of these, 'SIS Login ID', to match students between rosters)
- the class section
- lots of other columns (that are stripped, so that peeking at the dataframe.head() is cleaner)

# Dependencies

- numpy
- pandas
