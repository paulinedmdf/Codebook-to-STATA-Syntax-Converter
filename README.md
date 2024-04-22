
# Codebook to Stata Syntax Converter

This converter takes your typical csv-based codebook and converts the information into data labeling syntax for Stata. 

It is important that the first three columns of your codebook are labeled and formatted the same way as the <b>codebook_file.csv</b>

Here's how this csv file looks when opened:

![alt text](https://github.com/FernandoUCI/Codebook-to-STATA-Syntax-Converter/blob/master/codebook_screenshot.png)

Notice that all you need are three pieces of information:

<b>Variable</b> contains the variable name

<b>Item</b> contains the question item

<b>Response Options</b> contains the response options for each question item.

Use the <b>CodebookConverter.py</b> to run the converter. Details about the structure of the code can be found in the <b>CodebookConverter.ipynb</b> notebook.

After running the program, you will get the following Stata Syntax:<br>
Syntax that defines the labels for each unique response option, numbering them by their unique instance. <br>
Syntax that labels each variable.<br>
<br>
<br>

***DEFINING LABELS FOR EACH UNIQUE RESPONSE OPTION***

label define labelname2 1 "Online" 0 "Face-to-face"

label define labelname3 1 "Participated" 0 "Did not participate"

label define labelname4 1 "Not at all true" 2 "Not true" 3 "Somewhat true" 4 "True" 5 "Very true"

label define labelname5 1 "Yes"  0 "No"

label define labelname6 "None"

*** DATA LABELING AND TABULATION***

** coursetype data label
label variable coursetype "Course type"
label values coursetype labelname2
tab coursetype

** pre_status data label
label variable pre_status "Pre-survey participation status"
label values pre_status labelname3
tab pre_status

** post_status data label
label variable post_status "Post-survey participation status"
label values post_status labelname3
tab post_status

** pre_ma3 data label
label variable pre_ma3 "I like class work best when it really makes me think"
label values pre_ma3 labelname4
tab pre_ma3

** pre_pav6 data label
label variable pre_pav6 "One reason I would not participate in class is to avoid looking stupid"
label values pre_pav6 labelname4
tab pre_pav6

** pre_ma5 data label
label variable pre_ma5 "An important reason I do my class work is because I enjoy it"
label values pre_ma5 labelname4
tab pre_ma5

** pre_int data label
label variable pre_int "Are you an international student?"
label values pre_int labelname5
tab pre_int

** pre_eng data label
label variable pre_eng "Is English your native language"
label values pre_eng labelname5
tab pre_eng

** score data label
label variable score "How would you score this class on a scale of 1 to 10?"
label values score labelname6
tab score

** age data label
label variable age "What is your age?"
label values age labelname6
tab age

## Author

**Fernando Rodriguez** https://github.com/FernandoUCI
**Updated by Paulina Del Mundo Del Fierro

