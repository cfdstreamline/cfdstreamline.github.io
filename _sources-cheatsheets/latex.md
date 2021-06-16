---
title: Latex
layout: wiki
sidebar: toc
excerpt: ""
header:
  teaser: /assets/images/logos/logo_latex.svg
---


## Overview

```latex
% All comment lines start with %. There are no multi-line comments
% Every LaTeX command starts with a backslash (\)


% Preamble
%-----------------------------------------------
% Document Class
\documentclass[12pt]{article}

% Packages
\usepackage{caption}     % Sets figure captions
\usepackage{float}       % Allows figures to float
\usepackage{hyperref}    % Allows hyperlinks

% Document Properties Definitions
\author{Author's name} 
\date{\today}
\title{Title}


% Document
%-----------------------------------------------
\begin{document}

% Title
\maketitle
\newpage          % Creates a new page

% Tables of Content
\tableofcontents % Main table of content
\newpage
\listoffigures   % List of figures
\newpage
\listoftables    % List of tables
\newpage

% Abstract: command is available in the document classes article and report.
\begin{abstract}
 \LaTeX{} documentation written as \LaTeX! How novel and totally not
 my idea!
\end{abstract}

% Sections
\section{Introduction}
Hello, my name is Colton and together we're going to explore \LaTeX!

\section{Another section}
This is the text for another section. I think it needs a subsection.

\subsection{This is a subsection} % Subsections are also intuitive.
I think we need another one.

\subsubsection{Pythagoras}
Much better now.
\label{subsec:pythagoras}

\section*{This is an unnumbered section}
However not all sections have to be numbered!

\section{Some Text notes}
\LaTeX{} is generally pretty good about placing text where it should
go. If
a line \\ needs \\ to \\ break \\ you add \textbackslash\textbackslash{}
to the source code.

Separate paragraphs by empty lines.

You need to add a backslash after abbreviations (if not followed by a comma), because otherwise the spacing after the dot is too large:
E.g., i.e., etc.\ are are such abbreviations.

\section{Lists}
\begin{enumerate} % This creates an "enumerate" environment.
  % \item tells the enumerate to increment
  \item Salad.
  \item 27 watermelon.
  \item A single jackrabbit.
  % we can even override the item number by using []
  \item[how many?] Medium sized squirt guns.

  Not a list item, but still part of the enumerate.
\end{enumerate} % All environments must have an end.

\section{Math}

Here's how you state all x that belong to X, $\forall x \in X$.
We can also enter math mode with \[a^2 + b^2 = c^2 \].

% Display math with the equation 'environment'
\begin{equation} % enters math-mode
    c^2 = a^2 + b^2.
    \label{eq:pythagoras} % for referencing
\end{equation} % all \begin statements must have an end statement

Eqn.~\ref{eq:pythagoras} is also known as the Pythagoras Theorem which is also
the subject of Sec.~\ref{subsec:pythagoras}. A lot of things can be labeled:
figures, equations, sections, etc.


\section{Figures}

% See https://en.wikibooks.org/wiki/LaTeX/Floats,_Figures_and_Captions for more details

\begin{figure}[H] % H here denoted the placement option.
    \centering % centers the figure on the page
    % Inserts a figure scaled to 0.8 the width of the page.
    %\includegraphics[width=0.8\linewidth]{right-triangle.png}
    % Commented out for compilation purposes. Please use your imagination.
    \caption{Right triangle with sides $a$, $b$, $c$}
    \label{fig:right-triangle}
\end{figure}

\subsection{Table}

\begin{table}[H]
  \caption{Caption for the Table.}
  % The basic is simple: one letter for each column, to control alignment:
  % basic options are: c, l, r and p for centered, left, right and paragraph
  % optionnally, you can add a | for a vertical line
  % See https://en.wikibooks.org/wiki/LaTeX/Tables for more details
  \begin{tabular}{c|cc}  % here it means "centered | vertical line, centered centered"
    Number &  Last Name & First Name \\ % Column rows are separated by &
    \hline % a horizontal line
    1 & Biggus & Dickus \\
    2 & Monty & Python
  \end{tabular}
\end{table}

\section{Getting \LaTeX{} to not compile something (i.e.\ Source Code)}

% There are other packages that exist (i.e. minty, lstlisting, etc.)
% but verbatim is the bare-bones basic one.
\begin{verbatim}
  print("Hello World!")
  a%b; % look! We can use % signs in verbatim.
  random = 4; #decided by fair random dice roll, https://www.xkcd.com/221/
  See https://www.explainxkcd.com/wiki/index.php/221:_Random_Number
\end{verbatim}

\section{Compiling}

\begin{enumerate}
  \item Write the document in plain text (the ``source code'').
  \item Compile source code to produce a pdf.
    The compilation step looks like this (in Linux): \\
    \begin{verbatim}
      > pdflatex learn-latex.tex
    \end{verbatim}
\end{enumerate}

\section{Hyperlinks}

There exists two main types of links: visible URL \\
\url{https://learnxinyminutes.com/docs/latex/}, or
\href{https://learnxinyminutes.com/docs/latex/}{shadowed by text}
% You can not add extra-spaces or special symbols into shadowing text since it
% will cause mistakes during the compilation

This package also produces list of thumbnails in the output pdf document and
active links in the table of contents.

\section{Writing in ASCII or other encodings}

It is easy to insert accents and basic Latin symbols, with backslash shortcuts
Like \,c, \'e, \`A, \ae and \oe etc.  % for ç, é, À, etc
% See https://en.wikibooks.org/wiki/LaTeX/Special_Characters#Escaped_codes for more

To write directly in UTF-8, when compiling with pdflatex, use
\begin{verbatim}
    \usepackage[utf8]{inputenc}
\end{verbatim}
The selected font has to support the glyphs used for your document, you have to add
\begin{verbatim}
    \usepackage[T1]{fontenc}
\end{verbatim}


\section{End}

That's all for now!

% Bibliography
\begin{thebibliography}{1}
  \bibitem{latexwiki} The amazing \LaTeX{} wikibook: \emph{https://en.wikibooks.org/wiki/LaTeX}
  \bibitem{latextutorial} An actual tutorial: \emph{http://www.latex-tutorial.com}
\end{thebibliography}

% Ends the document
\end{document}
```


