# sandhi

Denormalized Sanskrit Sandhi (based on Pāṇini's sūtras) implemented in pure Python.

## 🚀 Run in Google Colab

Use the link below to open and run the notebook directly in Google Colab (no installation required):

**https://colab.research.google.com/github/shantanuo/sandhi/blob/main/sanskrit_sandhi.ipynb**

Run all the cells in the notebook, then test your word at the end of the script. For example:

```python
sandhi_builder('पितृ उपदेश')
```

returns:

```python
{'पित्रुपदेश'}
```

---

If you do not want to use Python, look for the last character of the first word and the first character of the second word in the index file (`sandhi_code_out.txt`), similar to looking up a telephone directory.

For example, if you are looking for the Sandhi of **यज् + न**, search for **ज् न** in the index file:

```bash
grep 'ज् न' sandhi_code_out.txt
```

Output:

```
ज् न ज्ञ 2.1.1 श्चुत्व
ज् न ञ्न 2.7.1 अनुनासिक
```

You get **ज्ञ**, and hence the Sandhi word becomes:

```
य + ज्ञ = यज्ञ
```

This is a poor man's Sandhi builder. For a richer experience, visit:

https://sanskrit.uohyd.ac.in/scl/#

---

If more than one level of Sandhi is required, enter the output again.

For example, when you type:

```
सत् जन
```

you may expect:

```
सज्जन
```

but the software will first return:

```
सद् जन
```

Enter **सद् जन** again to obtain the expected result:

```
सज्जन
```

---

### 1) Underscore (`_`) in Sandhi Output

If an underscore (`_`) appears in the output, it indicates that the words cannot be joined.

Example:

**Input**

```
मुनी इमो
```

**Output**

```
मुनी_इमो
```

This indicates that no Sandhi is possible because of **प्रकृतिभाव सन्धि (ईदूदेद्द्विवचनं प्रगृह्यम्)**.

Even if **मुनीमो** is also returned, it should be ignored.

### 2) Asterisk (`*`) in Sandhi Output

If a word is followed by an asterisk (`*`), it indicates the preferred form.

Example:

**Input**

```
महा ऋषी
```

**Output**

```
महर्षी* महार्षी
```

Here **महर्षी*** is the preferred form.

---

## A) Telegram Bot

If you use Telegram, add the **Sanskrit One** bot to your contacts:

https://t.me/sanskritonebot

## B) Android App

If you use an Android phone, install the **Marathi Spell Check** app. It includes a Sanskrit Sandhi tab.

https://play.google.com/store/apps/details?id=com.myapp.marathispellcheckandsanskritsandhi

You get three tools in one:

- Sandhi Builder
- Sandhi Splitter
- Spell Checker

---

Achieved **93.5% accuracy** on the Bhagavad Gītā benchmark corpus.

Compare it with other solutions mentioned in this paper:

http://www.lrec-conf.org/proceedings/lrec2018/pdf/755.pdf
