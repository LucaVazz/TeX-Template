# DHBW - LaTeX - Template
Please use XeLaTeX or LuaLaTex for building.

## Features
- all formal layout-properties of the document are in accordance to the requirements given by the Technical Faculty of DHBW Mannheim.
- Titlepages for Internship Reports, Study Reports and Bachelor Thesis in accordance to these requirements included
![various Titlepages](http://i.imgur.com/ddOe000.png)
- Fully customizable coloring
![Coloring](http://i.imgur.com/TGjZShi.png)
- Easy switching between the (default) *english* and *german* version of the document


## How to Setup and Use
1. inside `./setup.tex`:
	- choose the type of your Report
	- choose if you want to write your report in english or german
	- fill out the fields for your informations
	- choose your desired color theme or define your own
2. places the entries for your bibliography into `./resources/references.bib`
3. place the `.tex`-files containing your content into `./content` and define the structure of your content inside `./content/structure.tex`
4. fill your acronyms and custom macros as needed into `./content/acronyms.tex` and `./content/macros.tex`
5. save your image files into `./resources`
	- you can then use them easily by just referencing `\includegraphics{asdf}` if you saved your file at `./resources/asdf.png`


## Included Custom Elements for Ease of Use
#### striped Tables
```Latex
\begin{stripedacenttable}
	{formating}
	{Headings-Content}
	row definitions
\end{stripedacenttable}

\begin{stripedtable}
	{coloring}
	{formating}
	{Headings-Content}
	row definitions
\end{stripedtable}
```

- formating should have the form `x^x^x^...` where `x` specifies the alignment for the column
	+ possible aligments: `l`: left-aligned , `c`: centered , `r`: right-aligned

> *Example:*
> ```Latex
\begin{stripedacenttable}
	{c^l^l}
	{Quarter & asdf & foobar}
	prev. Year & 42 & 17 \\
	Q1 & -3 & -7 \\
	Q2 & +7 & -1 \\
	Q3 & -4 & +12 \\
	Q4 & +2 & +2 \\
\end{stripedacenttable}

> \begin{stripedtable}
	{Green}
	{c^l^l}
	{Quarter & asdf & foobar}
	prev. Year & 42 & 17 \\
	Q1 & -3 & -7 \\
	Q2 & +7 & -1 \\
	Q3 & -4 & +12 \\
	Q4 & +2 & +2 \\
\end{stripedtable}
```

> ![Tables](http://i.imgur.com/Soih9hH.png)

#### Code Listings
```Latex
\begin{lstlisting}[
	caption={description of your program}
   	\label{lst:name},
   	captionpos=b,
   	language=language-name
]
your code
\end{lstlisting}
```

> *Example:*

> ```Latex
\begin{lstlisting}[
	caption={The Classic, realized in Python}
   	\label{lst:python1},
   	captionpos=b,
   	language=Python
]
> # classic
>
> hi = "Hello Wolrd"
print(hi)
\end{lstlisting}
```

> ![Code Lisitng](http://i.imgur.com/8zXqzOZ.png)

#### Citations in the Footnotes
````Latex
\footnotecite{source}
```

#### Prevent Pagebreaks absolutely, definitively
```Latex
\begin{absolutelynopagebreak}
	content
\end{absolutelynopagebreak}
```


---


## Contributing
I'm open for all forks, feedback and Pull Requests ;)
