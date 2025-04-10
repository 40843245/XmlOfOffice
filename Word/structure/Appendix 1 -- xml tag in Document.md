# Appendix 1 -- xml tag in Document.md
## Prequisite
To have a better understanding of a list of tags in OOXML, it's better to be familiar with these basic knowledgement or concepts before looking at these articles.

+ concept of layout, style, headings etc that will be used in a Document.
+ commonly used terms. (Some advanced terms can be reviewed at this article -- `Prequisite Review 1 -- terms`[^1] )
+ commonly used tags (and theire attributes) in native html5 and native xml.
+ concepts of namespace, class in OO (Object-Oriented) design pattern.
+ concepts of `Part and Relationship in OOXML`[^4].

## Suggestion
Here is my suggestion to reader.

**NEVER cram these tags in OOXML into your brain (死記，沒理解就硬塞東西)**. Otherwise, you may got stuck on this.

Just understand these commonly used tags in OOXML then remember (理解在記住) it.

For those uncommonly used tags and attribute, **search it when you need it**. 

After all, it only lists some tags and its attribute in OOXML. 

It's like a dictionary, search it when you want to know a vocabulary.

## tables
> [!WARNING]
> Most content of these table are refered from Google Gemini's answer or from non-official website, which BOTH may be incorrect.
>
> Read with caution.

### processing instruction
See `Appendix 1 -- tags in xml`[^3]

But in OOXML, there are many ways added to process a file that will be parse with OOXML preprocessor.

I just list some of them that commonly seen in Word file.

| target of the processing instruction | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `mso-application` | | targets Microsoft Office applications. | | |

#### attributes in `mso-application`
| attributes name | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `progid` | *Pr*ogrammatic *Id*entifier | It's a string that uniquely identifies a COM (Component Object Model) component or application. | | |

#### examples and explanation
##### example 1
`Docx1.docx` file

```
<?mso-application progid="Word.Document"?>
```

In above example, we can know that

+ `Docx1.docx` file targets to Microsoft Office.
+ it is a Document.
+ Thus, it targets to Microsoft Office Word and you can open it with Microsoft Office Word.

### namespace declaration in xml tag 
| namespace in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `xmlns` | | xml namespace | declare a namespace in xml. Or configure the property in xml (such as `xmlns:aml`) | | |

### namespace under `xmlns` namespace
| namespace under `xmlns` namespace | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `aml` | *A*nnotation *M*arkup *L*anguage | used for comments and revisions. | | |
| `a` | *A*nnotation | specifies which core DrawingML elements will be used for graphical objects. | | |
| `w` | *W*ordProcessingML | assign a value to it determine which WordprocessingML elements is used. | | |
| `w14` | *W*ordProcessingML | assign a value to it determine which WordprocessingML (with version id 14) elements is used. | | |
| `w15` | *W*ordProcessingML | assign a value to it determine which WordprocessingML (with version id 15) elements is used. | | |
| `w16cid` | *W*ordProcessingML *C*ontent *Id*entifiers | assign a value to it determine which Content Identifiers of WordprocessingML (with version id 16) elements is used. | | |
| `w16se` | *W*ordProcessingML *S*ymbol *E*xtensibility | assign a value to it determine which Symbol Extensibility of WordprocessingML (with version id 16) elements is used. | | |
| `wpg` | *W*ordProcessingML *G*rouping  | assign a value to it determine which Symbol Extensibility of WordprocessingML Grouping is used. | | |
| `wpi` | *W*ordProcessingML *I*nk  | assign a value to it determine which Symbol Extensibility of WordprocessingML Ink is used. | At intial release of WordprocessingML Ink (in Microsoft Office 2010), its namespace is named as `wpi` but it is named as `aink` at later release. | |
| `wps` | *W*ord*P*rocessing *S*hapes | assign a value to it determine which Wordprocessing Shapes is used. | | |
| `wp` | *W*ord*P*rocessing | assign a value to it determine which WordProcessing is used. | | |
| `wp14` | *W*ord*P*rocessing version id 14 | assign a value to it determine which WordProcessing with version id 14 is used. | | |
| `wpc` | *W*ord*P*rocessing *C*anvas | assign a value to it determine which WordProcessing Canvas is used, WordProcessing Canvas is for drawing and layout within the Word document (particularly newer drawing features). | | |
| `c` | *C*harts | specific which `DrawingML Charting Schema` is used. It is used for defining properties for charts. | | |
| `cx` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (main extension) is used. | | |
| `cx1` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 1) is used. | | |
| `cx2` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 2) is used. | | |
| `cx3` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 3) is used. | | |
| `cx4` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 4) is used. | | |
| `cx5` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 5) is used. | | |
| `cx6` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 6) is used. | | |
| `cx7` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 7) is used. | | |
| `cx8` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 8) is used. | | |
| `aink` | Ink | specific which `DrawingML Ink Schema` is used. It is used for defining properties for inks, provide Digital Ink Support, and provide DrawingML Integration  | | |
| `am3d` | *M*odel *3D* | specific which `DrawingML 3D Model Schema` is used. It is used for defining properties for 3D model, embed 3D models, and provide DrawingML Integration  | | |
| `dt` | *D*ata *T*ypes | often used for properties or values within the document. | | |
| `mc` | *Markup* *C*ompatibility | determine which version of documents are allowed to be able to be compatible with different versions of Office Open XML. | | |
| `ve` | *Markup* *C*ompatibility | Same as above | a convention of `mc` in `~/word/document.xml` file under a Office Word file | |
| `o` | *O*ffice | it is for Office-specific elements, often related to general Office document properties. | | | 
| `v` | *V*ector Markup Language | it is for Vector Markup Language, which is a legacy format for vector graphics in Office documents. | | |
| `w10` | *W*ord *10*-specific elements | it is for Word 10-specific elements, indicating features or settings from that version. | | |
| `w` | *W*ord 2003 elements | it is the primary namespace for Word 2003 XML. | reason about why it is for Word 203 XML see following history. | |
| `wx` | *W*ord 2003 Au*x*iliary Hints | it is for Word 2003 Auxiliary Hints, which might contain additional information for specific Word features. | The word `Auxiliary` has a meaning of the word `Extension`, but its usage of the word `Auxiliary` is narrower and more concise than that of the word `Extension`, and we usually abbreviates the word `Extension` to `X`. And I guess this is the reason why the namespace is declared as `wx`. | |
| `wne`| WNE | it points to elements from which version (according to the value of `xmlns:wne`). Its presence suggests potential compatibility features or elements used across versions. | See `WNE class`[^5] for more details. | | 
| `wsp` | *W*ord *S*ervice *P*ack | This namespace might relate to Word xxx (version according to value of `xmlns:wsp` ) Service Pack 2 specific elements or extensions. | | | 
| `sl` | *S*chema *L*ibrary | This namespace could be for a Schema Library, possibly related to document templates or components. | | | 
| `r` | *R*elationship | it specifies which relationship will be used. | | | 
| `m` | *M*ath | it specifies which tools about math (its functionalities contain `Equation`) will be used. | | | 
| `ignorable` | ignorable | it specifies which namespace declaration in this tag will be ignored. | it must be string, seperated by exactly one space. (To represent that many of them will be ignored.) | | 

> [!NOTE]
> History of Office and OOXML.
>
> + In year 2000, Microsoft released Microsoft Office 2000 which is the intial release that uses XML tag.
>
> + In year 2003, Microsoft released Microsoft Office 2003 which is the intial release that uses XML tag cooperate with OOXML,
> 
> making the Office file in cross-platform (before that, to view the Office file or access it, you must use Office products which is developed by Microsoft)
>
> and more sharable.

#### examples and explanation
##### example 1
`Docx1.docx` file.

```
<w:wordDocument xmlns:aml="http://schemas.microsoft.com/aml/2001/core" xmlns:wpc="http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas" xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882" xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006" xmlns:o="urn:schemas-microsoft-com:office:office" xmlns:v="urn:schemas-microsoft-com:vml" xmlns:w10="urn:schemas-microsoft-com:office:word" xmlns:w="http://schemas.microsoft.com/office/word/2003/wordml" xmlns:wx="http://schemas.microsoft.com/office/word/2003/auxHint" xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml" xmlns:wsp="http://schemas.microsoft.com/office/word/2003/wordml/sp2" xmlns:sl="http://schemas.microsoft.com/schemaLibrary/2003/core" w:macrosPresent="no" w:embeddedObjPresent="no" w:ocxPresent="no" xml:space="preserve">
```

In above example, we can know that

+ The tag is a root node in an Office Word file.
+ In `xmlns:aml="http://schemas.microsoft.com/aml/2001/core"`, its *A*nnotation *M*arkup *L*anguage refers the url `http://schemas.microsoft.com/aml/2001/core`.
+ In `xmlns:wpc="http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas"`, it uses the url `http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas` as WordProcessing Canvas.
+ In `xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"`, its data type is UUID where its UUID is `C2F41010-65B3-11d1-A29F-00AA00C14882`.
+ In `xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006`, for markup language, it is compatible with version 2006 or above.
+ In `xmlns:o="urn:schemas-microsoft-com:office:office"`, it declares a namespace named `o` and alias the namespace `urn:schemas-microsoft-com:office:office` as `o`.
+ In `xmlns:v="urn:schemas-microsoft-com:vml"`, its Vector Markup Language uses `urn:schemas-microsoft-com:vml`
+ In `xmlns:w10="urn:schemas-microsoft-com:office:word`, its Word 10-specific elements targets to the namespace `urn:schemas-microsoft-com:office:word`.
+ In `xmlns:w="http://schemas.microsoft.com/office/word/2003/wordml"`, its Word 2003 elements targets to the url `http://schemas.microsoft.com/office/word/2003/wordml`.
+ In `xmlns:wx="http://schemas.microsoft.com/office/word/2003/auxHint"`, its Word 2003 Auxiliary Hints targets to the url `http://schemas.microsoft.com/office/word/2003/auxHint`, simply said, it uses `http://schemas.microsoft.com/office/word/2003/auxHint` as an extension for Word 2003 elements.
+ In `xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml"`, its wne targets to the url `http://schemas.microsoft.com/office/word/2006/wordml`.
+ In `xmlns:wsp="http://schemas.microsoft.com/office/word/2003/wordml/sp2"`, its Word Service Pack targets to the url `http://schemas.microsoft.com/office/word/2003/wordml/sp2`, and its Word Service Pack uses version 2003.
+ In `xmlns:sl="http://schemas.microsoft.com/schemaLibrary/2003/core"`, its Schema Library targets to the url `http://schemas.microsoft.com/schemaLibrary/2003/core` and the Word file uses Schema Library in version 2003.
+ In `w:macrosPresent="no"`, the Word file does NOT execute the macros (written in VBA or VB)
+ In `w:embeddedObjPresent="no"`, the Word file does NOT embed object.
+ In `w:ocxPresent="no"`, the Word file does NOT use Active Control.
+ In `xml:space="preserve"`, the Word file does fully preserve the space.

