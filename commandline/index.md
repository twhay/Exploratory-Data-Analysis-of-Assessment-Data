# The Unix/Linux/MacOS Terminal

All users of all skill levels are able to use the terminal in order to inspect and clean data that is in Comma Separated Values (csv) format. 
**Note** The instructions here will not apply to a windows machine unless [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install) has been properly installed and configured. For instructions on how to do the same functions using Windows Cmd and Windows PowerShell, please view that section.
For this tutorial, we are using the [Public School Characteristics 2020-21](https://catalog.data.gov/dataset/public-school-characteristics-2020-21) from the National Center of Education Statistics via Data.gov. 
[This link](https://data-nces.opendata.arcgis.com/datasets/nces::public-school-characteristics-2020-21.csv?outSR=%7B%22latestWkid%22%3A4326%2C%22wkid%22%3A4326%7D) should download the csv to your machine.
For this example, we want to see the first two rows of data within the CSV. In order to do this, we will type the command ```head -n 2 Public_School_Characteristics_202-21.csv```
This will display the first two rows of the CSV, which will look like below:
```X,Y,OBJECTID,NCESSCH,SURVYEAR,STABR,LEAID,ST_LEAID,LEA_NAME,SCH_NAME,LSTREET1,LSTREET2,LCITY,LSTATE,LZIP,LZIP4,PHONE,GSLO,GSHI,VIRTUAL,TOTFRL,FRELCH,REDLCH,PK,KG,G01,G02,G03,G04,G05,G06,G07,G08,G09,G10,G11,G12,G13,TOTAL,MEMBER,AM,HI,BL,WH,HP,TR,FTE,LATCOD,LONCOD,ULOCALE,NMCNTY,STUTERATIO,TITLEI,STITLEI,AMALM,AMALF,ASALM,ASALF,HIALM,HIALF,BLALM,BLALF,WHALM,WHALF,HPALM,HPALF,TRALM,TRALF,TOTMENROL,TOTFENROL,STATUS,UG,AE,SCHOOL_TYPE_TEXT,SY_STATUS_TEXT,SCHOOL_LEVEL,AS,CHARTER_TEXT,MAGNET_TEXT```

```-86.2062,34.2602000000001,1,010000500870,2020-2021,AL,0100005,AL-101,Albertville City,Albertville Middle School,600 E Alabama Ave,,Albertville,AL,35950,    ,(256)878-2341,07,08,Not Virtual,332,332,0,,,,,,,,,469,439,,,,,,908,908,2,469,33,371,0,29,42,34.2602,-86.2062,32-Town: Distant,Marshall County,21.62,1-Yes,1-Yes,1,1,0,4,239,230,18,15,187,184,0,0,19,10,,,1,,,Regular school,Currently operational ,Middle,4,No,No```

We can immediately see that the first row is the headers of the data set.