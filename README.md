# MDS_ACO
This project is implemented by Asma Bader Al-Saleh. It creates a multi-document summarizer that generates MDS summaries by maximizing the overall content scores using an ACS algorithm.  It summarizes the given corpus's docsets (the 2011 MultiLing Pilot - English and Arabic languages) and follows the compitition's rules.


External sources: (others not mentioned below were all coded by me)
- Stanford CoreNLP version 3.9.1 library (downloaded from https://stanfordnlp.github.io/CoreNLP/).
- Porter Stemming Algorithm [in Stemmer class] (downloaded from https://tartarus.org/martin/PorterStemmer/).
- Khoja�s stemmer (http://zeus.cs.pacificu.edu/shereen/research.htm)
- calculate_LCS function in Utility class (the code is from http://rosettacode.org/wiki/Longest_common_subsequence#Dynamic_Programming_2).
- An English stop word list from the SMART information retrieval system is used (http://jmlr.csail.mit.edu/papers/volume5/lewis04a/a11-smart-stop-list/english.stop).
- An Arabic stop word list provided in (Ibrahim Abu El-Khair. 2006. Effects of stop words elimination for arabic information retrieval: A comparative study. International Journal of Computing & Information Sciences, 4(3):119 � 133.)
	

Inputs: the corpus 
1: for the English language version of the 2011 MultiLing Pilot 
or
2: for the Arabic language version of the 2011 MultiLing Pilot. 


Outputs:
The output is the summaries of the corpus's docsets (one sentence per line). Summaries are generated in 'output' folder.


 
To run the code, please follow these main steps (summaries will be found in 'output' folder.):
1) Download the corpus content (docsets) and save it in its folder; "Multiling_2011" for English version and "Multiling_2011_Arabic" for Arabic version. Remove the Readme file in thses two folders.

2) Download the CoreNLP jar files and save them into 'MDS_lib' folder (CoreNLP 3.9.1, model jar version 3.9.1 for English, model jar version 3.9.1 for English(KBP, model jar version 3.9.1  for Arabic) and delete the Readme file in this folder. Namely, these library are: ejml-0.23.jar, javax.json.jar, javax.json-api-1.0-sources.jar, joda-time.jar, joda-time-2.9-sources.jar, jollyday.jar, jollyday-0.4.9-sources.jar, protobuf.jar, slf4j-api.jar, slf4j-simple.jar, stanford-arabic-corenlp-2018-02-27-models.jar, stanford-corenlp-3.9.1.jar, stanford-corenlp-3.9.1-javadoc.jar, stanford-corenlp-3.9.1-models.jar, stanford-corenlp-3.9.1-sources.jar, stanford-english-corenlp-2018-02-27-models.jar, stanford-english-kbp-corenlp-2018-02-27-models.jar, xom.jar, and xom-1.2.10-src.jar.

3) Create two folders under "output" folder and name them: "output_multiling2011" and "output_multiling2011_Arabic".

4) Excute the program, write the following command in the Command Prompt window: 

java -Dfile.encoding=UTF8 -jar MDS.jar {1|2}

E.g. java -Dfile.encoding=UTF8 -jar MDS.jar 1


Note: The executable jar file works only with version 3.9.1 (latest) of CoreNLP libraries. In the case of not finding the specified version, use the java files in "src" folder.



