# sandhi
denormalized sanskrit sandhi (based on Panini sutra) in pure python.
Run all cells in the notebook, test your word at the end of the script. for e.g.

sandhi_builder('पितृ उपदेश') 

returns {'पित्रुपदेश'}

If you do not want to use python, then look for the last and first character in the file (sandhi_code_out.txt) like a telephone directory. for e.g. if you are looking for sandhi of यज् + न then look for  **ज् न** in the index file. 

!grep 'ज् न' sandhi_code_out.txt

ज् न ज्ञ 2.1.1 श्चुत्व

ज् न ञ्न 2.7.1 अनुनासिक

You will get ज्ञ and hence your sandhi word will be 
य + ज्ञ = यज्ञ

This is poor man's sandhi builder. For richer experiece you can visit:

https://sanskrit.uohyd.ac.in/scl/#

_____

If there is more than one level of nesting required, then you need to type the entry again. For e.g. when you type सत् जन you expect सज्जन  but the software will reply सद् जन You need to again type सद् जन and you will get the expected सज्जन 
_____

1) Underscore ('_') in Sandhi Output:
   
If an underscore ('_') appears in the Sandhi output, it indicates that the words cannot be joined. For example:

Input: मुनी इमो
Output: मुनी_इमो

This implies that no Sandhi is possible due to प्रकृतिभाव सन्धि (ईदूदेद्द्विवचनं प्रगृह्यम्). Even if the word मुनीमो is also returned, it should be ignored.

2) Asterisk ('*') in Sandhi Output:
   
If a word in the output is followed by an asterisk ('*'), it signifies that the word is preferred. For example:

Input: महा ऋषी
Output: महर्षी* महार्षी

Here, the word महर्षी* is marked with an asterisk *, indicating that it is more appropriate than महार्षी

_____

A) Telegram Bot:

f you are using Telegram, add the "Sanskrit One" bot to your contacts list.

https://t.me/sanskritonebot


B) Android App:

If using android phone, add "Marathi Spell check" app. (It has Sanskrit Sandhi tab.)

https://play.google.com/store/apps/details?id=com.myapp.marathispellcheckandsanskritsandhi

You get three in one! sandhi, splitter and spell checker.

_____

Achived accuracy of 93.5% in the Bhagvad gita benchmark corpus:

https://github.com/sanskrit-sandhi/SandhiKosh/

Compare with other solutions in this paper:

http://www.lrec-conf.org/proceedings/lrec2018/pdf/755.pdf

JNU: 23.64% || UoH: 73.1% || INRIA: 82.1%
