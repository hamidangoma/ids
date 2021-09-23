## Miscellaneous learnings

### For hidden Code:

```python
#@hidden
from IPython.display import HTML, Image

HTML('''<script>
code_show=true; 
function code_toggle() {
 if (code_show){
 $('.cm-comment:contains(@hidden)').closest('div.input').hide();
 } else {
 $('.cm-comment:contains(@hidden)').closest('div.input').show();
 }
 code_show = !code_show
} 
$( document ).ready(code_toggle);
</script>
The raw code for the following figures related code
is by default hidden. This can be used to give
quizzes whereby the raw dataset is hidden but a plot 
is shown or so on. To toggle on/off the raw code, 
<a href="javascript:code_toggle()">click here to 
toggle for raw hidden code</a>.''')
```

### For running bash in ipynb

```python
## copy a file
!cp myscript.py myscript2.py
```

```python
## run timeit on python
!python -m timeit -r 20 '"-".join(str(n) for n in range(100))'
## r does repetition
## The output suggests there were 20000 loops, repeated 20 
## times for accuracy, and 

"-".join(str(n) for n in range(100))
```

```python
## pip install packages
!pip install pstats 
```

### Save a file dynamically into a .py or .R file from jupyter notebook
```python
%save -a example.py -n 28   ## change 28 to respective line number
```

### Convert .ipynb to .md file
```python
jupyter nbconvert --to FORMAT notebook.ipynb
```

Here FORMAT could be `Markdown`, `html`, `pdf`, `tex`, `slides`