##### example 2
`~/word/document.xml` file under `Docx1.docx` file.

```
<w:document
    xmlns:ve="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:o="urn:schemas-microsoft-com:office:office"
    xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"
    xmlns:m="http://schemas.openxmlformats.org/officeDocument/2006/math"
    xmlns:v="urn:schemas-microsoft-com:vml"
    xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"
    xmlns:w10="urn:schemas-microsoft-com:office:word"
    xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"
    xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml"
    xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"
    xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart"
    xmlns:wpc="http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas"
    xmlns:cx="http://schemas.microsoft.com/office/drawing/2014/chartex"
    xmlns:cx1="http://schemas.microsoft.com/office/drawing/2015/9/8/chartex"
    xmlns:cx2="http://schemas.microsoft.com/office/drawing/2015/10/21/chartex"
    xmlns:cx3="http://schemas.microsoft.com/office/drawing/2016/5/9/chartex"
    xmlns:cx4="http://schemas.microsoft.com/office/drawing/2016/5/10/chartex"
    xmlns:cx5="http://schemas.microsoft.com/office/drawing/2016/5/11/chartex"
    xmlns:cx6="http://schemas.microsoft.com/office/drawing/2016/5/12/chartex"
    xmlns:cx7="http://schemas.microsoft.com/office/drawing/2016/5/13/chartex"
    xmlns:cx8="http://schemas.microsoft.com/office/drawing/2016/5/14/chartex"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:aink="http://schemas.microsoft.com/office/drawing/2016/ink"
    xmlns:am3d="http://schemas.microsoft.com/office/drawing/2017/model3d"
    xmlns:wp14="http://schemas.microsoft.com/office/word/2010/wordprocessingDrawing"
    xmlns:w14="http://schemas.microsoft.com/office/word/2010/wordml"
    xmlns:w15="http://schemas.microsoft.com/office/word/2012/wordml"
    xmlns:w16cid="http://schemas.microsoft.com/office/word/2016/wordml/cid"
    xmlns:w16se="http://schemas.microsoft.com/office/word/2015/wordml/symex"
    xmlns:wpg="http://schemas.microsoft.com/office/word/2010/wordprocessingGroup"
    xmlns:wpi="http://schemas.microsoft.com/office/word/2010/wordprocessingInk"
    xmlns:wps="http://schemas.microsoft.com/office/word/2010/wordprocessingShape"
    mc:Ignorable="w14 w15 w16se w16cid wp14">
</w:document>
```

In above example, we can know that

+ In `<w:document>` tag, we define a document and configure metedata about the `Docx1.docx` file.
+ In `xmlns:ve="http://schemas.openxmlformats.org/markup-compatibility/2006"`, `ve` is a convention of `mc` namespace. This namespace indicates that markup compatibility targets to the url `http://schemas.openxmlformats.org/markup-compatibility/2006"`, indicating that it is compatible with markup language released in 2006.
+ In `xmlns:o="urn:schemas-microsoft-com:office:office"`, it targets to `urn:schemas-microsoft-com:office:office`
, indicating the office refers to Microsoft Office. 
+ In `xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"`, it targets to the namespace `http://schemas.openxmlformats.org/officeDocument/2006/relationships`, indicating the relationship targets to `http://schemas.openxmlformats.org/officeDocument/2006/relationships` (in version Office 2006).
+ In `xmlns:m="http://schemas.openxmlformats.org/officeDocument/2006/math"`, it targets to `http://schemas.openxmlformats.org/officeDocument/2006/math`, indicating that it refers to math tool in version Office 2006.
+ In `xmlns:v="urn:schemas-microsoft-com:vml"`, it targets to `urn:schemas-microsoft-com:vml`, indicating the vml refers to vml developed by Microsoft.
+ In `xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"`, it targets to `http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing`, indicating that it refers WordprocessingML Drawing in version Office 2006.
+ In `xmlns:w10="urn:schemas-microsoft-com:office:word"`, it targets to `urn:schemas-microsoft-com:office:word`, indicating that it is Word-10 specific.
+ In `xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"`, it targets to `http://schemas.openxmlformats.org/wordprocessingml/2006/main`, indicating that its main functionality of WordProcessingML refers to that in version Office 2006.
+ In `xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml"`, it targets to `http://schemas.microsoft.com/office/word/2006/wordml`, indicating that its WNE refers to WordML in version Office 2006.
+ In `xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"`, it targets to `http://schemas.openxmlformats.org/drawingml/2006/main`, indicating that its DrawingML refers to that in version Office 2006.
+ In `xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart"`, it targets to `http://schemas.openxmlformats.org/drawingml/2006/chart`, indicating that the chart refers that in version Office 2006.
+ In `xmlns:wpc="http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas"`, it targets to `http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas`, indicating that the WordProcessing Canvas refers that in version Office 2006.
+ In `xmlns:cx="http://schemas.microsoft.com/office/drawing/2014/chartex"`, it indicates the extension of chart package (with highest preceedence) refers to the release at 2014 from Microsoft Office.
+ In `xmlns:cx1="http://schemas.microsoft.com/office/drawing/2015/9/8/chartex"`, it indicates the extension of chart package refers to the release at 2015/09/08 from Microsoft Office.
+ In `xmlns:cx2="http://schemas.microsoft.com/office/drawing/2015/10/21/chartex"`, it indicates the extension of chart package refers to the release at 2015/10/21 from Microsoft Office.
+ In `xmlns:cx3="http://schemas.microsoft.com/office/drawing/2016/5/9/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/9 from Microsoft Office.
+ In `xmlns:cx4="http://schemas.microsoft.com/office/drawing/2016/5/10/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/10 from Microsoft Office.
+ In `xmlns:cx5="http://schemas.microsoft.com/office/drawing/2016/5/11/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/10 from Microsoft Office.
+ In `xmlns:cx6="http://schemas.microsoft.com/office/drawing/2016/5/12/chartex"` , it indicates the extension of chart package refers to the release at 2016/5/12 from Microsoft Office.
+ In `xmlns:cx7="http://schemas.microsoft.com/office/drawing/2016/5/13/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/13 from Microsoft Office.
+ In `xmlns:cx8="http://schemas.microsoft.com/office/drawing/2016/5/14/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/14 from Microsoft Office.
+ In `xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"`, its other convention is `ve`. But it has higher preceedence.
+ In `xmlns:aink="http://schemas.microsoft.com/office/drawing/2016/ink"`, it targets to `http://schemas.microsoft.com/office/drawing/2016/ink`, indicating that the Drawing ink refers that in version Office 2016.
+ In `xmlns:am3d="http://schemas.microsoft.com/office/drawing/2017/model3d"`, it targets to `http://schemas.microsoft.com/office/drawing/2017/model3d`, indicating that the 3D Model Drawing refers that in version Office 2017.
+ In `xmlns:wp14="http://schemas.microsoft.com/office/word/2010/wordprocessingDrawing"`, it targets to `http://schemas.microsoft.com/office/word/2010/wordprocessingDrawing`, indicating that, for Office 2014 ,WordProcessing Drawing refers that in version Office 2010.
+ In `xmlns:w14="http://schemas.microsoft.com/office/word/2010/wordml"`, it targets to `http://schemas.microsoft.com/office/word/2010/wordml`, indicating that, for Office 2014, WordProcessingML refers that in version Office 2017.
+ In `xmlns:w15="http://schemas.microsoft.com/office/word/2012/wordml"`, it targets to `http://schemas.microsoft.com/office/word/2012/wordml`, indicating that, for Office 2015, WordProcessingML refers that in version Office 2012.
+ In `xmlns:w16cid="http://schemas.microsoft.com/office/word/2016/wordml/cid"`, it targets to `http://schemas.microsoft.com/office/word/2016/wordml/cid`, indicating that, for Office 2016, WordProcessingML Content Identifiers refers that in version Office 2016.
+ In `xmlns:w16se="http://schemas.microsoft.com/office/word/2015/wordml/symex"`, it targets to `http://schemas.microsoft.com/office/word/2016/wordml/cid`, indicating that, for Office 2015, WordProcessingML Symbol Extensibility refers that in version Office 2015.
+ In `xmlns:wpg="http://schemas.microsoft.com/office/word/2010/wordprocessingGroup"`, it targets to `http://schemas.microsoft.com/office/word/2016/wordml/cid`, indicating that WordProcessingML Grouping refers that in version Office 2010.
+ In `xmlns:wpi="http://schemas.microsoft.com/office/word/2010/wordprocessingInk"`, `wpi` is an old alternative name of `aink`. But it has lower preceedence.
+ In `xmlns:wps="http://schemas.microsoft.com/office/word/2010/wordprocessingShape"`,  it targets to `http://schemas.microsoft.com/office/word/2010/wordprocessingShape`, indicating that WordProcessingML Shapes refers that in version Office 2010.
+ In `mc:Ignorable="w14 w15 w16se w16cid wp14"`, it ignores the following namespace in this tag.</br>`xmlns:w14`</br>`xmlns:w15`</br>`xmlns:w16se`</br>`xmlns:w16cid`</br>`xmlns:wp14`.
  
