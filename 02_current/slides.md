!SLIDE

# Where we are now #

!SLIDE

# Think AOL vs. CompuServe vs. local ISPs #
# _not IE/Netscape_ #

!SLIDE bullets incremental

# Common formats #

* HTML
* ePub
* Mobipocket (Kindle, various mobile devices)
* PDF (desktop systems)

!SLIDE bullets incremental

# Which format(s) should I use? #

* ePub
* HTML

!SLIDE

# Questions? #

!SLIDE 

# What is ePub? #

!SLIDE bullets incremental

# ePub format #

* XHTML + CSS + image files
* Open Packaging Format (OPF) metadata
* ZIP archive + container
* ...
* That's it!

!SLIDE

# OPF metadata

!SLIDE code

<div style="font-size: 18pt;">
&lt;?xml version=&quot;1.0&quot;?&gt;
&lt;package version=&quot;2.0&quot; 
 xmlns=&quot;http://www.idpf.org/2007/opf&quot; unique-identifier=&quot;BookId&quot;&gt;
 
 &lt;metadata xmlns:dc=&quot;http://purl.org/dc/elements/1.1/&quot; 
  xmlns:opf=&quot;http://www.idpf.org/2007/opf&quot;&gt;
  &lt;dc:title&gt;Pride and Prejudice&lt;/dc:title&gt;
  &lt;dc:language&gt;en&lt;/dc:language&gt;
  &lt;dc:identifier id=&quot;BookId&quot; opf:scheme=&quot;ISBN&quot;&gt;123456789X&lt;/dc:identifier&gt;
   &lt;dc:creator opf:file-as=&quot;Austen, Jane&quot; 
    opf:role=&quot;aut&quot;&gt;Jane Austen&lt;/dc:creator&gt;
 &lt;/metadata&gt;
 
 &lt;manifest&gt;
  &lt;item id=&quot;chapter1&quot; href=&quot;chapter1.xhtml&quot; 
   media-type=&quot;application/xhtml+xml&quot;/&gt;
  &lt;item id=&quot;stylesheet&quot; href=&quot;style.css&quot; 
   media-type=&quot;text/css&quot;/&gt;
  &lt;item id=&quot;ch1-pic&quot; href=&quot;ch1-pic.png&quot; 
   media-type=&quot;image/png&quot;/&gt;
  &lt;item id=&quot;myfont&quot; href=&quot;css/myfont.otf&quot; 
   media-type=&quot;application/x-font-opentype&quot;/&gt;
  &lt;item id=&quot;ncx&quot; href=&quot;book.ncx&quot; 
   media-type=&quot;application/x-dtbncx+xml&quot;/&gt;
 &lt;/manifest&gt;
 
&lt;/package&gt;
</div>

!SLIDE

# ZIP archive

!SLIDE code

<div style="font-size: 24pt;">
mimetype
META-INF/
  container.xml
OPS/
  book.opf
  chapter1.xhtml
  cover.png
  css/
    book.css
    font.otf
</div>

!SLIDE code

# container.xml #

<div style="font-size: 22pt;">
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot; ?&gt;
&lt;container version=&quot;1.0&quot; 
 xmlns=&quot;urn:oasis:names:tc:opendocument:xmlns:container&quot;&gt;
  &lt;rootfiles&gt;
    &lt;rootfile full-path=&quot;OPS/book.opf&quot; 
     media-type=&quot;application/oebps-package+xml&quot;/&gt;
  &lt;/rootfiles&gt;
&lt;/container&gt;
</div>

!SLIDE bullets incremental

# Open Source ePub tools #

## epub-tools ##
## [http://code.google.com/p/epub-tools/](http://code.google.com/p/epub-tools/) ##

* Conversion from Word, DocBook, and other formats to ePub
* Validation, pure-HTML preview tools

!SLIDE bullets incremental

# Open Source ePub tools, cont. #

## Bookworm ##
## [http://code.google.com/p/threepress/](http://code.google.com/p/threepress/)

* Django web application for reading ePub books online via a computer or mobile device

!SLIDE bullets

# Open Source ePub tools, cont. #

## Calibre ##

* Cross-platform GUI e-book conversion app
* Manages e-book library, provides sync server
