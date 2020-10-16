---
permalink: /
title: "Opening Books and the National Corpus of Graduate Research"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

## ABSTRACT

Virginia Tech University Libraries, in collaboration with Virginia Tech Computer Science and Old Dominion University Computer Science, will bring computational access to book-length documents, through a research and piloting effort employing Electronic Theses and Dissertations (ETDs). The library and archives fields lack research on extracting and analyzing segments of long documents (chapters, reference lists, tables, figures), as well as methods for summarizing individual chapters of longer texts to enable findability. The project brings cutting-edge computer science and machine learning technologies to advance discovery, use, and potential for reuse of the knowledge hidden in the text of books and book-length documents. By focusing on libraries' ETD collections, the research will enhance libraries' ETD programs, devising effective and efficient methods for opening the knowledge currently hidden in the rich body of graduate research and scholarship.

The project is divided broadly into three research areas. 
* RA 1: Document analysis and extraction
* RA 2: Adding value
* RA 3: User services

### Research Area 1
Research Area 1 attempts to answer the research question "How can we effectively identify and extract key parts (chapters, sections, tables, fgures, citations),in both born digital and page image formats?"

To answer the research question, we divide the work into tasks that we want to accomplish.
* Task 1: Compiling ETD sample
* Task 2: Building ground truth for ETD segmentation and extraction
* Task 3: Researching on ETD segmentation and extraction models

### Research Area 2
Research Area 2 attempts to answer the research question "HHow can we develop e￿ective automatic classi￿cation as well as chapter summarization techniques?". 

The tasks that will help us accomplish the goals are 

* Task 4: Building ground truth for ETD (chapters) topical classification
* Task 5: Building topical classi￿cation models for ETDs and their chapters
* Task 6: Building ground truth for ETD chapters summarization
* Task 7: Researching on summarization models for ETD chapters

### Research Area 3
Research Area 3 attempts to answer the research question "How can our ETD digital library most e￿ectively serve stakeholders?" We primarily focus on investigating new ways to interact with ETD collections,and study which best support the needs of the user community.


* Name a file ".md" to have it render in markdown, name it ".html" to render in HTML.
* Go to the [commit list](https://github.com/academicpages/academicpages.github.io/commits/master) (on your repo) to find the last version Github built with Jekyll. 
  * Green check: successful build
  * Orange circle: building
  * Red X: error
  * No icon: not built

## Resources
 * [Liquid syntax guide](https://shopify.github.io/liquid/tags/control-flow/)

## Markdown guide

### Header three

#### Header four

##### Header five

###### Header six

## Blockquotes

Single line blockquote:

> Quotes are cool.

## Tables

### Table 1

| Entry            | Item   |                                                              |
| --------         | ------ | ------------------------------------------------------------ |
| [John Doe](#)    | 2016   | Description of the item in the list                          |
| [Jane Doe](#)    | 2019   | Description of the item in the list                          |
| [Doe Doe](#)     | 2022   | Description of the item in the list                          |

### Table 2

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|-----------------------------|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=============================|
| Foot1   | Foot2   | Foot3   |

## Definition Lists

Definition List Title
:   Definition list division.

Startup
:   A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.

#dowork
:   Coined by Rob Dyrdek and his personal body guard Christopher "Big Black" Boykins, "Do Work" works as a self motivator, to motivating your friends.

Do It Live
:   I'll let Bill O'Reilly [explain](https://www.youtube.com/watch?v=O_HyZ5aW76c "We'll Do It Live") this one.

## Unordered Lists (Nested)

  * List item one 
      * List item one 
          * List item one
          * List item two
          * List item three
          * List item four
      * List item two
      * List item three
      * List item four
  * List item two
  * List item three
  * List item four

## Ordered List (Nested)

  1. List item one 
      1. List item one 
          1. List item one
          2. List item two
          3. List item three
          4. List item four
      2. List item two
      3. List item three
      4. List item four
  2. List item two
  3. List item three
  4. List item four

## Buttons

Make any link standout more when applying the `.btn` class.

## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}

## HTML Tags

### Address Tag

<address>
  1 Infinite Loop<br /> Cupertino, CA 95014<br /> United States
</address>

### Anchor Tag (aka. Link)

This is an example of a [link](http://github.com "Github").

### Abbreviation Tag

The abbreviation CSS stands for "Cascading Style Sheets".

*[CSS]: Cascading Style Sheets

### Cite Tag

"Code is poetry." ---<cite>Automattic</cite>

### Code Tag

You will learn later on in these tests that `word-wrap: break-word;` will be your best friend.

### Strike Tag

This tag will let you <strike>strikeout text</strike>.

### Emphasize Tag

The emphasize tag should _italicize_ text.

### Insert Tag

This tag should denote <ins>inserted</ins> text.

### Keyboard Tag

This scarcely known tag emulates <kbd>keyboard text</kbd>, which is usually styled like the `<code>` tag.

### Preformatted Tag

This tag styles large blocks of code.

<pre>
.post-title {
  margin: 0 0 5px;
  font-weight: bold;
  font-size: 38px;
  line-height: 1.2;
  and here's a line of some really, really, really, really long text, just to see how the PRE tag handles it and to find out how it overflows;
}
</pre>

### Quote Tag

<q>Developers, developers, developers&#8230;</q> &#8211;Steve Ballmer

### Strong Tag

This tag shows **bold text**.

### Subscript Tag

Getting our science styling on with H<sub>2</sub>O, which should push the "2" down.

### Superscript Tag

Still sticking with science and Isaac Newton's E = MC<sup>2</sup>, which should lift the 2 up.

### Variable Tag

This allows you to denote <var>variables</var>.
