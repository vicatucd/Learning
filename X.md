# Markdown Syntax
***
{{TOC}}
***

Markdown text is stored in plaintext files with a *.md* or other *.MarkdownExtension.*

## Annotations
- *Italics* refer file names and file paths.
- `code` 
- **Terms** 
- \[placeholder\]

# Basics
***
## Headings
Input:
```	
		# Heading Level 1  
		## Heading Level 2  
		### Heading Level 3  
		#### Heading Level 4  
		##### Heading Level 5  
```

## Horizontal Rules
To create a horizontal rule, use three or more asterisks (`***`), dashes (`---`), or underscore (`___`) on a line by themselves.  
Input:
```
		***
		---
		___
```
***
## Paragraphs Structures
### Line Breaks
2 spaces at the end of a sentence.
### Paragraphs
1 blank line between paragraphs
### Single Line Blockquote
`>` in front of a sentence. 
Input:
```
		> Indented text here
```
### Multiline Blockquotes
`>` in front of each line in the blockquote. 
Input:
```
		> Indented lines here...
		> ... continues here   
```
### Nested Blockquotes
Add an extra `>` in front of each line to nest the line below the previous line.   
Input:
```
		> Main Topic
		>> Sub Topic
```
***
## Font
### Bold/Emphasis
`**` or `__` in front and at the end of the text that is to be bolded.   
Input:
```
		**text here**   
```
### Italic/Important
`*` or `_` in front and at the end of the text that is to be bolded.   
Input:
```
		*text here* or _text here_   
```
### Bold and Italic
`***` or `___` in front and at the end of the text that is to be bolded.    
Input:
```
		***text here*** OR ____text here____
```

***

## Listed Items
### Ordered List
Add "\[\#\]. " in front of each item.  
Input:
```
		1. First item
		2. Second item
		3. ...etc.
```
### Nested Ordered List
Add 4 spaces and "\[\#\]. " in front of each item below the item it is to be nested.  
Input:
```
		1. First item
		2. Second item
			1. First subitem 
			2. Second subitem
```
### Unordered List
Add dashes (-), asterisks (*), or plus signs (+) in front of each list item.   
Input:
```
		- Item 1
		+ Item 2
		* Item 3
```
### Adding Elements in List
To add another element in a list while preserving the continuity of the list, indent the element four spaces or one tab. 

#### Adding Paragraphs
Input:
```
		- Some list item
		- Another list item
				Text in line with list, but not bulleted or numbered
		- More list items
```
Output:  
- Some list item.  
- Another list item.    
	Text in line with list, but not bulleted or numbered.  
- More list items.  

#### Adding Blockquotes
Input:
```
		- Some list item
		- Another list item
				> Text in line with list, but not bulleted or numbered
		- More list items
```
Output:   
- Some list item.  
- Another list item.  
	>Text in line with list, but not bulleted or numbered.  
- More list items
#### Adding Code Blocks
Code blocks are normally indented four spaces or one tab. When they're in a list, indent them eight space or two tabs.   
Input: 
```
		* Some list item
		* Another list item
		
				Tex
		* More list items
``` 
Output:  
* Some list item.    
	* Another list item.     

				Code text here  
	* More list items    
#### Adding Images
		* Some list item
		* Another list item
	
				![Image Title Here](images/filename.png)
		* More list items
		
---
## Code
To denote a word or phrase as code, enclose it in tick marks (\`).

		This is a single `word` of code
This is a single `word` of code

### Escaping Tick Marks
If the word of phrase you want to denote as code includes one or more tick marks, you can escape it by enlcosing the word or phrase in double tick marks (\`‌\`)

### Code Blocks
To create code blocks, indent every line of the block by at least four spaces or one tab.
```
		This  
		Is  
		A  
		Code  
		Block 
```
### Fenced Code Blocks
Depending on your Markdown processor or editor, you'll use three tick marks (\'\'\') or three tilde (\~\~\~) on the lines before and after the code block, without the need of indening the code block.
Input:   
~~~
This  
is a  
Code  
Block
~~~
### Code Block Syntax Highlighting
~~~python
A = 1
while A < 5,
	A += 1
~~~ 
### URL & Email Links
To create a link, enclose the link text in brackets (eg. [Google]) and then follow it immediately with the URL in parenthesis (eg. (google.com))
Input:
```
		[Google](google.com)
```
[Google](http://www.google.com)
### Links with Titles
You can optionally add a title for a link. This will appear as a tooltip when the user hovers over the link. To add a title, enclose it in parenthesis after the URL. 
Input:
```
		[Google](google.com)
```
[Google](http://www.google.com "My search engine!")
### URLs and Email Addresses
To quickly turn a URL or email address into a link, enlcose it in angle brackets.
Input:
```
		<google.com>
		<username@domain.com>
```	
Output: 
<google.com>  
<username@domain.com>

### Formatting Links
To emphasize links, add asterisks before and after the brackets and parenthesis. 
Input:
```
		***[Google](google.com)***
```
Output:	
***[Google](google.com)***

### Reference-style Links (Footnotes)
Reference-style links are constructed in two parts: the part you keep inline with your text and the part you store somewhere else in the file to keep the text easy to read. 
#### Formating the First Part of the Link
The first part of a reference-style link is formatted with two sets of brackets. The first set of brackets surrounds the text taht should appear linked. The second set of brackets displays a label used to point to the link you're storing elsewhere in your document. 
		
		[anchor][ID#]
		
[anchor][1]

#### Formatting the Second Part of the Link
The second part of a reference-style link is formatted with the following attributes: 

1. The label, in brackets, followed immediately by a colon and at least one space (e.g., [label]: ).
2. The URL for the link, which you can optionally enclose in angle brackets. 
3. The optional title for the link, which you can enclose in double quotes, single quotes, or parenthesis. 

		[anchor]: google.com "my search engine"

Use [Google](google.com "my search engine") to search the internet. 

Use [Google][1] to search the internet. 
### Footnotes
When you create a footnote, a superscript number with a link appears where you added the footnote reference. To create a footnote reference, add a caret and an identifier inside brackets ([^1]). Indentifiers can be numbers or words, but they can't contain spaces or tabs. Identifiers only correlate the footnote reference with the footnote itself - in the output, footnotes are numbered sequentially. 
This is a footnote[^1].

[^1]: Reference for 1st footnote

## Images
To add an image, add an exclamation mark(!), followed by alt text in brackets, and the path or URL to the image asset in parentheses. You can optionally add a title after the URL in the parenthesis. 

		![Alt text for image](images/filename.png "image title")

## Escaping Characters
To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash(\) in front of the character. 
**Characters You Can Escape**

Character | Name
-----|-----
\\|backslash
\'|tickmark
\*|asterisk
\_|underscore
\{}|curly brackets
\[]|brackets
\()|parenthesis
\#|pound sign
\+|plus sign
\-|minus sign
\.|dot
\!|exclamation

## Tables
To add a table, use three or more hyphens (---) to create each column's header, and use pipes (|) to seperate each column. You can optionally add pipes on either end of the table. 

		col1 | col2
		--- | ---
		item1 | itema
		item2 | itemb

### Alighn table content
Col1 | Col2 | Col 3
:--- | :---: | ---:
Left | Center | Right


[1]: <google.com> "Google"



