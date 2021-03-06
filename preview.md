---
menu_item_id: 1
title: Preview
tags: [KAKUREMINO, Licensing]
author: Cedlog
license: "CC0 1.0"
license_url: https://creativecommons.org/publicdomain/zero/1.0/legalcode.txt
---
# Kramdown
This is a preview of some most used **Kramdown** formatting elements.
It is used to preview and compare CSS styles on generated HTML elements.

## Paragraph
A block of text is wrapped in a paragraph (\<p\>).
A new paragraph is generated for every block of text preceded by a blank line.
\\
Two consecutive backslash or space characters generated a line break (\<br\>).

HTML elements: **\<p\>**

## Text formatting
A text can be formatted like examples below but cannot be **underlined** :
* **Bold** (\<strong\>)
* *Italic* (\<em\>)
* ***Bold and Italic*** (\<strong\>\<em\>)
* ~~Strike through~~ (\<del\>)

HTML elements: **\<strong\> \<em\> \<del\>**

## Headers (heading) {#headers-id}
Headers have an auto-generated ID by default but a custom ID can be specified too.
\\
Note: auto-generated ID has been *disabled* for this preview.

# H1 Heading (\<h1\>)
## H2 Heading (\<h2\>)
### H3 Heading (\<h3\>)
#### H4 Heading (\<h4\>)
##### H5 Heading (\<h5\>)
###### H6 Heading (\<h6\>)

HTML elements: **\<h1\> \<h2\> \<h3\> \<h4\> \<h5\> \<h6\>**

## Blockquote
Blockquote content is wrapped in always paragraph (\<p\>).
Kramdown formatting is supported inside a blockquote (\<blockquote\>).

> Keep things simple and ~~stupid~~ quick.

HTML elements: **(\<blockquote\>) (\<p\>)**

## Code (Preformatted text)
A code generates a \<div\> with a class value of <<highlighter-rouge>>.
\\
The \<div\> contains a \<pre\> with a class value of <<highlight>>.
\\
The \<pre\> element contains a \<code\> element which contains the text content of the code.
\\
If a programming language were specified then the text content becomes a sequence of \<span\>.

~~~
/* Example of preformatted text aka *Code* */
if(Math.max(work.duration, fun.duration) > daily.threshold) {
  if(listeners.isEmpty())
    addListener(subconscious);
  schedule(Alerts.WARNING, Messages.THRESHOLD_EXCEEDED);
}
~~~

HTML elements: **\<div\> \<pre\> \<code\> \<span\>**
\\
CSS Classes: **highlighter-rouge highlight**

## Unformatted text (No conversion)
Text can be generated **AS-IS** without any conversion.
\\
\\
{::nomarkdown}
This "text IS NOT wrapped in a paragraph".
It is generated **AS-IS** without any conversion.
{:/}

HTML elements:

## Images

![Image alternate text]({{ site.baseurl }}/favicon.png)

![another image]

[another image]: {{ site.baseurl }}/favicon.png
{: height="70px" width="70px"}

HTML elements: **\<img\>**

## Links
Link examples:

