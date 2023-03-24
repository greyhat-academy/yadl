# YADL
#### "Yet Another Markdown Language"
###### Draft Version 0.0.1a
####
- "YAML in Markdown, but better!"
- "JSON without curly brackets!"
- "Yet Another Dumb Language!"
  - some random person on the Interwebz

## Why?
### Essential Quality of life Changes
### Like [Tabs instead of Spaces](https://www.youtube.com/watch?v=V7PLxL8jIl8)!
- Indentations are done with Tabs 
  - Data is organized in TSV [tab-seperated values] tables 
  - data can be called indirectly 
    - YADL to YAML compiltation is easily possible!

Tabs will be replaced with spaces, because YAML using spaces is just cringe and I'll refuse to do that bullshit!

### Changes compared to Markdown
#### Line Breaks just work, no double spaces at the end.
- Empty lines are easy to do. 
  - Paragraphs are seperated by double empty lines. 
  - Added HTML5 elements
  ```
  <audio	src=./media/sample.ogg	alt=this is a sample audio file>
  <video	src=./media/video.webm	alt=this is a sample video file>
  <image	src=./media/image.webp	alt=this is a sample image file>
  <table	src=./media/table.tsv	alt=this is a sample table>
  <file	src=/media/file.bin	alt=this is a sample binary file>
  ```
  - Easy compilation to HTML5
    - Embedding of files
      - This is seriously disrecommended and instead files should be organized in a relative hierachy like within [ePub](https://en.wikipedia.org/wiki/EPUB) and [Tarballs](https://en.wikipedia.org/wiki/Tar_(computing))!
      ```
      <file "filename" encoding=base64>
      ...
      </file>
      ```
##
### Unique Features
#### Embeddable Text
#### Embeddable Tables
- [tab-seperated values](https://en.wikipedia.org/wiki/Tab-separated_values)
  - inline TSV using
    - ```
      <table "table name" alt=inline table sample>
      ...
      </table>
      ```
- Easy to compile to JSON 
  - Embeddable JSON 
    - Allows for interactive just-in-time requests
      - i.e. Exchange Rates [to be requested via an HTTP-API]
###
#### Diferent Comment Types 
  ```
  ##	Comment to Comment
  #!	Important Comment
  #!!	Very Important Comment
  #?	Further Reading/Research required
  #??	Needs Clarification
  #s	Spoiler
  #t	Tip
  #n	Notes
  #q	Question
  #q!	Important Question
  #a	Answer
  #a!	Important Answer
  #c	<language=bash>	Code
  ```
###
#### Links across protocols
  - ```
    HTTP(S)	<link	src=https://example.com/sample.file>
    FTP(S)	<link	src=ftp://example.com/sample.file>
    IPFS	<link	src=ipfs://...>
    magnet	<link	magnet:...>
    Torrent	<link	torrent://...>
    ```
    - Webseeds, incl. IPFS are supported. 
###
#### Proper Citations & Acknowlegements
  - ```
    Webpage	<cite	src=https://example.com/source.html	Xavier Sample et. al.	Sample Title	Date of Retrieval (optional archive.org snapshot link)>
    Books	<cite	ISBN=...	p:420	l:13	Sample et. al.	Sample Book	1st Edition>
    Mags	<cite	ISSN=...	p:69	l:4		Sample Title	Sample Magazine 23/2022>
    Laws	<cite	Law	§ ...	section ...	sentence ...	x. half sensence	as-of-Date>
    Courts	<cite	Case-ID	Court	page	line	sentence	half sentence	Date>
    Acknowledgements	<ack Name	Date	Reason	Comment	Source>
    ```
###
#### Optional Beautifications for GUI Rendering and Export to HTML & PDF 
- Style Markup 
  - Fonts
  ```
  <font src=/media/ubuntu.otf font-family=ubuntu style=sans-serif>
  ```
    - Fonts are optional.
      - If no fonts are declared, all text has to use monospaced sans-serif [i.e. ubuntu mono]
  - Colour
  ```
  <colour="pink" #ff00ff>
  ```
    - Colours are optional.
      - If no colour is declared, the default will be amber [#FF8000] with green [#00FF00] as alternative colour on black [i.e. #000000] background.


### Encoding
#### UTF-8 per Default
- Other Encodings need to be specified with
	```
    <encoding=encoding>
    ```
    at the
	```
    <header>
    ```
    of the document.
  - Besides [Unicode](https://de.wikipedia.org/wiki/Unicode), only [ASCII](https://en.wikipedia.org/wiki/ASCII) is officially supported, but in theory any encoding is possible, tho it's severily discouraged!

### File Extension & Conventions
#### .yadl file extension
- not used as of the day of writing 
  - Systems that only support 8+3 characters in filenames are all end-of-life and should not be used in any productive way. 
    - .yaml is used by YAML
#### LF Line endings
- OSes that use CRLF are inherently trash or EoL anyways.
#### Date & Time Format 
- Dates and Times are exclusively stored in only two acceptable forms:
  ```
  # Unix Timestamp
  <time=1640991364>
   ```
- Other accepted formats are: YYYYMMDD,hhmmss:TZ - i.e. 
  ```
  20211231,235604:CET
  ```
  - Dates can also be presented as YYYYMMDD,- 
  - Time can also be presented as -,HHMMSS 
  - Unless the Timezone has been specified, it'll be interpreted as [Unixtime](https://en.wikipedia.org/wiki/Unix_time) - (human readable [UTC without leap seconds](https://en.wikipedia.org/wiki/Unix_time#Leap_seconds)).

## License:
This Document is [ licensed under Creative Commons CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

See also [LICENSE.md](./LICENSE.md).