
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

After running the program, you will get two get the following Stata Syntax:<br>
Syntax that defines the labels for each unique response option.<br>
Syntax that labels each labels each variable.<br>
<br>
<br>

*** DEFINING LABELS FOR EACH UNIQUE RESPONSE OPTIONS ***

*** DATA LABELING AND TABULATION***

* coursetype data label
label variable coursetype "Course type"
label values coursetype labelname2
asdoc tab coursetype , append

* pre_status data label
label variable pre_status "Pre-survey participation status"
label values pre_status labelname3
asdoc tab pre_status , append

* post_status data label
label variable post_status "Post-survey participation status"
label values post_status labelname3
asdoc tab post_status , append

* pre_ma3 data label
label variable pre_ma3 "I like class work best when it really makes me think"
label values pre_ma3 labelname4
asdoc tab pre_ma3 , append

* pre_pav6 data label
label variable pre_pav6 "One reason I would not participate in class is to avoid looking stupid"
label values pre_pav6 labelname4
asdoc tab pre_pav6 , append

* pre_ma5 data label
label variable pre_ma5 "An important reason I do my class work is because I enjoy it"
label values pre_ma5 labelname4
asdoc tab pre_ma5 , append

* pre_int data label
label variable pre_int "Are you an international student?"
label values pre_int labelname5
asdoc tab pre_int , append

* pre_eng data label
label variable pre_eng "Is English your native language"
label values pre_eng labelname5
asdoc tab pre_eng , append

* score data label
label variable score "How would you score this class on a scale of 1 to 10?"
label values score labelname6
asdoc tab score , append

* age data label
label variable age "What is your age?"
label values age labelname6
asdoc tab age , append

## Author

**Fernando Rodriguez** https://github.com/FernandoUCI
**Updated by Paulina Del Mundo Del Fierro

