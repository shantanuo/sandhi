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