### namespace in xml tag in OOXML
| namespace in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w` | | Microsoft Word | indicates that it describes xml content of a Microsoft Word file.| w stands for Microsoft *W*ord | |

### namespace declared in `<w:wordDocument>`
You can know which namespaces in `xmlns` namespace are declared through finding `xmlns` in `<w:wordDocument>`.

| namespace in xml tag | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `o` | *O*ffice-specific namespace | it contains metadata about the Word document itself. | | |

### namespace and its attribute in OOXML
#### about `xmlns` namespace
##### attribute in `xmlns` namespace
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `xmlns:space` | | space | assign a value to determine how to deal with whitespace (i.e. ` `, `\t`,`\n`).

#### about `xml` namespace
##### attribute in `xml` namespace
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `xml:space` | | space | assign a value to determine how to deal with whitespace (i.e. ` `, `\t`,`\n`).

#### about `v` namespace
##### attribute in `v` namespace
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `v:ext` | | | specifies editing behavior for shapes created with these defaults. | | |

### element and its attribute in xml tag in OOXML
#### about `o` namespace
`o` namespace contains metadata about the Word document itself.

##### elements in `o` namespace
| element in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<o:DocumentProperties>` | | document property | defines a property for the document itself. | | |
| `<o:Subject>` | | document subject | configures the subject of the document itself. | | |
| `<o:Author>` | | document author | configures the author of the document itself. | | |
| `<o:Keywords>` | | document keywords | configures keywords or tags associated with the document itself. | | |
| `<o:Description>` | | document description | configures the description of the document itself. | | |
| `<o:LastAuthor>` | | last saved author | configures the author who saved the document itself recently. | | |
| `<o:Revision>` | | document revision number | configures the revision number of the document itself recently. | | |
| `<o:TotalTime>` | | total time | stores the total time spent on the document itself. | | |
| `<o:LastPrinted>` | | last printed date and time | stores the date and time of last print to the document itself. | | |
| `<o:Created>` | | created date and time | stores the date and time the document was created. | | |
| `<o:LastSaved>` | | last saved date and time | stores the date and time the document was last saved. | | |
| `<o:Company>` | | company | stores the company or organization associated with the document. | | |
| `<o:Manager>` | | manager | stores the manager or responsible person for the document. | | |
| `<o:Category>` | | category | stores the category of the document. | | |
| `<o:PresentationFormat>` | | Presentation Format | The format used when saving as a presentation. | | |
| `<o:Bytes>` | | bytes | estimated of the document size in bytes. | | |
| `<o:Words>` | | words | estimated of the number of words in the document. | | |
| `<o:Characters>` | | characters | estimated of the number of characters in the document. | excluding spaces. | |
| `<o:CharactersWithSpaces>` | | characters | estimated of the number of characters in the document. | including spaces. | |
| `<o:Lines>` | | lines | estimated of the number of lines in the document. | | |
| `<o:Paragraphs>` | | paragraphs | estimated of the number of paragraphs in the document. | | |
| `<o:Version>` | | version | The version number of the application that created the document. | | |
| `<o:GUID>` | | Guid | Guid of the document. | | |
| `<o:HyperlinkBase>` | | base of hyperlink | The base path or URL for hyperlinks within the document. | | |
| `<o:Slides>` | | slides | estimated of the number of slides in the Slide. | (Potentially for PowerPoint documents etc embedded in Word) | |
| `<o:HiddenSlides>` | | notes | estimated of the number of hidden slides in the document. | (Potentially for PowerPoint documents etc embedded in Word) | |
| `<o:Notes>` | | notes | estimated of the number of notes in the document. | (Potentially for notes in the document). | |
| `<o:MMClips>` | | *M*utli*m*edia clips | estimated of the number of mutlimedia clips in the document. | (Potentially for embededded mutlimedia in the document). | |
| | | | | | |
| `<o:shapedefaults/>` | | | specifies the default properties for newly created shapes within a drawing canvas. | | |
| `<o:shapelayout>`| | | acts a container that holds information about how shapes are laid out and interact with the surrounding text. | | |
| `<o:idmap/>` | | | defines the map id. | | |

##### attribute about `o` namespace
###### attribute in `<o:shapedefaults>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `v:ext` | | | | explained in ``attribute in `v` namespace`` section | |
| `spidmax` | | max *s*ha*p*e *id* | sets the maximum Shape ID that can be assigned to new shapes created within the current drawing canvas. | 

###### attribute in `<o:shapelayout>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `v:ext` | | | | explained in ``attribute in `v` namespace`` section | |

###### attribute in `<o:idmap>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `v:ext` | | | | explained in ``attribute in `v` namespace`` section | |
| `data` | | | specifies the current shape ID. | The id of newly create shape will be value of `data` attribute plus one. | |

##### examples and explanation
###### example 1
`Docx1.docx` file.

```
<o:DocumentProperties>
   <o:Title>Docx1</o:Title>
   <o:Author>40843245</o:Author>
   <o:LastAuthor>40843245</o:LastAuthor>
   <o:Revision>2</o:Revision>
   <o:TotalTime>0</o:TotalTime>
   <o:LastPrinted>2016-06-13T09:16:00Z</o:LastPrinted>
   <o:Created>2016-12-13T04:53:00Z</o:Created>
   <o:LastSaved>2016-12-13T04:53:00Z</o:LastSaved>
   <o:Pages>1</o:Pages>
   <o:Words>70</o:Words>
   <o:Characters>405</o:Characters>
   <o:Company>NFU</o:Company>
   <o:Lines>3</o:Lines>
   <o:Paragraphs>1</o:Paragraphs>
   <o:CharactersWithSpaces>474</o:CharactersWithSpaces>
   <o:Version>15</o:Version>
</o:DocumentProperties>
```

In above example, we can know that

+ To look at `<o:DocumentProperties>` tag, it contains metadata about `Docx1.docx` file.
+ In `<o:Title>Docx1</o:Title>`, its title is `Docx1`.
+ In `<o:Author>40843245</o:Author>`, the author of document when it is created is `40843245`.
+ In `<o:LastAuthor>40843245</o:LastAuthor>`, the author who last modifies it is `40843245`.
+ In `<o:Revision>2</o:Revision>`, its revision number is 2.
+ In `<o:TotalTime>0</o:TotalTime>`, the last modifies spent 0 minutes (or less than 1 minute) on this file
+ In `<o:LastPrinted>2016-06-13T09:16:00Z</o:LastPrinted>`, it will not be printed after `2016-06-13 09:16:00` UTC Time Zone.
+ In `<o:Created>2016-12-13T04:53:00Z</o:Created>`, someone creates this file at `2016-12-13 04:53:00` UTC Time Zone.
+ In `<o:LastSaved>2016-12-13T04:53:00Z</o:LastSaved>`, this file is saved at `2016-12-13 04:53:00` UTC Time Zone.
+ In `<o:Pages>1</o:Pages>`, this file has one page.
+ In `<o:Words>70</o:Words>`, this file contains exactly 70 words.
+ In `<o:Characters>405</o:Characters>`, this file contains exactly 405 characters (excluding space).
+ In `<o:Company>NFU</o:Company>`, this file is create by orginization NFU. Simply said, someone creates this file with Microsoft Office Word where its Microsoft Office product is registered by NFU.
+ In `<o:Lines>3</o:Lines>`, Office Word estimates this file has three lines.
+ In `<o:Paragraphs>1</o:Paragraphs>`, Office Word estimates this file has one paragraph.
+ In `<o:CharactersWithSpaces>474</o:CharactersWithSpaces>` Office Word estimates this file has 474 characters (including space).
+ In `<o:Version>15</o:Version>`, this file is created with Microsoft Office 2015. Here the version number 15 suggests version 2015.
   
