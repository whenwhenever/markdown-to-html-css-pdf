# Using Pandoc to generate HTML and PDFs from Markdown 

### on a Mac running macOS 14.6.1

To install the needed components you can use [Homebrew](https://brew.sh)



### Two Components are needed:

1. [Pandoc](https://pandoc.org)
2. [MacTeX](https://www.tug.org/mactex/)

----

### Install instructions:

Use Homebrew to install pandoc:
```
brew install pandoc
```

Then use Homebrew to install the PDFLaTex program.

```
brew install --cask mactex-no-gui
```

You should now have all the needed components but it won't work until you restart your terminal.

----

### Use instructions markdown to html:

The idea is to be able to create an html file using css for styling

```
pandoc file.md -o file.html -s --css=style.css
```

----

### Use instructions markdown to PDF:

#### Option 1

In this case, you can use either css for styling, but it requires an intermediary step markdown to html and then print as PDF.

```
pandoc file.md -o file.html -s --css=style.css
```

#### Option 2

Or you can do the styling with LaTex in which case you can go directly from markdown to PDF:

```
pandoc file.md -o file.pdf  --template=latexstyle.tex
```

----

Inspiration :

https://gist.github.com/ilessing/7ff705de0f594510e463146762cef779#file-pandoc-markdown-to-pdf-md
