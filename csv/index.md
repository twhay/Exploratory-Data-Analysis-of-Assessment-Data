# Comma Separated Values (CSVs)

1. [Preamble](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#preamble)
2. [Data Set](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#data-set)
3. [The Unix/Linux/MacOS Terminal](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#the-unixlinuxmacos-terminal)
4. [Excel](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#excel)
5. [Google Sheets](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#excel)
6. [R](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#r)
7. [Python](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#python)
8. [Tableau](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#tableau)
9. [PowerBI](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#powerbi)
10. [Relational Databases](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/index.md#relational-databases)

## Preamble

A comma separate value is a file format in which the values are separated by a comma. Due to many data requiring the use of commas, there are formats which allow for a comma to be used as part of the file format like using a semi-colon ; instead or using a tab separated file (TSV). This section will address all of these, though we will work with the below data set.

## Data Set

For this tutorial, we are using the [Public School Characteristics 2020-21](https://catalog.data.gov/dataset/public-school-characteristics-2020-21) from the National Center of Education Statistics via Data.gov. [This link](https://data-nces.opendata.arcgis.com/datasets/nces::public-school-characteristics-2020-21.csv?outSR=%7B%22latestWkid%22%3A4326%2C%22wkid%22%3A4326%7D) should download the csv to your machine. Note where the downloaded file went on your machine, as you will need to know the file path of the CSV in order to successfully import it.

## The Unix/Linux/MacOS Terminal

**Note** The instructions here will not apply to a windows machine unless [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install) has been properly installed and configured. For instructions on how to do the same functions using Windows Cmd and Windows PowerShell, please view that section.


All users of all skill levels are able to use the terminal in order to inspect and prepare data that is in Comma Separated Values (csv) format. We would use the terminal in situations where we havea CSV that we want to inspect quickly before deciding our next steps for data cleaning. Using the terminal allows us to better choose the tools that we would like to use for further data wrangling. If I have a CSV, I like to start with the terminal before 

For this example, we want to see the first two rows of data within the CSV. In order to do this, we will type the command ```head -n 2 Public_School_Characteristics_202-21.csv```. **Important** In order for this command to work, we have to navigate to the folder which contains the CSV. Depending on how your downloads are configured, this means navigating to the folder where the CSV was downloaded.  As an example, we change directory to Downloads run the command:

```cd Downloads```
``` head -n 2 Public_School_Characteristics_202-21.csv```

This will display the first two rows of the CSV, which will look like below:
```X,Y,OBJECTID,NCESSCH,SURVYEAR,STABR,LEAID,ST_LEAID,LEA_NAME,SCH_NAME,LSTREET1,LSTREET2,LCITY,LSTATE,LZIP,LZIP4,PHONE,GSLO,GSHI,VIRTUAL,TOTFRL,FRELCH,REDLCH,PK,KG,G01,G02,G03,G04,G05,G06,G07,G08,G09,G10,G11,G12,G13,TOTAL,MEMBER,AM,HI,BL,WH,HP,TR,FTE,LATCOD,LONCOD,ULOCALE,NMCNTY,STUTERATIO,TITLEI,STITLEI,AMALM,AMALF,ASALM,ASALF,HIALM,HIALF,BLALM,BLALF,WHALM,WHALF,HPALM,HPALF,TRALM,TRALF,TOTMENROL,TOTFENROL,STATUS,UG,AE,SCHOOL_TYPE_TEXT,SY_STATUS_TEXT,SCHOOL_LEVEL,AS,CHARTER_TEXT,MAGNET_TEXT```

```-86.2062,34.2602000000001,1,010000500870,2020-2021,AL,0100005,AL-101,Albertville City,Albertville Middle School,600 E Alabama Ave,,Albertville,AL,35950,    ,(256)878-2341,07,08,Not Virtual,332,332,0,,,,,,,,,469,439,,,,,,908,908,2,469,33,371,0,29,42,34.2602,-86.2062,32-Town: Distant,Marshall County,21.62,1-Yes,1-Yes,1,1,0,4,239,230,18,15,187,184,0,0,19,10,,,1,,,Regular school,Currently operational ,Middle,4,No,No```

We can immediately see that the first row is the headers of the data set, and the second row is a mix of data types, and there are some missing values as well.

We can see the last rows in the CSV by using the command ```tail```.

The following command will let us see the final row of the CSV.

```tail -n 1 Public_School_Characteristics_2020-21.csv```

The row will look like this:

```-64.8903109999999,18.31823,101662,780003000034,2020-2021,VI,7800030,VI-001,Saint Thomas - Saint John School District,BERTHA BOSCHULTE JUNIOR HIGH,9 1 and 12A BOVONI,,Saint Thomas,VI,00802,    ,(340)775-4222,06,08,Full Virtual,574,574,0,,,,,,,,190,191,196,,,,,,577,577,,55,516,2,,,47,18.31823,-64.890311,33-Town: Remote,St. Thomas Island,12.28,1-Yes,1-Yes,,,4,,25,30,269,247,1,1,,,,,,,1,,,Regular school,Currently operational ,Middle,4,N,No```

## Excel

## Google Sheets

Importing a CSV into Google Sheets relies upon Google's built-in tooling to conver the CSV to a Google Sheet.

1. Download the CSV locally to your computer
2. Go to sheets.google.com and login into your google account
3. Create new spreadsheet
4. In that spreadsheet go to File -> Import ![alt text](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/images/google-sheets-file-menu-import.png "Google Sheets File Menu clicking on the Import menu" )

5. Go to the upload tab and either find the CSV on your computer or drag and drop it from a file explorer ![alt text](https://github.com/twhay/data-wrangling-toolkit/blob/master/csv/images/google-sheets-import-upload.png "Google Sheets Import Upload browser" )
6. Choose the location to save the CSV as a spreadsheet and the separator type
7. Refresh the page once the upload is complete and find your uploaded CSV as a Google Sheet

Advantages: Google Workspace stores your CSV and any associated history (version control)

Disadvantages: You are at the mercy of Google's cell limits for imported into Google Drive, which as of late March 2023 were " [Up to 10 million cells or 18,278 columns for spreadsheets imported from Microsoft Excel. The limits are the same for Excel and CSV imports.](https://support.google.com/drive/answer/37603)

## R

Using the same file, we are going to use R to read in the CSV, and see what kind of data we are working with. This section assumes you have some familiarity with R, and already have it installed on your machine.

### tidyverse

The R package tidyverse is the first recommended way to do this, as it is an incredible versatile package for data importing and data wrangling. First, we need to install and load the package.

```install.packages("tidyverse")```
```library(tidyverse)```

**Note: It is common to get errors like 
```Error: package or namespace load failed for ‘tidyverse’ in loadNamespace(i, c(lib.loc, .libPaths()), versionCheck = vI[[i]]): namespace ‘rlang’ 0.3.0.1 is already loaded, but >= 0.3.1 is required```
when loading a library for the first time. Copying and pasting the error into Google or Stack Overflow will typically give a quick solution - for example, [here](https://stackoverflow.com/questions/55415631/error-package-or-namespace-load-failed-for-tidyverse-in-loadnamespace) is the Stack Overflow post to solve this issue**

Once tidyverse is loaded into our R terminal, we can use [read_csv()](https://readr.tidyverse.org/reference/read_delim.html) to pull our data into a tibble. We can do this using the URL of the CSV directly in this instance.

```r
schools <- read_csv("https://data-nces.opendata.arcgis.com/datasets/nces::public-school-characteristics-2020-21.csv?outSR=%7B%22latestWkid%22%3A4326%2C%22wkid%22%3A4326%7D")
```

This gives us the following output:

```r
Rows: 100722 Columns: 79
── Column specification ─────────────────────────────────────────────────────────────────────────────────
Delimiter: ","
chr (26): NCESSCH, SURVYEAR, STABR, LEAID, ST_LEAID, LEA_NAME, SCH_NAME, LST...
dbl (51): X, Y, OBJECTID, TOTFRL, FRELCH, REDLCH, PK, KG, G01, G02, G03, G04...
lgl  (2): TOTMENROL, TOTFENROL

ℹ Use `spec()` to retrieve the full column specification for this data.
ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
```

## Python

Now let's do this again but with Python. This section assumes you have some familiarity with Python, and already have it installed on your machine.

### pandas 

## Tableau
## Looker
## PowerBI
## Relational Databases