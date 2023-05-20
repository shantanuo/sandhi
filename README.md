# sandhi
denormalized sanskrit sandhi based on panini sutra.
run all cells in the notebook, add your word at the end of the script. for e.g.

sandhi_builder('पितृ उपदेश') 
# returns {'पित्रुपदेश'}

If you do not ant to use python, then look for the last and first character in the index file. for e.g.
if you are looking for sandhi of यज् + न then look for  **ज् न** in the index file. You will get ज्ञ and hence your sandhi word will be 
य + ज्ञ = यज्ञ