#### about `w` namespace
##### elements in `w` namespace
| element in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| | | | | | |
| `<w:settings>` | | setting | it serves as a container for a wide range of document-level settings and properties that control how the Word document behaves and is displayed. | it usually resides in `~/word/setting.xml` file under a Office Word file. | |
| `<w:zoom>` | | zoom | specifies the display zoom level for the document when it is opened in Microsoft Word. | same as above| |
| `<w:characterSpacingControl>` | | character spacing controlls | specifies how to adjust the spacing between characters. | |
| `<w:compat/>` | | compatibility | it is a container element that holds various compatibility settings designed to ensure the document is displayed and behaves as expected across different versions of Microsoft Word. | | |
| | | | | | |
| `<w:rsids>` | | *r*evision *s*ave *id*entifier*s* | it is a container of revision save identifiers element (`<w:rsid>`, `<w:rsidRoot>`) | | |
| `<w:rsidRoot>` | | *r*evision *s*ave *id*entifiers baseline | establishes a revision save identifiers baseline for current editing session or the most recent save operation that affected the main content of the document. | | |
| `<w:rsid>` | | *r*evi*s*ion save | establishes a revision save identifier. | | |
| | | | | | |
| `<w:wordDocument>` | `<html>` | root node | the root node of a Microsoft Word file. | | |
| `<w:document>` | `<html>` | root node | the root node of **`~/word/document.xml`** file under a Microsoft Word file. | | |
| `<w:ignoreSubtree>` | | ignore a specific subtree | it instructs the Word processor to ignore a specific subtree of the XML document (according to the value of `w:val` attribute) during processing. | | | 
| `<w:body>` | `<body>` | body | the main part of file in native xml (and native html5) | | |
| `<w:lang>` | `<lang>` | language | the language for characters | lang stands for *lang*uage | |
| `<w:charset>` | `<charset>` in native html5 | charset | configure charset of this font | | |
| `<w:family>` | | family | configure family of this font | | |
| `<w:pitch>` | | character's pitch | configure pitch of characters that uses this font. | | | 
| `<w:defaultFont>` | | configure the default font | | |
| `<w:font>` | font in native css | define a font | | |
| `<w:sig>` | | digital signature | encapsulate the digital signature of this font. | | | 
| `<w:panose1>` | | panose | configure the panose (with highest priority) | The lower number is it, the higher priority it has. | |
| `<w:altName>` | `alt` attribute in `<img>` tag in native html5 | alternative | use the alternative (according to the value specified in `w:val` attribute) **when** an element (such as an image) or things that used in an element (such as font) **can not be used or worked correctly**. | | |
| | | | | | | | 
| `<w:p>` | `<p>` | paragraph | A paragraph | notice that if an end-user only inputs an whitespace in .docx file, it will have `<w:p>` tag, the article `docx格式文档详解：xml解析并用html还原`[^4] says this situation. | 
| `<w:pStyle>` | | paragraph style | applies style (according to value of `w:val` attribute) to paragraph (that is inside `<w:p>` tag) | the style to apply is defined in `~/word/style.xml` file | |
| `<w:pPr>` | | paragraph property | property of a paragraph (that is inside `<w:p>` tag) in Microsoft Word file | Pr stands for *Pr*operty | |
| `<w:ind>` | | paragraph indentation | configure the indentation for this paragraph. | ind stands for *ind*entation | |
| | | | | | | | 
| `<w:b/>` | `<b>` and `<b/>` in native html5 | bold | determine the text is bold | | |
| `<w:spacing>` | spacing | settings about spacing between paragraphs | | |
| `<w:jc>` | | justification | settings about justification (alignment) of the paragraph | jc stands for *j*ustifi*c*ation | |
| | | | | | | | 
| `<w:r>` | | run | defines a run in Word | r stands for run | |
| | | | | | | | 
| `<w:rPr>` | | run property | configure property of a run (that is inside `<w:r>` tag) | | |
| `<w:rFonts>`| | run fonts | configure fonts of a run (that is inside `<w:rPr>` tag) | |
| | | | | | | | 
| `<w:sz>` | | size | defines a font size for standard characters (that is inside `<w:rPr>` tag) |  |
| `<w:szCs>` | | size | defines a font size for complex script characters (that is inside `<w:rPr>` tag) | Cs stands for *C*omplex *s*cript | |
| | | | | | | | 
| `<w:tbl>` | `<table>` | table | a table in Microsoft Word file | tbl stands for table | |
| `<w:tblPr>` | | table property | configure property (such as style and appearance) of a table (that is inside `<w:tbl>` tag) in Microsoft Word file | | |
| `<w:tblGrid>` | `<tr>` (first occurence) | table grid | defines a grid (header) of a table in Microsoft Word file | you can think of a grid like a header row ( consists of lots of columns ) in table | |
| `<w:gridCol>` | `<th>` | table grid column | defines a cell in a grid of a table in Microsoft Word file | | it must be inside `<w:tblGrid>` tag. Otherwise, the Word file is corrupted. |
| `<w:tr>`| `<tr>` | table row | a row of a table | t stands for *t*able, r stands *r*ow | |
| `<w:tc>` | `<td>` | table cell | an cell of a table | c stands for *c*ell | |
| `<w:tcW>` | | table cell width | determines the width of the cell of a table | W stands for *w*idth | |
| `<w:tcPr>` | | table cell property | configure property of a table cell (that is inside `<w:tc>` tag) | including width and grid span | |
| `<w:tblStyle>` | | table style | applies style (according to value of `w:val` attribute) to paragraph (that is inside `<w:tbl>` tag) | the style to apply is defined in `~/word/style.xml` file | |
| | | | | | | | 
| `<w:sectPr>` | | sect property | configure property of a sect | sect stands for section | |
| `<w:pgSz>` | | page size | configures a page size (that is inside `<w:sectPr>` tag) | pg stands for *p*a*g*e | |
| `<w:pgMar>` | | page margin | configures a page margin (that is inside `<w:sectPr>` tag) | Mar stands for *Mar*gin | |
| `<w:col>` | | columns in section | add columns in section (that is inside `<w:sectPr>` tag) | | |
| `<w:docGrid>` | | document grid | add document grid (that is inside `<w:sectPr>` tag) | | |
| | | | | | | | 
| `<w:tabs>` | | | acts like a container of tab stops (`<w:tab>`) | you may see one or more `<w:tab>` tag inside `<w:tabs>` tag. | | 
| `<w:defaultTabStop>` | | tab | define property of the default tab stop by assign the value to its attributes. | | | 
| `<w:tab>` | | tab | define property of a tab stop by assign the value to its attributes. | | | 
| | | | | | | | 
| `<w:bookmarkStart>` | | bookmark start | defines a bookmark with start point | | One `<w:bookmarkStart>` tag must match one `<w:bookmarkEnd>` tag. Otherwise, the file is corrupted. | 
| `<w:bookmarkEnd>` | | bookmark end | defines a bookmark with end point to enclose a bookmark | | Same as above | 
| | | | | | | | 
| `<w:lists>` | | | acts like a container of a list (`<w:list>`) | | |
| `<w:numbering>` | | numbering | It acts as a container for numbering definitions, which are then referenced by paragraphs to apply specific list styles. | | |
| `<w:listDef>` | | list definition | defines a list with specific id for style | | |
| `<w:lsid>` | | list style id | assign the value of `w:val` attribute to id of list style to determine which style will be used | the id is defined in `~/word/style.xml` | |
| `<w:lvl>` | | list level | defines a level of list | lvl stands for *l*e*v*e*l* | |
| `<w:plt>` | | picture list type (exactly to say, list pattern type in modern version of Word) | it describes the complexity or structure of the list definition | | |   
| `<w:tmpl>` | | template | it configure the what template will be used | <ol><li>tmpl stands for *t*e*mpl*ate</li><li>It accords to value of `W:val` attribute.</li><li>The template that will be used must be prefined (usually is predefined in `~/word/style.xml` or `~/word/template.xml`</li></ol> | | 
| `<w:start>` | | start | configure starting value for the numbering sequence at this list level | | It's only relevant when the <w:numFmt> (number format) for this level is set to a numbering style (like decimal, upperRoman, lowerLetter, etc.). |
| `<w:numFmt>` | | number formatting | determines whether this level uses numbers or bullets, and the specific style  | | |
| `<w:bullet>` | | bullet formatting | same above | | |
| `<w:numPr>` | | number property | configure the property if it7 uses number formatting.  | | |
| `<w:suff>` | | suffix | specifies what character (if any) follows the number (e.g., a period, a hyphen, or a tab) | | |
| `<w:lvlText>` | | level text | defines the numbering format using placeholders (e.g., "%1." for first-level numbers) | | |
| `<w:lvlJc>` | | level justification | configures the justification of this level | | | 
| `<w:nfc>` | | Number Formatting Code | configures Number Formatting Code of this level | nfc stands for *N*umber *F*ormatting *C*ode | | 
| | | | | | | | 
| `<w:bdr>` | `border` in css | border | configures properties of the border. | | |
| `<w:pgBorders>` | | page border | configures properties of the borders of page. | | |
| `<w:top>` | | top | configures properties of top borders of some elements (according to this tag is inside what tag). | | |
| `<w:left>` | | left | configures properties of left borders of some elements (according to this tag is inside what tag). | | |
| `<w:bottom>` | | bottom | configures properties of bottom borders of some elements (according to this tag is inside what tag). | | |
| `<w:right>` | | right | configures properties of right borders of some elements (according to this tag is inside what tag). | | |
| `<w:displayBackgroundShape/>` | | | determines if the background shape is display or not | | | 
| `<w:themeFontLang/>`| | | specifies the language settings for the theme fonts used in a Microsoft Word document. | | | 
| `<w:clrSchemeMapping/>` | | | clear the settings of scheme mapping table, then configures the properties of scheme mapping table for document role. | | |
| | | | | | | | 
| `<w:shapeDefaults>` | | | acts like an container containing default properties for newly created drawing shapes within a Microsoft Word document. | It usually resides in `~/word/settings.xml` under a Word file. | |
| | | | | | | | 
| `<w:decimalSymbol/>` | | | explicitly specifies the decimal separator (by given value of `w:val` attribute) for numbers within the document. | | |
| `<w:listSeparator/>` | | | explicitly specifies the list separator (by given value of `w:val` attribute) for list within the document. | It is used when there are many items. | |
| | | | | | | | 
| `<w:docDefaults>` | | | serves as a container for defining the default formatting properties for the entire document. | | |
| `<w:rPrDefault>` | | | defines the default formatting properties for all text runs within the document. | | |
| `<w:pPrDefault/>` | | | defines the default formatting properties for all paragraphs in the document. | | |
| `<w:latentStyles> | | | servers as a container for defining the latent styles (i.e. current unused styles). | | |
| `<w:lsdException>` | | LSD exception | defines exceptions to the default behavior of LSD (Linked Style Definitions). | | |


##### attribute about `w` namespace
###### attribute in `<w:zoom>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:percentage` | | percentage | which zoom level should be when the document is displayed. | | must be a string contains positive number. |

###### attribute in `<w:characterSpacingControl>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | percentage | determines how to adjust characters between spaces. | | |

> [!IMPORTANT]
> The available value of `w:val` attribute in `<w:characterSpacingControl>` is defined in [Character-Level Whitespace Compression Settings](https://c-rex.net/samples/ooxml/e1/Part4/OOXML_P4_DOCX_ST_CharacterSpacing_topic_ID0E6AK2.html)

###### attribute in `<w:rsid>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | specifies a Guid as a revision save identifier. | | |

###### attribute in `<w:word>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:macrosPresent` | | macro to present or not | assign a value to determine it will use macro (written in VBA or VB).</br>If it is specified to "yes", it will use macro.</br>Otherwise, it will not use macro. | | |
| `w:embeddedObjPresent` | | embedded object to present or not | assign a value to determine whether the document contains embedded objects (like Excel spreadsheets or other OLE objects). | | |
| `w:ocxPresent` | | OCX controls to present or not | assign a value to determine whether the document will use OCX controls (i.e. ActiveX controls) | | |  

###### attribute in `<w:font>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:name` | | name | assign a value to give the name to this font. | | |

###### attribute in `<w:family>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | value | assign a value to determine which family will be used for those text that uses this font. | | |

###### attribute in `<w:charset>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | value | assign a value to determine which charset will be used for those text that uses this font. | | |

###### attribute in `<w:pitch>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | value | assign a value to determine which how many pitches will be used for those text that uses this font. | | |

###### attribute in `<w:defaultFonts>`
Same as attribute in `<w:rFonts>`.

###### attribute in `<w:p>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:rsidR` | | revision id for run | assign the value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidRDefault` | | revision id for run default | assign the default value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidSect` | | revision id for section | assign the default value of revision id for section | rs stands for *r*evi*s*ion | |

###### attribute in `<w:ind>`
> [!CAUTION]
> I highly NOT recommend that specify BOTH `w:first-line` and `w:hanging` attribute.
>
> The Google Gemini says that
>
>> If both `w:first-line` and` w:hanging` are specified, `w:hanging` is usually ignored.

> [!CAUTION]
> Similarly, I highly NOT recommend that specify BOTH `w:first-line-chars` and `w:hanging-chars` attribute.
>
> The Google Gemini says that
>
>> If both `w:first-line-chars` and` w:hanging-chars` are specified, `w:hanging-chars` is usually ignored.

> [!NOTE]
> I list some common used attributes.
>
> For `<w:ind>` tag and its attributes, see the [DocumentFormat.OpenXml.Wordprocessing.Indentation class (MSDS API reference)](https://learn.microsoft.com/en-us/dotnet/api/documentformat.openxml.wordprocessing.indentation?view=openxml-3.0.1)

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:left-chars` | | left indentation, characters unit | assign an positive value to specify left indentation of the paragraph, measured in character units. | it is measured with its unit -- default character | it is deprecated, but not obsolete. At Microsoft Office 2019, it can recongize this attribute |
| `w:left` | | left indentation | assign an positive value to specify left indentation of the paragraph, measured in twips.  | its unit is twips | same as above |
| `w:start-chars` | | start indentation, characters | assign an positive integer to specify left indentation of the paragraph, measured in character units. | it has meaning of `w:left-chars` attribute | However, it is implemented in later version of OOXML standard (ECMA-376, 2011), so Microsoft Word 2007 may not recognize this attribute. |
| `w:start` | | start indentation | assign an positive value to specify start indentation of the paragraph, measured in twips.  |  it has meaning of `w:left` attribute | same as above |
| `w:right-chars` | | right indentation, characters unit | assign an positive integer to specify right indentation of the paragraph, measured in character units. | it is measured with its unit -- default character | it is deprecated, but not obsolete. At Microsoft Office 2019, it can recongize this attribute |
| `w:right` | | right indentation | assign an positive value to specify right indentation of the paragraph, measured in twips.  | its unit is twips | same as above |
| `w:end-chars` | | end indentation, characters unit | assign an positive value to specify end indentation of the paragraph, measured in character units. | it has meaning of `w:right-chars` attribute | However, it is implemented in later version of OOXML standard (ECMA-376, 2011), so Microsoft Word 2007 may not recognize this attribute. |
| `w:end` | | end indentation | assign an positive value to specify end indentation of the paragraph, measured in twips.  |  it has meaning of `w:right` attribute | same as above |
| `w:hang-chars` | | hang indentation, characters unit | assign an positive integer to specify hang indentation of the paragraph, measured in character units. | <ol><li>it is measured with its unit -- default character</li><li>For explanation about the term hang indentation, see `Appendix 4 -- terms`[^3]</li></ol>| |
| `w:hanging` | | hanging indentation | assign an positive value to specify hanging indentation of the paragraph, measured in twips.  | its unit is twips | |
| `w:first-line-chars` | | first-line indentation, characters unit | assign an value to specify first-line indentation of the paragraph, measured in twips.  | it is measured with its unit -- default character | It can be negative value, but when it is a negative value, there are some different effects.</br>See following cases.</br>Case 1:</br>When speficies a positive value, it indents the first line further to the right than the rest of the paragraph.</br>Case 2:</br>When specifics a negative value, it creates a `hanging indent` effect where the first line starts to the left of the subsequent lines. |
| `w:first-line` | | first-line indentation | assign an value to specify first-line indentation of the paragraph, measured in twips.  | its unit is twips |
same as above |
| `w:mirrorIndents` | | mirror indentation | the indentation should be mirrored.</br>Specifying to `"false"` indicates that the indentation will not be mirrored.</br>Otherwise, specifying to `"true"` indicates that it will be indented.</br>Default value is `"false"`. | | |

##### attribute in `<w:r>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:rsidR` | | revision id for run | assign the value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidRDefault` | | revision id for run default | assign the default value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidSect` | | revision id for section | assign the default value of revision id for section | rs stands for *r*evi*s*ion | |

###### attribute in `<w:tab>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines alignment or behavior of the tab stop. | This attribute is required. | |
| `w:pos` | | | determines position of the tab stop. | This attribute is required. | |
| `w:leader` | | leader character | determines leader character that will fill the space before the tab stop.  | This attribute is optional. | |

###### attribute in `<w:defaultTabStop>`
Same as attribute in `<w:tab>`.

###### attribute in `<w:sz>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `value` in native html5 | assign the value to determine default font size for **non-complex script characters** (that is inside `<w:pPr>` tag) | its unit is half-point. | |

###### attribute in `<w:szCs>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `value` in native html5 | assign the value to determine default font size for **complex script characters** (that is inside `<w:pPr>` tag) | its unit is half-point. | |

###### attribute in `<w:pgSz>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:w` | `width` in css | assign the value to determine width of page size (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:h` | `height` in css | assign the value to determine height of page size (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |

###### attribute in `<w:pgMar>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:top` | `margin-top` in css | margin-top |assign the value to determine top of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:right` | `margin-right` in css | margin-right | assign the value to determine right of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:bottom` | `margin-bottom` in css | margin-bottom | assign the value to determine bottom of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:left` | `margin-left` in css | margin-left | assign the value to determine left of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:header` | | header | assign the value to determine the distance from the top edge to the header (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:footer` | | footer | assign the value to determine the distance from the bottom edge to the footer (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:gutter` | | footer | assign the value to determine gutter margin (for binding) | its unit is twips (twentieths of a point). | |

###### attribute in `<w:cols>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:space | | space | assign an value to determine the space between columns in section (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |

###### attribute in `<w:docGrid>`
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:linePitch | | vertical spacing | assign an value to determine the vertical spacing between grid lines in section (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| w:charSpace | | horizontal spacing | assign an value to determine horizontal spacing between grid lines in section (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| w:type | | type of document grid | assign an value to determine the type of document grid will be used in section (that is inside `<w:sectPr>` tag) | See `Appendix 2`[^2] for more information | |
| w:lineGrid | | number of line per grid | assign an value to determine number of line per grid in section (that is inside `<w:sectPr>` tag) | | its value must be positive number. |

###### attribute in `<w:tbW>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:w | | width | assign an value to determine the width of the cell (that is inside `<w:tc>` tag) | NOTES that its unit is not necessary twips (its unit is according to value of `w:type` attribute. See next record | |
| w:type | | type | assign an value to determine its unit | | |

###### attribute in `<w:pStyle>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign an Guid as value that determines what style of 7the paragraph (that is inside `<w:p>` tag) will apply to | | |

###### attribute in `<w:tblStyle>`
Way to parsing it is similar to parsing `<w:pStyle>`.

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign an Guid as value that determines what style of the table (that is inside `<w:tbl>` tag) will apply to | | |

###### attribute in `<w:lsid>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign an Guid as value that determines what style of the list (that is inside `<w:listDef>` tag) will apply to | | |

###### attribute in `<w:bookmarkStart>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | `id` in native html5 | id of start point of bookmark | assign the id of start point of bookmark that in the tag | | |
| `w:name` | `name` in native html5 | name of start point of bookmark | assign the name of start point of bookmark that in the tag | | |

###### attribute in `<w:bookmarkEnd>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | `id` in native html5 | id of end point of bookmark | assign the id of end point of bookmark that in the tag | | | 

###### attribute in `<w:listDef>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:listDefId` | | list definition id | specify the unique id when defines a list to determine which style will be used. | | |

###### attribute in `<w:plt>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the Guid as value to determine which style will be applied to for the list pattern type | | |

###### attribute in `<w:tmpl>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the Guid as value to determine which template will be applied to for the list pattern type | | |

###### attribute in `<w:lvl>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:ilvl` | | | specifies indentation of this level | | it must be a positive integer |

###### attribute in `<w:start>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the positive integer as value to determine which the first item will be numbered to | the first item will use number or letter or bullet accords to value of `w:val` attribute in `<w:numFmt>` | it must be a positive integer |

###### attribute in `<w:lvlText>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the string as value to specify the format for this level | | |

###### attribute in `<w:lvlJc>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the string as value to determine the alignment for this level | | |

###### attribute in `<w:bdr>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `style` attribute in tag in native html5 | style | specifies the style of the border. | It is required. | | 
| `w:sz` | | size | specifies thickness or size of the border line | It is required. | | 
| `wx:bdrwidth` | `border-width` in css | *b*or*d*e*r* width | specifies border width. | Observe name of namespace -- `wx`, we can know its used in Word 2003-specific extension.</br>So this tag is available on Word that can the extension -- Word 2003-specific extension.</br> Use alternative `w:sz` instead. | | 
| `w:space` | | space | specifies spacing of border. | It is required. | | 
| `w:color` | color in css | color | specifies color of the border. | It is required. | |
| `w:themeColor` | | theme color | specifies theme color of the border. | It is optional.</br>There are default value. | |
| `w:themeTint` | | theme tint | specifies theme tint of the border. | It is optional.</br>There are default value. | |
| `w:themeShade` | | theme shade | specifies theme shade of the border. | It is optional.</br>There are default value. | |
| `w:frame` | | frame | determines the border should have frame effect. | It is optional.</br>Default value is `"false"`. | |
| `w:shadow` | | shadow | determines the border should have shadow effect. | It is optional.</br>Default value is `"false"`. | |

> [!NOTE]
> For introduction of frame effect, see [frame effect.md](https://github.com/40843245/CSS/blob/main/terms/frame%20effect.md)

> [!NOTE]
> For introduction of shadow effect, see [shadow effect.md](https://github.com/40843245/CSS/blob/main/terms/shadow%20effect.md)

###### attribute in `<w:pgBorders>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:display` | | display | specifies on which pages within the section the page border should be displayed. | It is optional | | 
| `w:offsetFrom` | | offeset from | determines how the page border's position is calculated relative to the page. | It is optional | |  
| `w:zOrder` | | z order | whether the page border should be rendered in front of or behind the document content. | | |

###### attribute in `<w:displayBackgroundShape>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines to display the background shape or not | | |

###### attribute in `<w:themeFontLang>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | specifies a language code to determines which language will be used, for complex script language, when the theme fonts are applied. | | |
| `w:bidi` | | | specifies a language code to determines which language will be used, for bi-directional language (such as Arabic or Hebrew) , when the theme fonts are applied. | | |

###### attribute in `<w:clrSchemeMapping>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:bg1` | | background color 1 | specifics background color 1 in scheme mapping table. | | | 
| `w:bg2` | | background color 2 | specifics background color 2  in scheme mapping table. | | | 
| `w:t1` | | text color 1 | specifics text color 1 in scheme mapping table. | | | 
| `w:t2` | | text color 2 | specifics text color 2 in scheme mapping table. | | | 
| `w:accent1` | | accent color 1 | specifics accent color 1 in scheme mapping table. | | | 
| `w:accent2` | | accent color 2 | specifics accent color 2 in scheme mapping table. | | | 
| `w:accent3` | | accent color 3 | specifics accent color 3 in scheme mapping table. | | | 
| `w:accent4` | | accent color 4 | specifics accent color 4 in scheme mapping table. | | | 
| `w:accent5` | | accent color 5 | specifics accent color 5 in scheme mapping table. | | | 
| `w:accent6` | | accent color 6 | specifics accent color 6 in scheme mapping table. | | | 
| `w:hyperlink` | | hyperlink | specifics hyperlink in scheme mapping table. | | | 
| `w:followedHyperlink` | | followedHyperlink  | specifics followed hyperlink in scheme mapping table. | | | 

For more informations and details, see [DocumentFormat.OpenXml.Wordprocessing.ColorSchemeMapping Class (MSDS API reference)](https://learn.microsoft.com/en-us/dotnet/api/documentformat.openxml.wordprocessing.colorschememapping?view=openxml-3.0.1)

###### attribute in `<w:latentStyles>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:default` | | | determined whether latent styles are enabled by default for the document. | | |
| `w:count` | | | an integer indicating the total number of latent styles defined within this element. | | |
| `w:defLockedState` | | | specifies the default locked state for new latent styles. | | |
| `w:defUIPriority` | | | specifies the default UI priority for new latent styles. | The higher value of ui priority is, the less preceedence it has so that styles might be displayed less prominently. | |
| `w:defSemiHidden` | | | specifies the default semi-hidden state for new latent styles. | | |
| `w:defUnhideWhenUsed` | | | specifies the default `unhide when used` state. | | |
| `w:defQFormat` | | | specifies the default "quick format" state for new latent styles. | | |

###### attribute in `<w:lsdException>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:name` | | | defines the exception to default LSD as `Normal` style | | |
| `w:semiHidden` | | | determines whether the style is hidden from the user interface under normal circumstances. | | |
| `w:uiPriority` | | | of the style in the user interface (e.g., in the Styles pane). | Concept similar to the concept mentioned at cell whose row is `w:defUIPriority` and column is `note`. | |
| `w:unhideWhenUsed` | | | specifies whether the style should become visible in the UI if it's used in the document, even if it was initially semi-hidden. | Concept similar to the concept mentioned at cell whose row is `w:defUnhideWhenUsed` and column is `note`. | | 
| `w:qFormat` | | | determines whether the style appears in the Quick Styles gallery. | Concept similar to the concept mentioned at cell whose row is `w:defQFormat` and column is `note`. | |



##### examples and explanations
###### example 1 -- fonts
```
<w:fonts>
   <w:defaultFonts w:ascii="Times New Roman" w:fareast="新細明體" w:h-ansi="Times New Roman" w:cs="Times New Roman"/>
   <w:font w:name="Times New Roman">
      <w:panose-1 w:val="02020603050405020304"/>
      <w:charset w:val="00"/>
      <w:family w:val="Roman"/>
      <w:pitch w:val="variable"/>
      <w:sig w:usb-0="E0002EFF" w:usb-1="C000785B" w:usb-2="00000009" w:usb-3="00000000" w:csb-0="000001FF" w:csb-1="00000000"/>
   </w:font>
</w:fonts>
```

In above example, we can know that

+ In `<w:fonts>`, it configures properties of a collection of fonts.
+ In `<w:defaultFonts w:ascii="Times New Roman" w:fareast="新細明體" w:h-ansi="Times New Roman" w:cs="Times New Roman"/>`, it configure the default font.</br>It is `Times New Roman` when thoese text that uses default font is encoded with ascii encoding.</br>It is `新細明體` for thoese fareast-text that uses default font.</br>It is `Times New Roman` when thoese text that uses default font is encoded with high Ansi encoding.</br>It is `Times New Roman` for those complex script text that uses default font.
+ In `<w:font w:name="Times New Roman">`, it gives name of the font as `Times New Roman`, which indicates the text whose font is `Times New Roman` have these properties (inside `<w:font w:name="Times New Roman">` tag).
+ In `<w:panose-1 w:val="02020603050405020304"/>` (inside `<w:font w:name="Times New Roman">` tag), it classifies the text by PANOSE system with id `02020603050405020304` (that will be used with highest priority)
+ In `<w:charset w:val="00"/>`, it configures charset id as `00`.
+ In `<w:family w:val="Roman"/>`, it configures family of font as `Roman`.
+ In `<w:pitch w:val="variable"/>`, it configures pitch as variable-pitch.
+ In `<w:sig w:usb-0="E0002EFF" w:usb-1="C000785B" w:usb-2="00000009" w:usb-3="00000000" w:csb-0="000001FF" w:csb-1="00000000"/>`, it configure the digital signature.</br>Its 0th USB identifier (with highest priority) is `E0002EFF`.</br>Its 1th USB identifier is `C000785B`.</br>Its 2th USB identifier is `00000000`.</br>Its 3th USB identifier is `00000000`.</br>Its 0th CSB identifier is `000001FF`.</br>Its 1th CSB identifier is `00000000`.

> [!NOTE]
> USB id stands for unique signature block identifier.
> CSB id stands for custom signature block identifier.

> [!IMPORTANT]
> PANOSE system will be used when the specific font is NOT found in the device, it is corrupted, or it can not work.

> [!IMPORTANT]
> the value of the `w:val` attribute is "02020603050405020304". Each pair of digits represents a specific aspect of the font:
> 1.  **Family**: 02 = Text and display
> 2.  **Serif style**: 02 = Cove
> 3.  **Weight**: 06 = Book
> 4.  **Proportion**: 03 = Even width
> 5.  **Contrast**: 05 = Medium
> 6.  **Stroke variation**: 04 = Gradual/transitional
> 7.  **Arm style**: 05 = Slanted
> 8.  **Letterform**: 02 = Normal/upright
> 9.  **Midline**: 03 = Continuous
> 10. **X-height**: 04 = Medium

###### example 2 -- run
```
<w:r>
  <w:rPr>
    <!-- ... -->
    <w:rFonts w:ascii="標楷體" w:eastAsia="標楷體" w:hAnsi="標楷體"/>
    <w:sz w:val="52"/>
    <w:szCs w:val="52"/>
    <!-- ... -->
  </w:rPr>
</w:r>
```

In this example, we can know that

1. In `<w:r>`, it defines a run.
2. In `<w:rPr>`, it configures the property of the run.
3. In `<w:rFonts w:ascii="標楷體" w:eastAsia="標楷體" w:hAnsi="標楷體"/>`,

it configure the default fonts of the run,

the default fonts are `標楷體`, `標楷體`, `標楷體` when it is decoded as ascii characters, East Asian characters, high Ansi characters respectively.

4. In `<w:sz w:val="52"/>`,

it also configure the default size is 52 half-points for **standard characters** (i.e. non-complex script characters) (like English, French, German etc).

> [!TIP]
> You can think it as setting the `style` attr as `"font-size:52"` in native html5.

5. In `<w:szCs w:val="52"/>`,

it also configure the default size is 52 for **complex script characters** (like Arabic, Hebrew, Devanagari etc).

> [APPRECIATION]
> Thanks to Google Gemini, it refers from Google Gemini's answer.

###### example 3 -- table
```
<!-- other elements omitted -->

<w:tbl>
  <w:tblPr>
    <w:tblStyle w:val="TableGrid"/>
    <w:tblW w:w="5000" w:type="auto"/>
    <w:tblLook w:val="04A0"/>
  </w:tblPr>
  <w:tblGrid>
    <w:gridCol w:w="1892.5"/>
  </w:tblGrid>
  <w:tr>
    <w:tc>
      <w:tcPr>
        <w:tcW w:w="15140" w:type="dxa"/>
        <w:gridSpan w:val="9"/>
      </w:tcPr>
    </w:tc>
    <w:p>
      <w:pPr>
        <w:jc w:val="left"/>
      </w:pPr>
      <w:r>
        <w:rPr>
          <w:rFonts w:ascii="標楷體" w:hAnsi="標楷體" w:cs="標楷體" w:eastAsia="標楷體"/>
          <w:sz w:val="32"/>
          <w:szCs w:val="32"/>
          <w:b/>
        </w:rPr>
        <w:t>text 1</w:t>
      </w:r>
    </w:p>
  </w:tr>
</w:tbl>
```

In the above example, we can know that

+ In `<w:tbl>`, it adds a table.
+ In `<w:tblPr>`, it add some properties of the table.
+ In `<w:tblStyle w:val="TableGrid"/>`, the table uses predefined style named `TableGrid` which is defined in `~/word/style.xml`.
+ In `<w:tblW w:w="5000" w:type="auto"/>`, the table width is 5000 and the Word will automatically justify the width to fit the content in cells.
+ In `<w:tblLook w:val="04A0"/>`, the `<w:tblLook>` tag determines which table styles and formatting options should be applied to a table.</br>The value of `w:val` attribute acts like a bitmask then determines which table styles and formatting options.</br>Its value is `04A0` which is a hexadecimal number.</br>Converting `04A0` from hexadecimal number to binary number  gets `0000 0100 1010 0000`.</br>Only 5th bit (counting from LST, zero-based), 7th bit and 10th bit are set to 1 (other bits is set to 0).</br>When 5th bit is set to 1, applies table formatting for first row.</br>When 7th bit is set to 1, applies table formatting for first column.</br>When 10th bit is set to 1, do not apply column banding.</br>Therefore, applies table formatting for first row and first column. Dont't apply column banding. For more details, see [table formatting option and styling](https://github.com/40843245/Microsoft_Office/blob/main/Product/General%20Product/elements/table/table%20formatting%20option%20and%20styling/element%20value%20in%20OOXML.md)
+ In `<w:tblGrid>`, it defines a header of the table.
+ In `<w:gridCol w:w="1892.5"/>`, it defines a column of the table and set its width as 1892.5 twips.
+ In `<w:tr>`, it defines a row of the table.
+ In `<w:tc>`, it defines a cell in the row.
+ In `<w:tcPr>`, it defines the cell property.
+ In `<w:tcW w:w="15140" w:type="dxa"/>`, it configures width of the cell is 15140 twips.
+ In `<w:gridSpan w:val="9"/>`, it configure the grid span of the cell is nine, which means that the cell is cross from nine columns. The nine columns of this row is merged into this one cell.
+ In `<w:p>`, it defines a paragraph.
+ In `<w:pPr>`, it defines properties of the paragraph.
+ In `<w:jc w:val="left"/>`, it configures the alignment of the paragraph as left. The paragraph is left-aligned.
+ In `<w:r>` (inside `<w:p>`), it defines a run in this paragraph..
+ In `<w:rPr>`, it defines properties of the run.
+ In `<w:rFonts w:ascii="標楷體" w:hAnsi="標楷體" w:cs="標楷體" w:eastAsia="標楷體"/>`, it configures the fonts of run.</br>It is `標楷體` when the text that uses the run is encoded with ascii encoding.</br>It is `標楷體` when the text that uses the run is encoded with high Ansi encoding. It is `標楷體` for those complex-script text that uses the run.</br>It is `標楷體` when the text that uses the run is eastern-asia text (東南亞文字).
+ In `<w:sz w:val="32"/>`, it configures the size for those non-complex script text that uses the run is 32 twips.
+ In `<w:szCs w:val="32"/>`, it configures the size for those complex script text that uses the run is 32 twips.
+ In `<w:b/>`, it configures the text that uses the run is bold.
+ In `<w:t>text 1</w:t>` (inside `<w:r>`), it adds a text with content`text 1` in the run which is used by the paragraph. 

###### example 4 -- list
```
<w:lists>
   <w:listDef w:listDefId="0">
      <w:lsid w:val="FFFFFF7C"/>
      <w:plt w:val="SingleLevel"/>
      <w:tmpl w:val="CC904CB8"/>
      <w:lvl w:ilvl="0">
         <w:start w:val="1"/>
         <w:lvlText w:val="%1."/>
         <w:lvlJc w:val="left"/>
         <w:pPr>
            <w:tabs>
               <w:tab w:val="list" w:pos="2281"/>
            </w:tabs>
            <w:ind w:left-chars="1000" w:left="2281" w:hanging-chars="200" w:hanging="360"/>
         </w:pPr>
      </w:lvl>
   </w:listDef>
</w:lists>
```

In above example, we can know that

+ In `<w:lists>`, it acts as a container for the list definitions.
+ In `<w:listDef w:listDefId="0">`, it defines the definition of list</br>which id is 0.
+ In `<w:lsid w:val="FFFFFF7C"/>`, it specifies the list style identifier whose value is `FFFFFF7C`.
+ In `<w:plt w:val="SingleLevel"/>`, it specifies the list pattern type is `single`, which means this list has only one level.
+ In `<w:tmpl w:val="CC904CB8"/>`, it specifies the template identifier whose value is `CC904CB8`.
+ In `<w:lvl w:ilvl="0">`, it defines the properties for a specific level, whose indentation level is 0.
+ In `<w:start w:val="1"/>`, it speficies the start point is 1.</br>i.e. The placeholder of first item in this level will be marked as `1` (or its corresponding symbol according to number formatting).
+ In `<w:lvlText w:val="%1."/>`, it specifies the placeholder.</br>The placeholder of first item in this level will be marked as `%1` (or its corresponding symbol according to number formatting) instead of `1`.
+ In `<w:lvlJc w:val="left"/>`, the placeholder of items in this level item in this level are left-aligned.
+ In `<w:pPr>`, it defines properties of a paragraph.
+ In `<w:tabs>`, it acts a container of a tab stop.
+ In `<w:tab w:val="list" w:pos="2281"/>`, it defines a tab stop specifically for list indentation at the position "2281" twips (i.e. twentieths of a point).
+ In `<w:ind w:left-chars="1000" w:left="2281" w:hanging-chars="200" w:hanging="360"/>`, controls the indentation of the list item.</br>By this attribute `w:left="2281"`, left indentation of the paragraph takes 2281 twips in total.</br>By this attribute `w:left-chars="1000"`, left indentation of the paragraph takes 1000 characters unit in total.</br>By this attribute `w:hanging="360"`, hanging indentation of the paragraph takes 360 twips in total.</br>By this attribute `w:hanging-chars="200"`, hanging indentation of the paragraph takes 200 characters unit in total.</br>Watch out for preceedence of this attribute. See following note.

> [!NOTE]
> The `w:hanging` attributes usually takes precedence over than `w:hanging-chars`.
>
> Similarly, the `w:left` attributes usually takes precedence over than `w:left-chars`.

###### example 5 -- line border

```
<w:rPr>
   <!-- other tags omitted -->
   <w:rFonts w:fareast="標楷體" w:hint="fareast" />
   <w:bdr w:val="single" w:sz="4" wx:bdrwidth="10" w:space="0" w:color="auto" />
</w:rPr>
```

###### example 6 -- page border
```
<w:sectPr>
  <w:pgBorders w:display="notFirstPage" w:offsetFrom="text" w:zOrder="back">
    <w:top w:val="single" w:sz="8" w:space="24" w:color="0000FF"/>
    <w:left w:val="dashed" w:sz="12" w:space="18" w:color="FF0000"/>
    <w:bottom w:val="double" w:sz="6" w:space="24" w:color="008000"/>
    <w:right w:val="dotted" w:sz="10" w:space="18" w:color="800080"/>
  </w:pgBorders>
</w:sectPr>
```

In above example, we can know that

+ In `<w:sectPr>`, it defines properties of the section.
+ In `<w:pgBorders w:display="notFirstPage" w:offsetFrom="text" w:zOrder="back">`, <ol><li>`w:display="notFirstPage"` indicates all pages (except for first page) should be display the page border within the section.</li><li>`w:offsetFrom="text"` indicates the values of `w:space` attribute (inside this tag) will be measured from the text margins of the page.</li><li>`w:zOrder="back"` specifies that the page borders should be rendered behind the document content.</li></ol>

###### example 7 -- display background shape
```
<w:displayBackgroundShape w:val="true"/>
```

In above example, we can know that

+ In `<w:displayBackgroundShape w:val="true"/>`, it will display background shape when a user open a Word file with Microsoft Office Word.

###### example 8 -- theme font language
```
<w:themeFontLang w:val="zh-TW" w:bidi="ar-SA"/>
```

In above example, we can know that

+ In `w:val="zh-TW"`, when applying theme fonts to text that is marked as **Traditional Chinese (Taiwan)**, use language-specific rendering rules appropriate for `zh-TW`.
+ In `w:bidi="ar-SA"`, When applying theme fonts to text that is marked as **Arabic (Saudi Arabia)** (a right-to-left language), use language-specific rendering rules appropriate for `ar-SA`.

###### example 9 -- color scheme
```
<w:clrSchemeMapping w:bg1="light1" w:t1="dark1" w:bg2="light2" w:t2="dark2" w:accent1="accent1" w:accent2="accent2" w:accent3="accent3" w:accent4="accent4" w:accent5="accent5" w:accent6="accent6" w:hyperlink="hyperlink" w:followedHyperlink="followedHyperlink"/>
```

In above example, we can know that

+ By tag name `w:clrSchemeMapping`, we can know it configure the scheme mapping table for document role.
+ In `w:bg1`, in the scheme mapping table, the property -- background color 1 is set to `light1`.
+ In `w:t1`, in the scheme mapping table, the property -- text color 1 is set to `dark1`.
+ In `w:bg2`, in the scheme mapping table, the property -- background color 2 is set to `light2`.
+ In `w:t2`, in the scheme mapping table, the property -- text color 2 is set to `dark2`.
+ In `w:accent1`, in the scheme mapping table, the property -- accent color 1 is set to `accent1`.
+ In `w:accent2`, in the scheme mapping table, the property -- accent color 2 is set to `accent2`.
+ In `w:accent3`, in the scheme mapping table, the property -- accent color 3 is set to `accent3`.
+ In `w:accent4`, in the scheme mapping table, the property -- accent color 4 is set to `accent4`.
+ In `w:accent5`, in the scheme mapping table, the property -- accent color 5 is set to `accent5`.
+ In `w:accent6`, in the scheme mapping table, the property -- accent color 6 is set to `accent6`.
+ In `w:hyperlink`, in the scheme mapping table, the property -- hyperlink is set to `hyperlink`.
+ In `w:followedHyperlink`, in the scheme mapping table, the property -- followed hyperlink 1 is set to `followedHyperlink`.



###### example 10 -- default shape
```
<w:shapeDefaults>
    <o:shapedefaults v:ext="edit" spidmax="2050"/>
    <o:shapelayout v:ext="edit">
        <o:idmap v:ext="edit" data="1"/>
    </o:shapelayout>
</w:shapeDefaults>
```

In above example, we can know that

+ In `<w:shapeDefaults>`, it defines a container containing default shapes.
+ In `<o:shapedefaults v:ext="edit" spidmax="2050"/>`, it specifies that id of newly created shape must be less than or equal to 2050 (according from `spidmax="2050"`).</br>Additionally,it specifies that newly created shape is fully editable in Office app (according from `v:ext="edit"`).
+ In `<o:idmap v:ext="edit" data="1"/>`, it sets the current id of newly created shape to one. Thus, the next id of newly created shape will be set to two. And it is current newly created shape is fully editable.
  
###### example 11 -- separator for number symbol
```
<w:decimalSymbol w:val="."/>
```

In above example, we can know that

+ In `<w:decimalSymbol w:val="."/>`, it specifies the separator of decimal symbol is `.`.

###### example 12 -- separator for list
```
<w:listSeparator w:val=","/>
```

In above example, we can know that

+ In `<w:listSeparator w:val=","/>`, it specifies the separator of list is `,`.

###### example 13 -- default setting for entire document
```
<w:docDefaults>
    <w:rPrDefault>
        <w:rPr>
            <w:rFonts w:asciiTheme="minorHAnsi" w:eastAsiaTheme="minorHAnsi" w:hAnsiTheme="minorHAnsi" w:cstheme="minorBidi"/>
            <w:sz w:val="22"/>
            <w:szCs w:val="22"/>
            <w:lang w:val="zh-TW" w:eastAsia="en-US" w:bidi="ar-SA"/>
        </w:rPr>
    </w:rPrDefault>
    <w:pPrDefault/>
</w:docDefaults>
```

In above example, we can know that

+

###### example 14 -- default latent style
```
<w:latentStyles w:defLockedState="0" w:defUIPriority="99" w:defSemiHidden="1" w:defUnhideWhenUsed="1" w:defQFormat="0" w:count="267">
```

In above example, we can know that

+ In `w:latentStyles`, it specifies the default setting for latent styles.
+ In `w:defLockedState="0"`, it sets the locked state to `false` by default , meaning the latent styles will NOT be locked by default.
+ In `w:defUIPriority="99"`, it sets the ui priority of latent style to 99 by default.
+ In `w:defSemiHidden="1"`, it sets the semi-hidden state to `true` by default, meaning the latent styles are semi-hidden by default,</br>so that they will not be readily visible in the Styles pane unless they are in use in the document, by default.\
+ In `w:defUnhideWhenUsed`, it sets the unhide-when-used state to `true` by default, meaning that if a latent style is applied to content, then it will automatically become unhidden and visible in the Styles pane, by default.
+ In `w:defQFormat`, it sets the quick format style to `false`, meaning that latent styles are not included in the Quick Styles gallery, by default.
+ In `w:count="267"`, we can know there are 267 latent styles defined in the Word file.

###### example 15 -- LSD and latent style
```
<w:lsdException w:name="Normal" w:semiHidden="0" w:uiPriority="0" w:unhideWhenUsed="0" w:qFormat="1"/>
```

In above example, we can know that

+ In `w:lsdException`, it defines a latent style.
+ In `w:name="Normal"`, it uses `Normal` style.
+ In `w:semiHidden="0"`, it sets semi-hidden state to `false`, meaning that the latent style is NOT semi-hidden and will be visible in the Styles pane.
+ In `w:uiPriority="0"`, it sets the ui priority to zero.
+ In `w:unhideWhenUsed="0"`, the latent style is NOT unhide (i.e. become visible) when it is actually used.
+ In `w:qFormat="1"`, the latent style will be placed in Quick Style pane.
  
#### about `m` namespace
##### elements in `m` namespace
| element in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<m:mathPr>` | | math properties | configures properties about math. | | |
| `<m:mathFont>` | | math font | configures properties of font that used in mathematical content. | | |
| `<m:brkBin>` | | *br*ea*k* on *bin*ary operators | configures properties of break on binary operator (such as `+` in `3+4`.) that used in mathematical content. | See `Appendix 5`[^4] for more information. | |
| `<m:brkBinSub>` | | substitution string for *br*ea*k* on *bin*ary operators | configures properties of substitution string for break on binary operators (such as `+` in `3+4`.) that used in mathematical content.</br>Simply said, it configures the text to be displayed as a visual indicator of a broken binary operation. | See `Appendix 5`[^4] for more information.| |
| `<m:smallFrac>` | | small *frac*tion style | configure the setting for the display of inline fractions. | | DON'T confuse small *frac*tion style and style of small fraction (i.e. the style of fraction which is small (with small numerator and denominator)). |
| `<m:dispDef/>` | | display mode for default setting | indicates that the default display mode for equations (inline or block) should be determined by the application's default settings |
| `<m:lMargin/>` | | left margin | left margin for displayed (block-level) equations. | | |
| `<m:rMargin/>` | | right margin | right margin for displayed (block-level) equations. | | |
| `<m:defJc/>` | | *def*ault *j*ustifi*c*ation | configures default justification for groups to an equation. | | |
| `<m:wrapIndent>` | | wrap indent | configure indentation for wrapped lines within multiline equations. | | |
| `<m:intLim>` | | *int*egration *lim*itation | configures limits of integration should be displayed as.  | | | | 
| `<m:naryLim>` | | *n*-*ary* operation *lim*itation | configures limits of n-ary operator should be displayed as.  | | | 

##### atttribute about `m` namespace
###### attribute in `<m:brkBin>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines which position the binary operator should be placed when it has neccessary line break of the expression with a binary operator. | | |

###### attribute in `<m:brkBinSub>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | the string that will replaced to for the line break on an expression with a binary operator. | | |

###### attribute in `<m:smallFrac>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines small fraction style is enabled or disabled. | | |

###### attribute in `<m:lMargin>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines left margin of the equation | its unit is in twips. | |

###### attribute in `<m:rMargin>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines right margin of the equation | its unit is in twips. | |

###### attribute in `<m:defJc>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines justification of the equation in the default settings | | |

###### attribute in `<m:wrapIndent>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines indentation for wrapping text in a multiline equation. | | |

###### attribute in `<m:intLim>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines the behaviour for limitations of integration operators. | | |

> [!NOTE]
> Integration operators includes:
>
> + integral: <img width="71" alt="image" src="https://github.com/user-attachments/assets/22d6eb26-9b8f-4b7d-91b2-5b6e75ed3582" />
> + summation: <img width="50" alt="image" src="https://github.com/user-attachments/assets/d6e87f62-8e05-4a91-8081-e1bb62088943" />
> + product: <img width="82" alt="image" src="https://github.com/user-attachments/assets/4f1127b4-8c9b-484c-a338-895f20e96961" />

> [!NOTE]
> This is an example of equation that apply the configuration set by `<m:intLim m:val="subSup">`.
>
> <img width="570" alt="image" src="https://github.com/user-attachments/assets/5e850987-7ee7-425e-abee-daec42024f51" />

> [!NOTE]
> This is an example of equation that apply the configuration set by `<m:intLim m:val="undOvr">`.
>
> <img width="445" alt="image" src="https://github.com/user-attachments/assets/61b8c6bf-bd28-4eb9-8489-96778d353194" />

###### attribute in `<m:naryLim>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines the behaviour for limitations of n-ary operators | | |

> [!NOTE]
> n-ary operators includes:
>
> + summation: <img width="50" alt="image" src="https://github.com/user-attachments/assets/d6e87f62-8e05-4a91-8081-e1bb62088943" />
> + product: <img width="82" alt="image" src="https://github.com/user-attachments/assets/4f1127b4-8c9b-484c-a338-895f20e96961" />
> + union: <img width="22" alt="image" src="https://github.com/user-attachments/assets/fc6ffa1f-d2c5-44fd-a9f0-7881fefe2f06" />
> + intersection: <img width="22" alt="image" src="https://github.com/user-attachments/assets/88a3d1a0-a3d4-4d2c-87a4-b84757f254d9" />

> [!NOTE]
> An example of equations that use the configuration set by `<m:naryLim m:val="subSup"/>`.
>
> <img width="509" alt="image" src="https://github.com/user-attachments/assets/3c11af0e-f8c5-4f0c-919a-82861352179e" />

> [!NOTE]
> An example of equations that use the configuration set by `<m:naryLim m:val="undOvr"/>`.
>
> <img width="547" alt="image" src="https://github.com/user-attachments/assets/1149ce2c-8790-4579-b1ff-f0a43c03c835" />

##### examples and explanations
###### example 1 -- configuration about math equation
```
<m:mathPr>
    <m:mathFont m:val="Cambria Math"/>
    <m:brkBin m:val="before"/>
    <m:brkBinSub m:val="--"/>
    <m:smallFrac m:val="off"/>
    <m:dispDef/>
    <m:lMargin m:val="0"/>
    <m:rMargin m:val="0"/>
    <m:defJc m:val="centerGroup"/>
    <m:wrapIndent m:val="1440"/>
    <m:intLim m:val="subSup"/>
    <m:naryLim m:val="undOvr"/>
</m:mathPr>
```

In above example, we can know that

+ In `<m:mathPr>`, it defines the properties about math equation.
+ In `<m:mathFont m:val="Cambria Math"/>`, it configures the default font for math equation is `Cambria Math`.
+ In `<m:brkBin m:val="before"/>`, it indicates that the binary operator should be at the beginning of the new line if the expression with a binary operator.
+ In `<m:brkBinSub m:val="--"/>`, it indicates when line break is necessary, it will place the `--` around the binary operator.
+ In `<m:smallFrac m:val="off"/>`, it disables small fraction style, meaning that the fraction will not be displayed in smaller size, ensuring that the fraction can be displayed in standard size.
+ In `<m:dispDef/>`, the math equation will be rendered with this displayed style by default.
+ In `<m:lMargin m:val="0"/>`, left-margin is 0.
+ In `<m:rMargin m:val="0"/>`, right-margin is 0.
+ In `<m:defJc m:val="centerGroup"/>`, the default justification of math equation is center-aligned. It is applied to a group of element.
+ In `<m:wrapIndent m:val="1440"/>`, when wrapping the text on a math equation, it indents 1440 twips.
+ In `<m:intLim m:val="subSup"/>`, for integration operators, the lower limit will be placed as sub-script and upper limit will be placed in super-script. 
+ In `<m:naryLim m:val="undOvr"/>`, for n-ary operator, the n-th symbol should be displayed underneath and over the equation.

[^1]:[Prequisite Review 1 -- terms](https://github.com/40843245/XmlOfOffice/blob/main/Word/structure/Prequisite%20Review%201%20--%20terms.md)

[^2]:[Appendix 2 -- available options of attribute of tag in xml for Word](https://github.com/40843245/XmlOfOffice/blob/main/Word/structure/Appendix%202%20--%20available%20options%20of%20attribute%20of%20tag%20in%20xml%20for%20Word.md#appendix-2----available-options-of-attribute-of-tag-in-xml-for-word)

[^3]:[`Appendix 1 -- tags in xml`](https://github.com/40843245/Xml/blob/main/structure/Appendix%201%20--%20tags%20in%20xml.md)

[^4]: [Appendix 5 -- break on binary operations](https://github.com/40843245/XmlOfOffice/blob/main/Word/structure/Appendix%205%20--%20break%20on%20binary%20operations.md)

[^5]:[9.2 Relationships in Office Open XML](https://ooxml.info/docs/9/9.2/)

[^6]:[ DocumentFormat.OpenXml.Linq.WNE class (MSDS API reference)](https://learn.microsoft.com/en-us/dotnet/api/documentformat.openxml.linq.wne?view=openxml-3.0.1) 

[^7]:[`docx格式文档详解：xml解析并用html还原`](https://juejin.cn/post/7166821284087595038)
