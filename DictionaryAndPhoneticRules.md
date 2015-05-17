The dictionaries and phonetic rules are loaded from the classpath com/asankha/translit/resources

# Dictionaries #

**en-to-si.txt - English to Sinhala dictionary** en-to-ta.txt - English to Tamil dictionary
**si-to-ta.txt - Sinhala to Tamil dictionary**

## File format ##
The dictionary files are CSV files with each word specified on a new line. The first field specifies the word in the source language, the second field specifies the word in the target language. The third is '1' if the word specifies a gender based word in the source language, and the fourth is '1' if the target word specifies a gender based word in the target language

e.g.
Anjalika,අංජලිකා,1,1
Other,අනෙක්,0,0