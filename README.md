# sandhi
denormalized sanskrit sandhi (based on Panini sutra) in pure python.
Run all cells in the notebook, test your word at the end of the script. for e.g.

sandhi_builder('पितृ उपदेश') 

returns {'पित्रुपदेश'}

If you do not want to use python, then look for the last and first character in the index file. for e.g.
if you are looking for sandhi of यज् + न then look for  **ज् न** in the index file. 

!grep 'ज् न' sandhi_code_out.txt

ज् न ज्ञ 2.1.1 श्चुत्व

ज् न ञ्न 2.7.1 अनुनासिक

You will get ज्ञ and hence your sandhi word will be 
य + ज्ञ = यज्ञ
