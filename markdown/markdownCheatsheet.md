# Markdown Syntax

Markdown is a lightweight plain text format for writing structured documents. Its design allows it to be converted to many output formats, (most commonly, html or pdf). It is easy to learn. Once you know a little, you will be able to write documents on GitHub and you'll be able to write Rmarkdown documents (markdown combined with R code). Rmarkdown has additional elements like support for mathematical equations.

- [Markdown Syntax](#markdown-syntax)
- [Headers](#headers)
  - [smaller size 2 header `<h2>`](#smaller-size-2-header-h2)
    - [even smaller size 3 header `<h3>`](#even-smaller-size-3-header-h3)
      - [tiny header (size 4)](#tiny-header-size-4)
        - [size 5 header](#size-5-header)
          - [size 6 header](#size-6-header)
- [Horizontal rule](#horizontal-rule)
- [Emphasis](#emphasis)
- [Escape special characters](#escape-special-characters)
- [Lists](#lists)
  - [Unordered lists](#unordered-lists)
  - [Ordered lists](#ordered-lists)
- [Block quotes](#block-quotes)
- [Links](#links)
  - [Linking to a chapter](#linking-to-a-chapter)
  - [Links to images](#links-to-images)
- [Code blocks](#code-blocks)
- [Strikethroughs](#strikethroughs)
- [Math equations](#math-equations)
  - [Inline](#inline)
  - [Centered block](#centered-block)
- [Tables](#tables)
- [Check boxes](#check-boxes)
- [Bibliographies](#bibliographies)
- [HTML](#html)

# Headers

The size of the header is determined by the number of \# used precedding the header. These are equivalent to `<h>` tags in html documents.

```
## smaller size 2 header `<h2>`
### even smaller size 3 header `<h3>`
#### tiny header (size 4) `<h4>`
```
produces this:

## smaller size 2 header `<h2>`
### even smaller size 3 header `<h3>`
#### tiny header (size 4)
##### size 5 header
###### size 6 header

A size 6 is the smallest you can go

# Horizontal rule

A horizontal rule can be achieved in three ways:
Use either three consectutive hyphens, asterisks, or underscores

```
---
***
___
```

---
***
___

Three hyphens are standard.

# Emphasis

It is easy to make words bold and italic by using asteriks (\*)

```
Make a word *italic*
Make a word **bold**
Make a word ***bold and italic***
```
produces this: 

Make a word *italic*

Make a word **bold**

Make a word ***bold and italic***

# Escape special characters

If you want to use characters like \* , \_ , \!, \+ etc in your code then you need to "escape" them. This involves typing a backslash immediately before the character eg. `\*` 

```
 \* , \_ , \!, \+ 
```
prduces this:

\* , \_ , \!, \+ 


# Lists

There are two types of lists, ordered and unordered lists. Unordered lists will use bullet points for each list item. You can use either \*, \+, or \- for list items

## Unordered lists

```
* item 1
* item 2
    + sub item
    + another sub item
    - another
    * last item
* item 3
```
produces:

* item 1
* item 2
    + sub item
    + another sub item
    - another
    * last item
* item 3

## Ordered lists

Uses numbers in consecutive order. Either type list numbers or use `1.`  for all list items 

```
1. item 1
2. item 2
3. item 3
```
or 
```
1. item 1
1. item 2
1. item 3
```

produces this: 

1. item 1
2. item 2
3. item 3

# Block quotes

Block quotes are a way to indent some text fro greater emphasis. Often people will use persoal quotes in a block quote.

```
  > A block quotation (also known as a long quotation or extract) is a quotation in a written document that is set off from the *main* text as a paragraph, or block of text, and typically distinguished visually using indentation and a different typeface or smaller size font. 
```
will produce this:

  > A block quotation (also known as a long quotation or extract) is a quotation in a written document that is set off from the *main* text as a paragraph, or block of text, and typically distinguished visually using indentation and a different typeface or smaller size font. 
  
# Links

There are several options for links. We can link other parts of the document using the document `headers`, we can link to images locally or on the web, and we can link to web sites.

## Linking to a chapter

```
Link to [Emphasis](#emphasis) chapter
Link to [Block quotes](#block-quotes) chapter
```
produces: 

Link to [Emphasis](#emphasis) chapter

Link to [Block quotes](#block-quotes) chapter

Try clicking on the links!
Note: blank spaces in header titles need to replaced with a hyphens, (\-), when linked to.

## Links to images

Link to an image locally. For this example we have an image called `CHL_SEASONAL_ANOMS_2019.png` located in the `figures` folder.


```
![alt txt](figures/CHL_SEASONAL_ANOMS_2019.png "Seasonal anomolies")
```

The text "Seasonal anomolies" is considered the title text and will be seen as mouse over text in markdown and html files (but not pdfs)

This syntax for this line is equivalent to the following html:
```
<img src="figures/CHL_SEASONAL_ANOMS_2019.png" alt="alt txt" title="Seasonal anomolies">
```

![alt txt](figures/CHL_SEASONAL_ANOMS_2019.png  "Seasonal anomolies")

To make this link clickable we just wrap all of this in square brackets and add a link

```
[![alt txt](figures/CHL_SEASONAL_ANOMS_2019.png  "Seasonal anomolies")](https://github.com)
```

[![alt txt](figures/CHL_SEASONAL_ANOMS_2019.png  "Seasonal anomolies")](https://github.com)


Linking to an image on the web uses exacly the same format. Just substitute the path for the image url

```
![alt txt](https://www.mydomaine.com/thmb/h5wgN0JfBGfjnZ5K-BWITEreG0Y=/1880x1410/smart/filters:no_upscale()/GettyImages-108313003-5a9e18f2bfb2431492fa41f5148717ff.jpg "waterfall")
```


![alt txt](https://www.mydomaine.com/thmb/h5wgN0JfBGfjnZ5K-BWITEreG0Y=/1880x1410/smart/filters:no_upscale()/GettyImages-108313003-5a9e18f2bfb2431492fa41f5148717ff.jpg "waterfall")

# Code blocks

We have already used these in the above document. We encompass chunks of code between "fences" These fences are a sequence of 3 back ticks.


\```

For more help in R type ?dplyr

\```

produces:

```
For more help in R type ?dplyr
```

We can also use inline code using a single back tick.

A package i like in R is called \`dplyr\`
produces:

A package i like in R is called `dplyr`

# Strikethroughs

These are used for showing crossed out text. 

```
I ~~dont~~ like ice cream
```
produces:

I ~~dont~~ like ice cream

# Math equations

There are a great deal of options for mathematical equations (Greek letter, subscripts, superscripts, math symbols, fractions etc.). The mathematical typesetting is based on LaTeX. These are not part of the Markdown core specs but diffeent flavors of markdown have support for Equations, for example Rmarkdown. Here is small flavor: (You will need to `knit` in `Rmarkdown` or live preview in `Visual Studio Code` to see the rendered output)

## Inline 

```
The variable $X$ is Normally distributes with mean $\mu$ and stanard deviation $\sigma$.
```
produces:

The variable $X$ is Normally distributes with mean $\mu$ and stanard deviation $\sigma$.

## Centered block

All equations are enclosed between \$$

The Normal distribution can be written as:

```
$$f\left(X,\underline\theta\right) = \frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$$
```

$$f\left(X,\underline\theta\right) = \frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$$


# Tables

Tables can be added using the pipe, ( | ),   symbol to separate columns.

```
|name|occupation|dob|
|---|:---:|---|
|jim|chef|1988-02-22|
|bob|comedian|1966-05-01|

```
produces:

|name|occupation|dob|
|---|:---:|---|
|jim|chef|1988-02-22|
|bob|comedian|1966-05-01|

The use of colons in the spearator line justifies text to the left, right, or centered (as shown above in the middle column)


# Check boxes

```
- [x] checkbox item
- [ ] open box
```

- [x] checkbox item
- [ ] open box
 
# Bibliographies

Using bib files are not part of markdown but extensions in Visual studio code can help with that. They can also be linked to when editing in Rmarkdown.

# HTML

Markdown files can be used in conjuction with cascading style sheets (.css files) and html to create custom layouts, in particular for websites/webpages.
