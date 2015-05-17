# Introduction #

Translit is a fast, free and open source transliteration engine that ships with English, Sinhala and Tamil language support by default. Other languages maybe supported with corresponding language rules and dictionaries.

## Objective and Future Enhancements ##
The objective of this project is to build a very fast transliterator, that could be invoked as a Java library. Building a REST / SOAP based Web Service, a rules/dictionary update mechanism, and a Google Transliterator type of rich Ajax control for text fields are possible future enhancements.

## Uses a Dictionary lookup coupled with Phonetic Rules ##
The engine performs a dictionary lookup, and failing which, uses a phonetic rule based approach by default. Phonetic rules maybe added to support other languages, and existing rules maybe improved to increase accuracy of transliterations. However, the easiest way to improve accuracy is by updating the dictionaries.

## Core engine attempts to depend only on the JDK ##
This implementation attempts to be not-dependent on any external libraries - and hence debug and error logging are very limited and not based on SLF4J or Log4J etc. This is 'by choice'.

## Caching in memory and Heap memory usage ##
This implementation caches all words in memory, loaded from files found in the classpath. Hence an update of rules is possible by placing updated rules files on the classpath com/asankha/translit/resources followed by a restart. In future, this could be extended to reload via JMX, or a Web service call etc.

The implementation is optimized for performance, and hence uses RAM to keep rules and the dictionary cached. Thus the implementation will roughly take about 1.25MB of Heap Memory for English/Sinhala/Tamil transliteration. The size will vary for other languages or rules/dictionaries.

## Improving transliteration accuracy ##
The accuracy of the transliterator can be improved with updated dictionary files, or by tuning the phonetic rules used. The former is strongly encouraged. For example, the name of the town "Galle" cannot be correctly transliterated by only using phonetic rules, as its name in Sinhalese is different from the sound made by the word "Galle" in English.

The accuracy is generally better for person names etc. However, the Male/Female or Unknown
specifier must be specified to obtain a correct translation where application.

**e.g. Avanka - as a male "අවන්ක" or as a female "අවන්කා"**

## Standalone command-line execution ##

**Sample execution of the command line application**

$java -jar translit-core-1.0.0.jar
asankha perera
අසන්ඛ පෙරේරා

**Transliterating an input file /tmp/input into /tmp/output using default options**

$java -jar translit-core-1.0.0.jar < /tmp/input > /tmp/output