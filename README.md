# QuranSimiraty
## Knime - Similarity translator Surah (Al-Fatihah)

# Overview
   * This is a text mining project to verify that Surah Al-Fatihah is Al-Fatihah, find different translations and the closest percentage. by using a computer as a central     analysis this project is going to teach computers to understand more about Al-Fatihah by mining some mathematical matrix text through a no-code mining tool.
  
# Tools of use
   * KNIME
  
# package in need
   * Textproccessing (in knime)

# Steps
   * File Data or Access Data
   * Tranform Data
   * Text preprocessing
   * create model
   * View the result
# Method
   * Access Data
   * Use the Excel file in the database folder where this data is stored. KNIME

![Imgur](https://i.imgur.com/I0KqQXs.jpg)
 
* Result
 ![Imgur](https://i.imgur.com/wG3d3R1.jpg)
 
# Tranform Data
 # Tranpose data
 * Result
![Imgur](https://i.imgur.com/DeAiEQq.jpg)

 * Node Column Filter.
 * Result
 
![Imgur](https://i.imgur.com/5WniDM2.jpg)
 
 * Node Node Transpose .
 * Result
 
 ![Imgur](https://i.imgur.com/jij924h.jpg)
 
 * Node Column Combiner .
 * Node Column Fillter .
 * Result
 
 ![Imgur](https://i.imgur.com/JavOIIE.jpg)
 
 * Node Table Creator.
 * Node Column Appender.
 * Result
 
 ![Imgur](https://i.imgur.com/16XZEnG.jpg)
 ![Imgur](https://i.imgur.com/tJUuwND.jpg)
 
 * Node String Manipulation
 * Result
 
![Imgur](https://i.imgur.com/4rR2ktE.jpg)
 
# Text preprocessing
![Imgur](https://i.imgur.com/i22Gzhv.jpg)

1.Convert String to Document where Title will be Column tran_id and Text will be column surah. And then delete the columns that are not in use. By using!

* Node Strings To Document
* Node Column Fillter

![Imgur](https://i.imgur.com/VnqOpmt.jpg)

* Result

![Imgur](https://i.imgur.com/wvt5Pfz.jpg)

2.Remove special words such as , : _ ^ etc., change all letters to lowercase, remove unnecessary words. Frequently encountered words such as the,to,and etc. By using!

* Node Punctuation Erasure.
* Case Converter.
* Stop Word Filter.
* Result

![Imgur](https://i.imgur.com/U8k77K2.jpg)

3.Mark which words are in what category. And using Stanford Tagger to mark the words again in case the words in the POS Tagger are missing or skipped, change the verb into all verb one. By using!

* Node POS Tagger.
* Node Stanford Tagger.
* Node Standord Lemmatizer.

* Result

![Imgur](https://i.imgur.com/Zy7v9F9.jpg)

4.Separate words into individual words. in order to be able to compare each word. By using:

* Node Bag Of Words Creator

* Result

![Imgur](https://i.imgur.com/lA9VbYL.jpg)

5.Put all the separate words together in each column of words. By using:

* Node Document Vector

![Imgur](https://i.imgur.com/tCtCKif.jpg)

* Result

![Imgur](https://i.imgur.com/gA0PLLk.jpg)

# Model

![Imgur](https://i.imgur.com/8qGGB9g.jpg)

1.Model to find the frequency using TF and IDF and use math formula to multiply the results of TF,IDF

* Node TF
* Node Column Rename
* Node IDF
* Node Math Formula

* Result

![Imgur](https://i.imgur.com/kDLPZqp.jpg)

* Node Document Vector.

![Imgur](https://i.imgur.com/Q6PCYGc.jpg)

* Result

![Imgur](https://i.imgur.com/85xMzYW.jpg)

#Similarity View(TF-IDF)

![Imgur](https://i.imgur.com/WGKMMK0.jpg)

* Similarity View

* Result

![Imgur](https://i.imgur.com/XGwzx9B.jpg)
  
* Determines the translator to compare the similarity use Column ID.

#Conclusion

* Result

 ![Imgur](https://i.imgur.com/D5o24Lj.jpg)