## Document Classes

Usage: `\documentclass[opt,opt]{class}`.


### Classes

```latex
book    % Default is two-sided.
report  % No \part divisions.
article % No \part or \chapter divisions.
letter  % Letter.
slides  % Large sans-serif font.
```


### Common options

```latex
10pt/11pt/12pt       % Font size.
letterpaper/a4paper  % Paper size.
twocolumn            % Use two columns.
twoside              % Set margins for two-sided.
landscape            % Landscape orientation. Must use dvips -t landscape.
draft                % Double-space lines.
```


## Packages

```latex
\usepackage{fullpage}  % uses 1 inch margins.
\usepackage{anysize}   % sets margins: \marginsize{l}{r}{t}{b}
\usepackage{multicol}  % uses n columns: \begin{multicols}{n}.
\usepackage{lscape}    % allows a page to be rendered in landscape mode
\usepackage{appendix}  % allows appendix section to be included
\usepackage{lettrine}  % supports various dropped capitals styles
\usepackage{hyperref}  % allows hyperlinks
\usepackage{url}       % inserts URL: \url{http://... }.
\usepackage{latexsym}  % uses \LaTeX\ symbol font.

\usepackage{graphicx}  % shows image: \includegraphics[width=x]{file}.
\usepackage{epstopdf}  % convert eps figures to pdf
\usepackage{caption}   % sets figure captions
\usepackage{subcaption}% captions for the subfigures
\usepackage{float}     % allows figures to float

\usepackage{amsmath}   % American Mathematical Society package (allows \eqref)
\usepackage{amssymb}   % American Mathematical Society extra symbols
\usepackage{amsthm}    % offers the theorem setup of the AMS document classes
\usepackage{cancel}    % allows showing canceled terms in equations

\usepackage{tabularx}  % an extension of tabular which has an additional column designator, X, which creates a paragraph-like column whose width automatically expands so that the declared width of the environment is filled
\usepackage{booktabs}  % enhances the quality of tables and provides extra commands
\usepackage{multirow}  % tables with cell occuping more than one row
\usepackage{threeparttable} % tables with footnotes
\usepackage{placeins}  % defines a \FloatBarrier command, beyond which floats may not pass
```


## Title

Usage: `\maketitle`
```latex
\author{text}          % Author of document.
\title{text}           % Title of document.
\date{text}            % Date.
```