* URL links:
  * [ROOT URL (/)]({{ site.baseurl }}/)
  * [Github](https://github.com/ "Github website")
  * Styled link (color): [Twitter][Twitter URL]
  * Using angle brackets syntax: <email@example.com>
* Links to ID in the same document:
  * [Headers](#headers-id)
  * [Conclusion](#conclusion-id)

[Twitter URL]: https://twitter.com "Twitter website"
{: style="color: #c11"}

HTML elements: **\<a\>**

## Footnotes
A footnote looks like this example[^1].
It has a link (\<a\>) with a class of *footnote* which targets the footnote definition ID.
The link is wrapped in a \<sup\> element which will have an ID of *<<fnref:1>>* here.
The footnote definition will appear **at the end of this document**.

It has a class value of **footnotes** and an ID which will be *<<fn:1>>*.
It has a link (\<a\>) with a class of *reversefootnote* which points back to the footnote ID.

HTML elements: **\<sup\> \<a\>**
\\
CSS Classes: **footnote**

[^1]: This is a footnote definition example.
    All footnote definition are wrapped in one \<div\> with a class of *footnotes*.
    Each definition is a list item (\<li\>) of an unordered list (\<li\>).
    Each list item has an ID which is *<<fnref:1>>* for this example.

    HTML elements: **\<div\> \<ol\> \<li\> \<p\> \<a\>**
    \\
    CSS Classes: **footnotes reversefootnote**

    A **four** spaces indentation is required at the beginning
    of each line of a multi-line footnote definition.
    \\
    The link with a class value of *reversefootnote* which targets to footnote ID is here:

## Lists

**Ordered list (\<ol\>)**
1. Ordered list (Like this list).
  1. Item.
  2. Item.
2. Unordered list.
2. Definition list.

**Unordered list (\<ul\>)**
* Ordered list.
* Unordered list (Like this list).
  * Item.
  * Item.
* Definition list.

**Definition list (\<dl\>)**

Term (\<dt\>)
: A term is an element of the list (\<dl\>). The list is not called a **"term list"** though.
: A term definition like above (\<dd\>).

Another term (which makes the previous text become a term)

: A definition preceded by a blank line is wrapped in a paragraph (like this one).

: Same for this one which is wrapped in a paragraph (\<p\>).

HTML elements: **\<dl\> \<dt\> \<dd\> \<p\>**

## Table
Table **does not support multi-line** text.
Note that each cell of the table footer is actually generated as \<td\> and not as \<th\>.
\\
Also each column can have a specified content alignment which is generated in an inline style.

| Header 1: TR1 / TH1 | Header 1: TR1 / TH2 | Header 1: TR1 / TH3 | Header 1: TR1 / TH4 |
|:-|:-:|:-:|-:|
| Body 1: TR1 / TD1 | Body 1: TR1 / TD2 | Body 1: TR1 / TD3 | Body 1: TR1 / TD4 |
| Body 1: TR2 / TD1 | Body 1: TR2 / TD2 | Body 1: TR2 / TD3 | Body 1: TR2 / TD4 |
|---
| Body 2: TR1 / TD1 | Body 2: TR1 / TD2 | Body 2: TR1 / TD3 | Body 2: TR1 / TD4 |
| Body 2: TR2 / TD1 | Body 2: TR2 / TD2 | Body 2: TR2 / TD3 | Body 2: TR2 / TD4 |
|===
| Footer 1: TR1 / TD1 | Footer 1: TR1 / TD2 | Footer 1: TR1 / TD3 | Footer 1: TR1 / TD4 |

HTML elements: **\<table\> \<thead\> \<tr\> \<th\> \<td\> \<tfooter\>**

## Miscellaneous

### Typographic symbols
Example of available symbols :
* em-dash: ---
* en-dash: --
* Guillemets: << guillemets\\
symbols >>

### Underline text
Alternative solutions to underline text can be one listed below :

Specifying an *inline style attribute or CSS rule*{: style="text-decoration: underline"}.

Wrapping in an HTML <span style="text-decoration: underline; color: #00F;">
"span" element with inline style attribute or CSS rule</span>.

Using the HTML <u>"underline" element</u>.

### Kramdown comment
Kramdown syntax supports comments ie ignore a sequence of Kramdown text.
\\
{::comment}
Putting line break sequence in a new line like above is easier to read !!!
{:/}
Below is a syntax example for commenting Kramdown text :
~~~
{::comment}
Anything here and here will be ignored (Excepted when preformatted like this).
Any closing tag like {:/comment} or {:/sometag} can be replace by {:/} which is an equivalent.
{:/comment}
~~~

### Horizontal line
Three consecutive dash each separated by a space character
will generate an horizontal line (\<hr\>).
\\
The sequence must be preceded by a blank line (Otherwise it is interpreted as a heading).

HTML elements: **\<hr\>**

_ _ _

### Abbreviations
An abbreviation (\<abbr\>) can be defined for a word and it case sensitive. For example WWW.

It will apply on all occurrences of <<WWW>> but not on occurrences of <<www>>.

HTML elements: **\<abbr\>**

## Conclusion
{: id="conclusion-id"}

**Kramdown** has enough formatting features for writing simple documents like blog articles.
\\
The syntax is not difficult and it has some limitations though but it is a nice tool !

*[WWW]: World Wide Web