+++
author = "Elias Fahssi"
title = "XML, TEI, and the Digitization of Text"
date = "2023-06-19"
description = "Exploring the transformative power of XML and TEI in the field of digital humanities"
tags = [
    "technology",
    "medieval",
    "humanities",
]
thumbnail = "images/markup.png"
+++
  
## Introduction
  
The summer after discovering Middle English and medieval studies, I was lucky to sit in a directed reading course focused on palaeography, or the study of old writing systems. Before the invention of the printing press, handwriting was the norm. Now imagine the many languages and cultures across 14th century Europe. Now consider that our concept of a modern alphabet, with its standard letters and fixed order, was not yet fully formed. In the medieval world, there was no fixed style of writing. Instead, there were many different *scripts*, each a stylistic embodiment of the culture and the time. A script was akin to an expression of aesthetic, intellectual, and culture values, used to convey different languages across the contintent.  

Consider the precise strokes of the Caroline minuscule, or the robust and angular forms of the Gothic Textura:

{{< figure src="/images/caroline.jpg" caption="*Caroline minuscule, a script characterized by its clear, round forms and the careful spacing of words, was developed during the Carolingian Renaissance, serving as a pivotal force in standardizing writing practices across Europe.*  [Source](https://en.wikipedia.org/wiki/Carolingian_minuscule)">}}

{{< figure src="/images/gothic.jpg" caption="*Gothic Textura, a script prevalent in the High and Late Middle Ages, is distinguished by its vertical and angular letterforms, creating a dense and rhythmic visual texture reminiscent of woven fabric.*  [Source](https://en.wikipedia.org/wiki/Blackletter)">}}


At its core, I learned to appreciate the dischotomy between a "text" and a "document": the former being the sequence of symbols that creates meaning, and the latter their physical embodiment in the material world. We'd often look at the same text, a poem for example, across multiple different documents, each with their own layout, script, and origin story.

My exploration of these concepts led me to appreciate the immense value of two linked technologies focused on markup: XML and TEI -- digital tools capable of capturing and digitally representing texts and documents.
  
## Part I: A Brief History of Markup and XML
  
The concept of markup has its roots in the traditional publishing industry. Editors and typesetters would annotate manuscripts with instructions for typesetting, essentially 'marking up' the text. As we moved from physical print to digital documents, the concept evolved into what we now know as the Standard Generalized Markup Language (SGML). This early digital markup language, established in the 1980s, was comprehensive but complex - a digital reflection of the heavily annotated manuscripts of yesteryears.
  
SGML's intricacies paved the way for the development of XML (eXtensible Markup Language). XML, developed by the World Wide Web Consortium (W3C) in the late 1990s, took the core concepts of SGML and simplified them. It stripped away some of the complexity, aiming to create a standard that was both powerful and easy to use. The result was a more flexible and accessible way to define the structure and data within a document.
  
## Part II: The Evolution and Impact of TEI
  
While XML provided the means to markup and structure data, it was the Text Encoding Initiative (TEI) that brought it to life in the humanities. Introduced in 1987, TEI offered a standardized set of guidelines for encoding machine-readable texts, particularly within the humanities and social sciences.
  
TEI represented a significant expansion of the scope of XML, specifically tailored to meet the diverse needs of textual scholars. It allowed for the encoding of complex textual phenomena often found in scholarly texts, such as revisions, deletions, additions, and marginalia – aspects that are often collectively referred to as 'paratext'.
  
For instance, consider a simple modern letter:

```xml
<TEI xmlns="http://www.tei-c.org/ns/1.0">
  <teiHeader>
    <fileDesc>
      <titleStmt>
        <title>A Brief Letter</title>
      </titleStmt>
      <publicationStmt>
        <p>Unpublished</p>
      </publicationStmt>
      <sourceDesc>
        <p>Written by John Doe</p>
      </sourceDesc>
    </fileDesc>
  </teiHeader>
  <text>
    <body>
      <div type="letter">
        <opener>
          <salute>Dear Jane,</salute>
        </opener>
        <p>I hope this letter finds you well.</p>
        <closer>
          <salute>Yours sincerely,</salute>
          <signed><persName>John</persName></signed>
        </closer>
      </div>
    </body>
  </text>
</TEI>
```

And a basic encoding of a scene from Shakespeare's "Romeo and Juliet" might look like:

```xml
<TEI xmlns="http://www.tei-c.org/ns/1.0">
  <teiHeader>
    <fileDesc>
      <titleStmt>
        <title>Romeo and Juliet, Act 2, Scene 2</title>
      </titleStmt>
      <publicationStmt>
        <p>William Shakespeare</p>
      </publicationStmt>
    </fileDesc>
  </teiHeader>
  <text>
    <body>
      <div type="play">
        <div type="act">
          <head>Act 2</head>
          <div type="scene">
            <head>Scene 2</head>
            <sp>
              <speaker>Juliet</speaker>
              <l>O Romeo, Romeo! wherefore art thou Romeo?</l>
            </sp>
            <sp>
              <speaker>Romeo</speaker>
              <l>It is my lady, O, it is my love!</l>
            </sp>
          </div>
        </div>
      </div>
    </body>
  </text>
</TEI>
```

Got it??!!!