## Page Style

```latex
\pagestyle{empty}      % Both header and footer are cleared
\pagestyle{plain}      % Header is clear, but the footer contains the page number in the center.
\pagestyle{headings}   % Footer is blank, header displays information according to document class (e.g., section name) and page number top right.
\pagestyle{myheadings} % Page number is top right, and it is possible to control the rest of the header.
```


## Tables of Content

```latex
\tableofcontents % Adds a table of content.
\listoffigures   % List of figures
\listoftables    % List of tables
```


## Document Structure

```latex
\setcounter{secnumdepth}{x} % suppresses heading numbers of depth > x, where chapter has depth 0. 

\part{title}
\chapter{title}
\section{title}
\section*{title}, % not numbers the section and it does not appear in the table of contents
\subsection{title}
\subsubsection{title}
\paragraph{title}
\subparagraph{title}
```


## Text Environments

```latex
\begin{comment}   % Comment (not printed). Requires verbatim package.
\begin{quote}     % Indented quotation block.
\begin{quotation} % Like quote with indented paragraphs.
\begin{verse}     % Quotation block for verse.
```


## Text Properties

### Font Face

| Command | Declaration | Effect |
| :-: | :-: | :-- |
|`\textrm{text}`     | `{\rmfamily text}`  | Roman family |
|`\textsf{text}`     | `{\sffamily text}`  | Sans serif family |
|`\texttt{text}`     | `{\ttfamily text}`  | Typewriter family |
|`\textmd{text}`     | `{\mdseries text}`  | Medium series |
|`\textbf{text}`     | `{\bfseries text}`  | Bold series |
|`\textup{text}`     | `{\upshape text}`   | Upright shape |
|`\textit{text}`     | `{\itshape text}`   | Italic shape |
|`\textsl{text}`     | `{\slshape text}`   | Slanted shape |
|`\textsc{text}`     | `{\scshape text}`   | Small Caps shape |
|`\emph{text}`       | `{\em text}`        | Emphasized |
|`\textnormal{text}` | `{\normalfont text}`| Document font |
|`\underline{text}`  |                     | Underline |


### Font size

Usage `{\command text }`

```latex
\tiny         % tiny
\scriptsize   % scriptsize
\footnotesize % footnotesize
\small        % small
\normalsize   % normalsize
\large        % large
\Large        % Large
\LARGE        % LARGE
\huge         % huge
\Huge         % Huge
```

