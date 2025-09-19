---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.17.3
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# My Notebook

## Some Python Code

```{code-cell} ipython3
x = 3
y = 4

x ** y
```

```{code-cell} ipython3
x + 10
```

## Load & Plot Data

```{code-cell} ipython3
import polars as pl

df = (
    pl.read_csv(
        "https://gist.githubusercontent.com/slopp/ce3b90b9168f2f921784de84fa445651/raw/4ecf3041f0ed4913e7c230758733948bc561f434/penguins.csv",
        null_values="NA",
    )
)

df.head()
```

```{code-cell} ipython3
import matplotlib.pyplot as plt

fig, ax = plt.subplots(figsize=(6, 4))

ax.scatter(df["body_mass_g"], df["flipper_length_mm"])
ax.set_title("Penguin Flipper length and body is Correlated!")
ax.set_ylabel("Flipper Length (mm)")
ax.set_xlabel("Body Mass (g)")
```

## Common Markdown

### Typography

- bold text **bold text**
- italics *italicized text*

---

- unordered bullet points
- 2nd bullet point
    - indented point

---
 
1. ordered bullet points
2. 2nd bullet point
    1. indented point

---

https://en.wikipedia.org/wiki/Project_Jupyter

[Check out this jupyter link](https://en.wikipedia.org/wiki/Project_Jupyter)

![project jupyter logo](https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Jupyter_logo.svg/207px-Jupyter_logo.svg.png)

+++

## MyST Markdown 


### Roles

\{…\}\`…\`

{del}`this text is struck through`

{smallcaps}`this is small caps!`

C{sub}`6`H{sub}`12`O{sub}`6`

Today is Sept 19{sup}`th`


To copy text, clikc {kbd}`Ctrl` + {kbd}`C`

+++

### Quotations

> This is my quote, it is something I have said in the past.
>
> -- Cameron Riddell

+++

### Definition List

Water
: Something you drink to stay alive

Air
: Something you breathe to stay alive

+++

### Footnotes

Lets add a footnote[^footnote-1] and another [^footnote-2]

[^footnote-1]: Here is a comment/footnote about the referenced text
[^footnote-2]: Here is another comment/footnote about the referenced text

+++

[](doi:10.1038/s41586-020-2649-2)