<!--
#### Verbatim text
\begin{verbatim} Verbatim environment.
\begin{verbatim*} Spaces are shown as .
\verb!text! Text between the delimiting characters (in
this case `!') is verbatim.

#### Justification
Environment Declaration
\begin{center} \centering
\begin{flushleft} \raggedright
\begin{flushright} \raggedleft

#### Miscellaneous
\linespread{x} changes the line spacing by the multiplier x.

### Symbols
& \& \_ . . . \ldots  \textbullet
$ \$ ^ \^{} j \textbar n \textbackslash
% \% ~ \~{} # \# x \S

### Accents
o \`o o \'o ^o \^o ~o \~o o \=o
_o \.o o \"o o \c o o \v o }o \H o
c \c c o.
\d o o

\b o oo \t oo  \oe
 \OE  \ae  \AE a \aa A \AA
 \o  \O l \l L \L  \i
 \j < ~` > ?`

### Delimiters
` ` \ `` f \{ [ [ ( ( < \textless
' ' " '' g \} ] ] ) ) > \textgreater

### Dashes
Name Source Example Usage
hyphen - X-ray In words.
en-dash -- 1{5 Between numbers.
em-dash --- Yes|or no? Punctuation.


### Lists
```latex
\begin{enumerate}     % Numbered list.
  \item text          % Adds an item.
\end{enumerate}

\begin{itemize}       % Bulleted list.
  \item text          % Adds an item.
\end{itemize}

\begin{description}   % Description list.
  \item[x] text       % Uses x instead of normal bullet or number. Required for descriptions
\end{description}
```

### References
\label{marker} Set a marker for cross-reference, often of the
form \label{sec:item}.
\ref{marker} Give section/body number of marker.
\pageref{marker} Give page number of marker.
\footnote{text} Print footnote at bottom of page.

## Floating bodies
\begin{table}[place] Add numbered table.
\begin{figure}[place] Add numbered gure.
\begin{equation}[place] Add numbered equation.
\caption{text} Caption for the body.
The place is a list valid placements for the body. t=top,
h=here, b=bottom, p=separate page, !=place even if ugly.
Captions and label markers should be within the environment.





## Line and page breaks
\\ Begin new line without new paragraph.
\\* Prohibit pagebreak after linebreak.
\kill Don't print current line.
\pagebreak Start new page.
\noindent Do not indent current line.

## Miscellaneous
\today March 28, 2017.
$\sim$ Prints  instead of \~{}, which makes ~.
~ Space, disallow linebreak (W.J.~Clinton).
\@. Indicate that the . ends a sentence when following
an uppercase letter.
\hspace{l} Horizontal space of length l (Ex: l = 20pt).
\vspace{l} Vertical space of length l.
\rule{w}{h} Line of width w and height h.


## Tabular environments

### `tabbing` environment
\= Set tab stop. \> Go to tab stop.
Tab stops can be set on \invisible" lines with \kill at the end
of the line. Normally \\ is used to separate lines.


### `tabular` environment

`\begin{array}[`*pos*`]{`*cols*`}`\
`\begin{tabular}[`*pos*`]{`*cols*`}`\
`\begin{tabular*}{`*width*`}[`*pos*`]{`*cols*`}`


### `tabular` column specification

<span>@p@p<span>-</span>@</span> `l` & Left-justified column.\
`c` & Centered column.\
`r` & Right-justified column.\
`p{`*width*`}` & Same as `\parbox[t]{`*width*`}`.\
`@{`*decl*`}` & Insert *decl* instead of inter-column space.\
`|` & Inserts a vertical line between columns.

### `tabular` elements

<span>@p@p<span>-</span>@</span> `\hline` & Horizontal line between
rows.\
`\cline{`$x$`-`$y$`}` & Horizontal line across columns $x$ through $y$.\
`\multicolumn{`*n*`}{`*cols*`}{`*text*`}`\
& A cell that spans *n* columns, with *cols* column specification.


## Math mode

For inline math, use `\(...\)` or `$...$`. For displayed math, use
`\[...\]` or `\begin{equation}`.

Superscript$^{x}$ & `^{x}` & Subscript$_{x}$ & `_{x}`\
$\frac{x}{y}$ & `\frac{x}{y}` & $\sum_{k=1}^n$ & `\sum_{k=1}^n`\
$\sqrt[n]{x}$ & `\sqrt[n]{x}` & $\prod_{k=1}^n$ & `\prod_{k=1}^n`\

### Symbols

$\leq$ & `\leq` & $\geq$ & `\geq` & $\neq$ & `\neq` & $\approx$ &
`\approx`\
$\times$ & `\times` & $\div$ & `\div` & $\pm$ & `\pm` & $\cdot$ &
`\cdot`\
$^{\circ}$ & `^{\circ}` & $\circ$ & `\circ` & $\prime$ & `\prime` &
$\cdots$ & `\cdots`\
$\infty$ & `\infty` & $\neg$ & `\neg` & $\wedge$ & `\wedge` & $\vee$ &
`\vee`\
$\supset$ & `\supset` & $\forall$ & `\forall` & $\in$ & `\in` &
$\rightarrow$ & `\rightarrow`\
$\subset$ & `\subset` & $\exists$ & `\exists` & $\notin$ & `\notin` &
$\Rightarrow$ & `\Rightarrow`\
$\cup$ & `\cup` & $\cap$ & `\cap` & $\mid$ & `\mid` & $\Leftrightarrow$
& `\Leftrightarrow`\
$\dot a$ & `\dot a` & $\hat a$ & `\hat a` & $\bar a$ & `\bar a` &
$\tilde a$ & `\tilde a`\

$\alpha$ & `\alpha` & $\beta$ & `\beta` & $\gamma$ & `\gamma` & $\delta$
& `\delta`\
$\epsilon$ & `\epsilon` & $\zeta$ & `\zeta` & $\eta$ & `\eta` &
$\varepsilon$ & `\varepsilon`\
$\theta$ & `\theta` & $\iota$ & `\iota` & $\kappa$ & `\kappa` &
$\vartheta$ & `\vartheta`\
$\lambda$ & `\lambda` & $\mu$ & `\mu` & $\nu$ & `\nu` & $\xi$ & `\xi`\
$\pi$ & `\pi` & $\rho$ & `\rho` & $\sigma$ & `\sigma` & $\tau$ & `\tau`\
$\upsilon$ & `\upsilon` & $\phi$ & `\phi` & $\chi$ & `\chi` & $\psi$ &
`\psi`\
$\omega$ & `\omega` & $\Gamma$ & `\Gamma` & $\Delta$ & `\Delta` &
$\Theta$ & `\Theta`\
$\Lambda$ & `\Lambda` & $\Xi$ & `\Xi` & $\Pi$ & `\Pi` & $\Sigma$ &
`\Sigma`\
$\Upsilon$ & `\Upsilon` & $\Phi$ & `\Phi` & $\Psi$ & `\Psi` & $\Omega$ &
`\Omega`


## Bibliography and Citations

When using , you need to run `latex`, `bibtex`, and `latex` twice more
to resolve dependencies.

### Citation Types

`\cite{`*key*`}` & Full author list and year. (Watson and Crick 1953)\
`\citeA{`*key*`}` & Full author list. (Watson and Crick)\
`\citeN{`*key*`}` & Full author list and year. Watson and Crick (1953)\
`\shortcite{`*key*`}` & Abbreviated author list and year. ?\
`\shortciteA{`*key*`}` & Abbreviated author list. ?\
`\shortciteN{`*key*`}` & Abbreviated author list and year. ?\
`\citeyear{`*key*`}` & Cite year only. (1953)\

All the above have an `NP` variant without parentheses; Ex. `\citeNP`.

### `\BibTeX` entry types

`@article` & Journal or magazine article.\
`@book` & Book with publisher.\
`@booklet` & Book without publisher.\
`@conference` & Article in conference proceedings.\
`@inbook` & A part of a book and/or range of pages.\
`@incollection` & A part of book with its own title.\
`@misc` & If nothing else fits.\
`@phdthesis` & PhD. thesis.\
`@proceedings` & Proceedings of a conference.\
`@techreport` & Tech report, usually numbered in series.\
`@unpublished` & Unpublished.\


### `\BibTeX` Fields

`address` & Address of publisher. Not necessary for major publishers.\
`author` & Names of authors, of format ....\
`booktitle` & Title of book when part of it is cited.\
`chapter` & Chapter or section number.\
`edition` & Edition of a book.\
`editor` & Names of editors.\
`institution` & Sponsoring institution of tech. report.\
`journal` & Journal name.\
`key` & Used for cross ref. when no author.\
`month` & Month published. Use 3-letter abbreviation.\
`note` & Any additional information.\
`number` & Number of journal or magazine.\
`organization` & Organization that sponsors a conference.\
`pages` & Page range (`2,6,9--12`).\
`publisher` & Publisher’s name.\
`school` & Name of school (for thesis).\
`series` & Name of series of books.\
`title` & Title of work.\
`type` & Type of tech. report, ex. “Research Note”.\
`volume` & Volume of a journal or book.\
`year` & Year of publication.\

Not all fields need to be filled. See example below.


### Common `\BibTeX` Style Files

`abbrv` & Standard & `abstract` & `alpha` with abstract\
`alpha` & Standard & `apa` & APA\
`plain` & Standard & `unsrt` & Unsorted\

The LaTeX document should have the following two lines just before
`\end{document}`, where `bibfile.bib` is the name of the  file.

    \bibliographystyle{plain}
    \bibliography{bibfile}


### `\BibTeX` Example

The  database goes in a file called *file*`.bib`, which is processed
with `bibtex file`.

    @String{N = {Na\-ture}}
    @Article{WC:1953,
      author  = {James Watson and Francis Crick},
      title   = {A structure for Deoxyribose Nucleic Acid},
      journal = N,
      volume  = {171},
      pages   = {737},
      year    = 1953
    }

-->

## [Source](https://learnxinyminutes.com/docs/latex/){:target="_blank"}


## See Also

- [Learn X in Y minutes](https://learnxinyminutes.com/docs/latex/){:target="_blank"}
- [Wikibooks](https://en.wikibooks.org/wiki/LaTeX){:target="_blank"}
- [Overleaf - Learn Latex in 30 Minutes](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes){:target="_blank"}
- [Latex Tutorial](https://latex-tutorial.com/){:target="_blank"}
