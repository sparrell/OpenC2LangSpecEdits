<html>

<head>
<meta http-equiv=Content-Type content="text/html; charset=windows-1252">
<meta name=Generator content="Microsoft Word 15 (filtered)">
<title>Open Command and Control (OpenC2) Language Specification Version 1.0</title>
<style>
<!--
 /* Font Definitions */
 @font-face
	{font-family:Helvetica;
	panose-1:2 11 6 4 2 2 2 2 2 4;}
@font-face
	{font-family:Wingdings;
	panose-1:5 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"MS Mincho";
	panose-1:2 2 6 9 4 2 5 8 3 4;}
@font-face
	{font-family:"Cambria Math";
	panose-1:2 4 5 3 5 4 6 3 2 4;}
@font-face
	{font-family:Calibri;
	panose-1:2 15 5 2 2 2 4 3 2 4;}
@font-face
	{font-family:"Arial Unicode MS";
	panose-1:2 11 6 4 2 2 2 2 2 4;}
@font-face
	{font-family:Tahoma;
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:Consolas;
	panose-1:2 11 6 9 2 2 4 3 2 4;}
@font-face
	{font-family:"\@MS Mincho";
	panose-1:2 2 6 9 4 2 5 8 3 4;}
@font-face
	{font-family:"\@Arial Unicode MS";
	panose-1:2 11 6 4 2 2 2 2 2 4;}
 /* Style Definitions */
 p.MsoNormal, li.MsoNormal, div.MsoNormal
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
h1
	{margin-top:24.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.3in;
	text-indent:-.3in;
	page-break-before:always;
	page-break-after:avoid;
	border:none;
	padding:0in;
	font-size:18.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
h2
	{mso-style-name:"Heading 2\,H2";
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.4in;
	text-indent:-.4in;
	page-break-after:avoid;
	font-size:14.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
h3
	{mso-style-name:"Heading 3\,H3";
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.5in;
	text-indent:-.5in;
	page-break-after:avoid;
	font-size:13.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
h4
	{mso-style-name:"Heading 4\,H4";
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.6in;
	text-indent:-.6in;
	page-break-after:avoid;
	font-size:12.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
h5
	{margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.7in;
	text-indent:-.7in;
	page-break-after:avoid;
	font-size:12.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
h6
	{margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.8in;
	text-indent:-.8in;
	page-break-after:avoid;
	font-size:11.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
p.MsoHeading7, li.MsoHeading7, div.MsoHeading7
	{margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.9in;
	text-indent:-.9in;
	page-break-after:avoid;
	font-size:11.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
p.MsoHeading8, li.MsoHeading8, div.MsoHeading8
	{margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:1.0in;
	text-indent:-1.0in;
	page-break-after:avoid;
	font-size:11.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;
	font-style:italic;}
p.MsoHeading9, li.MsoHeading9, div.MsoHeading9
	{margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:1.1in;
	text-indent:-1.1in;
	page-break-after:avoid;
	font-size:11.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;
	font-style:italic;}
p.MsoToc1, li.MsoToc1, div.MsoToc1
	{margin-top:3.0pt;
	margin-right:0in;
	margin-bottom:3.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoToc2, li.MsoToc2, div.MsoToc2
	{margin-top:3.0pt;
	margin-right:0in;
	margin-bottom:3.0pt;
	margin-left:12.0pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoToc3, li.MsoToc3, div.MsoToc3
	{margin-top:3.0pt;
	margin-right:0in;
	margin-bottom:3.0pt;
	margin-left:24.0pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoToc4, li.MsoToc4, div.MsoToc4
	{margin-top:3.0pt;
	margin-right:0in;
	margin-bottom:3.0pt;
	margin-left:.5in;
	font-size:9.0pt;
	font-family:"Arial",sans-serif;}
p.MsoToc5, li.MsoToc5, div.MsoToc5
	{margin-top:3.0pt;
	margin-right:0in;
	margin-bottom:3.0pt;
	margin-left:48.0pt;
	font-size:9.0pt;
	font-family:"Arial",sans-serif;}
p.MsoToc6, li.MsoToc6, div.MsoToc6
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:60.0pt;
	font-size:9.0pt;
	font-family:"Arial",sans-serif;}
p.MsoToc7, li.MsoToc7, div.MsoToc7
	{margin-top:0in;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:1.0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoToc8, li.MsoToc8, div.MsoToc8
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:5.0pt;
	margin-left:70.0pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoToc9, li.MsoToc9, div.MsoToc9
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:5.0pt;
	margin-left:80.0pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoFootnoteText, li.MsoFootnoteText, div.MsoFootnoteText
	{mso-style-link:"Footnote Text Char";
	margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoHeader, li.MsoHeader, div.MsoHeader
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoFooter, li.MsoFooter, div.MsoFooter
	{mso-style-link:"Footer Char";
	margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoCaption, li.MsoCaption, div.MsoCaption
	{margin-top:6.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:0in;
	font-size:9.0pt;
	font-family:"Arial",sans-serif;
	font-style:italic;}
span.MsoFootnoteReference
	{vertical-align:super;}
p.MsoListBullet, li.MsoListBullet, div.MsoListBullet
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.25in;
	text-indent:-.25in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoListBullet2, li.MsoListBullet2, div.MsoListBullet2
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.5in;
	text-indent:-.25in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoTitle, li.MsoTitle, div.MsoTitle
	{margin-top:0in;
	margin-right:0in;
	margin-bottom:12.0pt;
	margin-left:0in;
	border:none;
	padding:0in;
	font-size:24.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
p.MsoBodyText, li.MsoBodyText, div.MsoBodyText
	{mso-style-link:"Body Text Char";
	margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoSubtitle, li.MsoSubtitle, div.MsoSubtitle
	{margin-top:0in;
	margin-right:0in;
	margin-bottom:12.0pt;
	margin-left:0in;
	border:none;
	padding:0in;
	font-size:18.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
p.MsoNoteHeading, li.MsoNoteHeading, div.MsoNoteHeading
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
a:link, span.MsoHyperlink
	{color:#0000EE;
	text-decoration:none;}
a:visited, span.MsoHyperlinkFollowed
	{color:purple;
	text-decoration:underline;}
p
	{margin-right:0in;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial Unicode MS",sans-serif;}
pre
	{margin:0in;
	margin-bottom:.0001pt;
	font-size:10.0pt;
	font-family:"Arial Unicode MS",sans-serif;}
tt
	{font-family:"Arial Unicode MS",sans-serif;}
p.MsoAcetate, li.MsoAcetate, div.MsoAcetate
	{mso-style-link:"Balloon Text Char";
	margin:0in;
	margin-bottom:.0001pt;
	font-size:8.0pt;
	font-family:"Tahoma",sans-serif;}
p.MsoListParagraph, li.MsoListParagraph, div.MsoListParagraph
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.5in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoListParagraphCxSpFirst, li.MsoListParagraphCxSpFirst, div.MsoListParagraphCxSpFirst
	{margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:0in;
	margin-left:.5in;
	margin-bottom:.0001pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoListParagraphCxSpMiddle, li.MsoListParagraphCxSpMiddle, div.MsoListParagraphCxSpMiddle
	{margin-top:0in;
	margin-right:0in;
	margin-bottom:0in;
	margin-left:.5in;
	margin-bottom:.0001pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.MsoListParagraphCxSpLast, li.MsoListParagraphCxSpLast, div.MsoListParagraphCxSpLast
	{margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.5in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.Titlepageinfo, li.Titlepageinfo, div.Titlepageinfo
	{mso-style-name:"Title page info";
	margin:0in;
	margin-bottom:.0001pt;
	page-break-after:avoid;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
p.Titlepageinfodescription, li.Titlepageinfodescription, div.Titlepageinfodescription
	{mso-style-name:"Title page info description";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.5in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.TitlepageinfodescriptionCxSpFirst, li.TitlepageinfodescriptionCxSpFirst, div.TitlepageinfodescriptionCxSpFirst
	{mso-style-name:"Title page info descriptionCxSpFirst";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:0in;
	margin-left:.5in;
	margin-bottom:.0001pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.TitlepageinfodescriptionCxSpMiddle, li.TitlepageinfodescriptionCxSpMiddle, div.TitlepageinfodescriptionCxSpMiddle
	{mso-style-name:"Title page info descriptionCxSpMiddle";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:0in;
	margin-left:.5in;
	margin-bottom:.0001pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.TitlepageinfodescriptionCxSpLast, li.TitlepageinfodescriptionCxSpLast, div.TitlepageinfodescriptionCxSpLast
	{mso-style-name:"Title page info descriptionCxSpLast";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.5in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.Contributor, li.Contributor, div.Contributor
	{mso-style-name:Contributor;
	margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.5in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.ContributorCxSpFirst, li.ContributorCxSpFirst, div.ContributorCxSpFirst
	{mso-style-name:ContributorCxSpFirst;
	margin-top:0in;
	margin-right:0in;
	margin-bottom:0in;
	margin-left:.5in;
	margin-bottom:.0001pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.ContributorCxSpMiddle, li.ContributorCxSpMiddle, div.ContributorCxSpMiddle
	{mso-style-name:ContributorCxSpMiddle;
	margin-top:0in;
	margin-right:0in;
	margin-bottom:0in;
	margin-left:.5in;
	margin-bottom:.0001pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.ContributorCxSpLast, li.ContributorCxSpLast, div.ContributorCxSpLast
	{mso-style-name:ContributorCxSpLast;
	margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.5in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.Legalnotice, li.Legalnotice, div.Legalnotice
	{mso-style-name:"Legal notice";
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.LegalnoticeCxSpFirst, li.LegalnoticeCxSpFirst, div.LegalnoticeCxSpFirst
	{mso-style-name:"Legal noticeCxSpFirst";
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:0in;
	margin-left:0in;
	margin-bottom:.0001pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.LegalnoticeCxSpMiddle, li.LegalnoticeCxSpMiddle, div.LegalnoticeCxSpMiddle
	{mso-style-name:"Legal noticeCxSpMiddle";
	margin:0in;
	margin-bottom:.0001pt;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.LegalnoticeCxSpLast, li.LegalnoticeCxSpLast, div.LegalnoticeCxSpLast
	{mso-style-name:"Legal noticeCxSpLast";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
span.Datatype
	{mso-style-name:Datatype;
	font-family:"Courier New";}
p.Code, li.Code, div.Code
	{mso-style-name:Code;
	margin-top:0in;
	margin-right:.3in;
	margin-bottom:0in;
	margin-left:.3in;
	margin-bottom:.0001pt;
	background:#D9D9D9;
	border:none;
	padding:0in;
	font-size:9.0pt;
	font-family:"Courier New";}
p.AppendixHeading2, li.AppendixHeading2, div.AppendixHeading2
	{mso-style-name:AppendixHeading2;
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.4in;
	text-indent:-.4in;
	page-break-after:avoid;
	font-size:14.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
span.Element
	{mso-style-name:Element;
	font-family:"Courier New";}
span.Attribute
	{mso-style-name:Attribute;
	font-family:"Courier New";}
span.Keyword
	{mso-style-name:Keyword;
	font-family:"Courier New";}
p.Note, li.Note, div.Note
	{mso-style-name:Note;
	margin-top:6.0pt;
	margin-right:.5in;
	margin-bottom:6.0pt;
	margin-left:.5in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.Definitionterm, li.Definitionterm, div.Definitionterm
	{mso-style-name:"Definition term";
	margin-top:4.0pt;
	margin-right:2.0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;
	font-weight:bold;}
p.Definition, li.Definition, div.Definition
	{mso-style-name:Definition;
	margin-top:4.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.5in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.Ref, li.Ref, div.Ref
	{mso-style-name:Ref;
	margin-top:2.0pt;
	margin-right:0in;
	margin-bottom:2.0pt;
	margin-left:1.5in;
	text-indent:-1.25in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;
	color:black;}
p.AppendixHeading1, li.AppendixHeading1, div.AppendixHeading1
	{mso-style-name:AppendixHeading1;
	margin-right:0in;
	margin-left:.25in;
	text-indent:-.25in;
	page-break-before:always;
	page-break-after:avoid;
	border:none;
	padding:0in;
	font-size:18.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
span.Refterm
	{mso-style-name:"Ref term";
	font-weight:bold;}
p.Example, li.Example, div.Example
	{mso-style-name:Example;
	margin-top:0in;
	margin-right:.3in;
	margin-bottom:0in;
	margin-left:.3in;
	margin-bottom:.0001pt;
	background:#E6E6E6;
	font-size:9.0pt;
	font-family:"Courier New";}
span.CODEtemp
	{mso-style-name:"CODE temp";
	font-family:"Courier New";}
p.Codesmall, li.Codesmall, div.Codesmall
	{mso-style-name:"Code small";
	margin-top:0in;
	margin-right:.3in;
	margin-bottom:0in;
	margin-left:.3in;
	margin-bottom:.0001pt;
	background:#E6E6E6;
	border:none;
	padding:0in;
	font-size:8.0pt;
	font-family:"Courier New";}
p.Examplesmall, li.Examplesmall, div.Examplesmall
	{mso-style-name:"Example small";
	margin-top:0in;
	margin-right:.3in;
	margin-bottom:0in;
	margin-left:.3in;
	margin-bottom:.0001pt;
	background:#E6E6E6;
	font-size:8.0pt;
	font-family:"Courier New";}
span.Variable
	{mso-style-name:Variable;
	font-style:italic;}
p.AppendixHeading4, li.AppendixHeading4, div.AppendixHeading4
	{mso-style-name:AppendixHeading4;
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.25in;
	text-indent:-.25in;
	page-break-after:avoid;
	font-size:12.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
span.FooterChar
	{mso-style-name:"Footer Char";
	mso-style-link:Footer;
	font-family:"Arial",sans-serif;}
p.RelatedWork, li.RelatedWork, div.RelatedWork
	{mso-style-name:"Related Work";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.75in;
	text-indent:-.25in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.RelatedWorkCxSpFirst, li.RelatedWorkCxSpFirst, div.RelatedWorkCxSpFirst
	{mso-style-name:"Related WorkCxSpFirst";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:0in;
	margin-left:.75in;
	margin-bottom:.0001pt;
	text-indent:-.25in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.RelatedWorkCxSpMiddle, li.RelatedWorkCxSpMiddle, div.RelatedWorkCxSpMiddle
	{mso-style-name:"Related WorkCxSpMiddle";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:0in;
	margin-left:.75in;
	margin-bottom:.0001pt;
	text-indent:-.25in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.RelatedWorkCxSpLast, li.RelatedWorkCxSpLast, div.RelatedWorkCxSpLast
	{mso-style-name:"Related WorkCxSpLast";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.75in;
	text-indent:-.25in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.Abstract, li.Abstract, div.Abstract
	{mso-style-name:Abstract;
	margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:.5in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.Notices, li.Notices, div.Notices
	{mso-style-name:Notices;
	margin-top:0in;
	margin-right:0in;
	margin-bottom:12.0pt;
	margin-left:0in;
	page-break-before:always;
	border:none;
	padding:0in;
	font-size:18.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
p.TextBody, li.TextBody, div.TextBody
	{mso-style-name:"Text Body";
	margin-top:0in;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;}
p.AppendixHeading3, li.AppendixHeading3, div.AppendixHeading3
	{mso-style-name:AppendixHeading3;
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.25in;
	text-indent:-.25in;
	page-break-after:avoid;
	font-size:13.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;}
span.BalloonTextChar
	{mso-style-name:"Balloon Text Char";
	mso-style-link:"Balloon Text";
	font-family:"Tahoma",sans-serif;}
span.FootnoteTextChar
	{mso-style-name:"Footnote Text Char";
	mso-style-link:"Footnote Text";
	font-family:"Arial",sans-serif;}
p.AppendixHeading5, li.AppendixHeading5, div.AppendixHeading5
	{mso-style-name:AppendixHeading5;
	margin-top:10.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:.7in;
	text-indent:-.7in;
	page-break-after:avoid;
	font-size:10.0pt;
	font-family:"Arial",sans-serif;
	color:#3B006F;
	font-weight:bold;
	font-style:italic;}
span.UnresolvedMention1
	{mso-style-name:"Unresolved Mention1";
	color:gray;
	background:#E6E6E6;}
span.BodyTextChar
	{mso-style-name:"Body Text Char";
	mso-style-link:"Body Text";
	font-family:"Arial",sans-serif;}
.MsoChpDefault
	{font-size:10.0pt;}
 /* Page Definitions */
 @page WordSection1
	{size:8.5in 11.0in;
	margin:1.0in 1.0in .5in 1.0in;}
div.WordSection1
	{page:WordSection1;}
@page WordSection2
	{size:8.5in 11.0in;
	margin:1.0in 1.0in .5in 1.0in;}
div.WordSection2
	{page:WordSection2;}
 /* List Definitions */
 ol
	{margin-bottom:0in;}
ul
	{margin-bottom:0in;}
-->
</style>

</head>

<body lang=EN-US link="#0000EE" vlink=purple>

<div class=WordSection1>

<div style='border:none;border-top:solid gray 1.0pt;padding:1.0pt 0in 0in 0in'>

<p class=MsoTitle><span style='font-size:14.0pt'>Open Command and Control
(OpenC2) Language Specification Version 1.0</span></p>

<p class=MsoSubtitle><span style='font-size:12.0pt'>Working Draft 01</span></p>

<p class=MsoSubtitle><a name="_Toc85472892"><span style='font-size:12.0pt'>31
October 2017</span></a></p>

</div>

<p class=Titlepageinfo>Technical Committee:</p>

<p class=Titlepageinfodescription><a
href="https://www.oasis-open.org/committees/openc2/">OASIS Open Command and
Control (OpenC2) TC</a></p>

<p class=Titlepageinfo>Chairs:</p>

<p class=ContributorCxSpFirst>Joe Brule (<a href="mailto:jmbrule@nsa.gov"><u><span
style='color:blue'>jmbrule@nsa.gov</span></u></a>), <a
href="https://www.nsa.gov/">National Security Agency</a></p>

<p class=ContributorCxSpLast><span style='color:black'>Sounil Yu</span> (<a
href="mailto:sounil.yu@bankofamerica.com"><u><span style='color:blue'>sounil.yu@bankofamerica.com</span></u></a>),
<a href="http://www.bankofamerica.com/">Bank of America</a></p>

<p class=Titlepageinfo>Editors:</p>

<p class=ContributorCxSpFirst>Jason Romano (<a href="mailto:jdroman@nsa.gov">jdroman@nsa.gov</a>),
<a href="https://www.nsa.gov/">National Security Agency</a></p>

<p class=ContributorCxSpLast>Duncan Sparrell (<a
href="mailto:duncan@sfractal.com">duncan@sfractal.com</a>), <a
href="http://www.sfractal.com/">sFractal Consulting LLC</a></p>

<p class=Titlepageinfo><a name=AdditionalArtifacts>Additional artifacts</a>:</p>

<p class=RelatedWorkCxSpFirst style='margin-left:.5in;text-indent:0in'>This
prose specification is one component of a Work Product that also includes:</p>

<p class=RelatedWorkCxSpLast><span style='font-family:Symbol'>·<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>TBSL</p>

<p class=Titlepageinfo><a name=RelatedWork>Related work</a>:</p>

<p class=Titlepageinfodescription>This specification is related to:</p>

<p class=RelatedWork><span style='font-family:Symbol'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>Related specifications (hyperlink, if available)</p>

<p class=Titlepageinfo>Declared XML namespaces:</p>

<p class=RelatedWork><span style='font-family:Symbol'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>TBSL</p>

<p class=Titlepageinfo>Abstract:</p>

<p class=Abstract>Cyberattacks are increasingly sophisticated, less expensive
to execute, dynamic and automated. The provision of cyberdefense via statically
configured products operating in isolation is no longer tenable. Standardized
interfaces, protocols and data models will facilitate the integration of the
functional blocks within a system or enterprise. Open Command and Control
(OpenC2) is a concise and extensible language to enable the command and control
of cyber defense components, subsystems and/or systems in a manner that is
agnostic of the underlying products, technologies, transport mechanisms or
other aspects of the implementation. It should be understood that a language
such as OpenC2 is necessary but insufficient to enable coordinated cyber
response. Other aspects of coordinated cyber response such as sensing,
analytics, and selecting appropriate courses of action are beyond the scope of
OpenC2.</p>

<p class=Titlepageinfo>Status:</p>

<p class=Abstract>This <a
href="https://www.oasis-open.org/policies-guidelines/oasis-defined-terms-2017-05-26#dWorkingDraft">Working
Draft</a> (WD) has been produced by one or more TC Members; it has not yet been
voted on by the TC or <a
href="https://www.oasis-open.org/policies-guidelines/tc-process#committeeDraft">approved</a>
as a Committee Draft (Committee Specification Draft or a Committee Note Draft).
The OASIS document <a
href="https://www.oasis-open.org/policies-guidelines/tc-process#standApprovProcess">Approval
Process</a> begins officially with a TC vote to approve a WD as a Committee
Draft. A TC may approve a Working Draft, revise it, and re-approve it any
number of times as a Committee Draft.</p>

<p class=Abstract>This Working Draft is being developed under the <a
href="https://www.oasis-open.org/policies-guidelines/ipr#Non-Assertion-Mode">Non-Assertion</a>
Mode of the <a href="https://www.oasis-open.org/policies-guidelines/ipr">OASIS
IPR Policy</a>, the mode chosen when the Technical Committee was established.
All members of the TC should be familiar with this document, which may create
obligations regarding the disclosure and availability of a member's patent,
copyright, trademark and license rights that read on an approved OASIS specification.
For information on whether any patents have been disclosed that may be
essential to implementing this specification, and any offers of patent
licensing terms, please refer to the Intellectual Property Rights section of
the TC’s web page (<a
href="https://www.oasis-open.org/committees/openc2/ipr.php">https://www.oasis-open.org/committees/openc2/ipr.php</a>).</p>

<p class=Abstract>Any machine-readable content (<a
href="https://www.oasis-open.org/policies-guidelines/tc-process#wpComponentsCompLang">Computer
Language Definitions</a>) declared Normative for this Work Product <u>must also
be provided</u> in separate plain text files. In the event of a discrepancy
between such plain text file and display content in the Work Product's prose
narrative document(s), the content in the separate plain text file prevails.</p>

<p class=Titlepageinfo>URI patterns:</p>

<p class=TitlepageinfodescriptionCxSpFirst><span class=MsoHyperlink><span
style='color:windowtext'>Initial publication URI:<br>
http://docs.oasis-open.org/openc2/oc2ls/v1.0/csprd01/oc2ls-v1.0-csprd01.docx</span></span></p>

<p class=TitlepageinfodescriptionCxSpLast><span class=MsoHyperlink><span
style='color:windowtext'>Permanent “Latest version” URI:<br>
http://docs.oasis-open.org/openc2/oc2ls/v1.0/oc2ls-v1.0.docx</span></span></p>

<p class=Abstract>&nbsp;</p>

<p class=Abstract>&nbsp;</p>

<p class=MsoNormal>Copyright © OASIS Open 2017. All Rights Reserved.</p>

<p class=MsoNormal>All capitalized terms in the following text have the
meanings assigned to them in the OASIS Intellectual Property Rights Policy (the
&quot;OASIS IPR Policy&quot;). The full <a
href="https://www.oasis-open.org/policies-guidelines/ipr">Policy</a> may be
found at the OASIS website.</p>

<p class=MsoNormal>This document and translations of it may be copied and
furnished to others, and derivative works that comment on or otherwise explain
it or assist in its implementation may be prepared, copied, published, and
distributed, in whole or in part, without restriction of any kind, provided
that the above copyright notice and this section are included on all such
copies and derivative works. However, this document itself may not be modified
in any way, including by removing the copyright notice or references to OASIS,
except as needed for the purpose of developing any document or deliverable
produced by an OASIS Technical Committee (in which case the rules applicable to
copyrights, as set forth in the OASIS IPR Policy, must be followed) or as
required to translate it into languages other than English.</p>

<p class=MsoNormal>The limited permissions granted above are perpetual and will
not be revoked by OASIS or its successors or assigns.</p>

<p class=MsoNormal>This document and the information contained herein is
provided on an &quot;AS IS&quot; basis and OASIS DISCLAIMS ALL WARRANTIES, EXPRESS
OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTY THAT THE USE OF THE
INFORMATION HEREIN WILL NOT INFRINGE ANY OWNERSHIP RIGHTS OR ANY IMPLIED
WARRANTIES OF MERCHANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE.</p>

<div style='border:none;border-top:solid gray 1.0pt;padding:1.0pt 0in 0in 0in'>

<p class=Notices>Table of Contents</p>

</div>

<p class=MsoToc1><a href="#_Toc497202203">1<span style='font-size:11.0pt;
font-family:"Calibri",sans-serif;color:windowtext'>        </span>Introduction<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>4</span></a></p>

<p class=MsoToc2><a href="#_Toc497202204">1.1 Goal<span style='color:windowtext;
display:none'> </span><span
style='color:windowtext;display:none'>4</span></a></p>

<p class=MsoToc2><a href="#_Toc497202205">1.2 Purpose and Scope<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>4</span></a></p>

<p class=MsoToc2><a href="#_Toc497202206">1.3 IPR Policy<span style='color:
windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>5</span></a></p>

<p class=MsoToc2><a href="#_Toc497202207">1.4 Terminology<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>5</span></a></p>

<p class=MsoToc2><a href="#_Toc497202208">1.5 Document Conventions<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>5</span></a></p>

<p class=MsoToc2><a href="#_Toc497202209">1.6 Naming Conventions<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>5</span></a></p>

<p class=MsoToc2><a href="#_Toc497202210">1.7 Normative References<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>5</span></a></p>

<p class=MsoToc2><a href="#_Toc497202211">1.8 Non-Normative References<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>5</span></a></p>

<p class=MsoToc1><a href="#_Toc497202212">2<span style='font-size:11.0pt;
font-family:"Calibri",sans-serif;color:windowtext'>        </span>OpenC2
Language<span style='color:windowtext;display:none'>. </span><span style='color:windowtext;display:none'>6</span></a></p>

<p class=MsoToc2><a href="#_Toc497202213">2.1 Overview<span style='color:windowtext;
display:none'>. </span><span
style='color:windowtext;display:none'>6</span></a></p>

<p class=MsoToc2><a href="#_Toc497202214">2.2 OpenC2 Command<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>6</span></a></p>

<p class=MsoToc3><a href="#_Toc497202215">2.2.1 Command Structure<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>6</span></a></p>

<p class=MsoToc3><a href="#_Toc497202216">2.2.2 Action Vocabulary<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>7</span></a></p>

<p class=MsoToc3><a href="#_Toc497202217">2.2.3 Target Vocabulary<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>8</span></a></p>

<p class=MsoToc3><a href="#_Toc497202218">2.2.4 Actuator<span style='color:
windowtext;display:none'> </span><span
style='color:windowtext;display:none'>9</span></a></p>

<p class=MsoToc3><a href="#_Toc497202219">2.2.5 Command Option Vocabulary<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>9</span></a></p>

<p class=MsoToc2><a href="#_Toc497202220">2.3 OpenC2 Response<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>9</span></a></p>

<p class=MsoToc3><a href="#_Toc497202221">2.3.1 Response Structure<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>9</span></a></p>

<p class=MsoToc1><a href="#_Toc497202222">3<span style='font-size:11.0pt;
font-family:"Calibri",sans-serif;color:windowtext'>        </span>OpenC2
Property Tables<span style='color:windowtext;display:none'>. </span><span style='color:windowtext;display:none'>10</span></a></p>

<p class=MsoToc1><a href="#_Toc497202223">4<span style='font-size:11.0pt;
font-family:"Calibri",sans-serif;color:windowtext'>        </span>Foundational
Actuator Profile<span style='color:windowtext;display:none'>. </span><span style='color:windowtext;display:none'>11</span></a></p>

<p class=MsoToc1><a href="#_Toc497202224">5<span style='font-size:11.0pt;
font-family:"Calibri",sans-serif;color:windowtext'>        </span>Conformance<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>12</span></a></p>

<p class=MsoToc1><a href="#_Toc497202225">Appendix A. Acknowledgments<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>13</span></a></p>

<p class=MsoToc1><a href="#_Toc497202226">Appendix B. Revision History<span
style='color:windowtext;display:none'>. </span><span
style='color:windowtext;display:none'>14</span></a></p>

<p class=Abstract>&nbsp;</p>

</div>

<span style='font-size:10.0pt;font-family:"Arial",sans-serif'><br clear=all
style='page-break-before:always'>
</span>

<div class=WordSection2>

<div style='border:none;border-top:solid gray 1.0pt;padding:6.0pt 0in 0in 0in'>

<h1><a name="_Toc287332006"></a><a name="_Toc497202203">1<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span>Introduction</a></h1>

</div>

<p class=MsoBodyText>The OpenC2 Language Specification defines a language used
to compose messages that instruct and coordinate the command and control of
cyber defenses between and within networks and systems. </p>

<p class=MsoBodyText>An OpenC2 command is composed of an action (what is to be
done), a target (what is being acted upon), an optional actuator (what is
executing the command), and command options, which influence how the command is
to be performed. </p>

<p class=MsoBodyText>A OpenC2 command that consists of an action coupled with a
target is sufficient for a high-level effects-based command (e.g., mitigate
evildomain.com). The inclusion in the command of an actuator and modifiers
provides additional precision and specificity (e.g., deny ip=1.2.3.4 by
actuator=firewall3 command-id=1eab14...). Additional detail about aspects of a
command may be included to increase the precision of the command.  For example,
which target (i.e., target specifier), additional information about what is to
be performed on a specific target type (i.e., target option), which actuator(s)
(i.e., actuator specifier) and/or additional information regarding how a
specific actuator executes the action (i.e., actuator option).</p>

<p class=MsoBodyText>An OpenC2 response is synchronously issued as a result of
an OpenC2 command.  OpenC2 responses are used to provide acknowledgement,
status, results of a command or other information in conjunction with a
particular command.</p>

<h2><a name="_Toc497202204">1.1 Goal</a></h2>

<p class=MsoBodyText>TBSL</p>

<h2><a name="_Toc497202205">1.2 Purpose and Scope</a></h2>

<p class=MsoBodyText>The OpenC2 Language Specification defines the set of
components to assemble a complete command and control message capability and
provide a framework so that the language can be extended to accommodate new
technologies. To achieve this purpose, the scope of this specification
includes: </p>

<p class=MsoBodyText style='margin-left:.75in;text-indent:-.5in'>1.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>the set of actions and options that may be used in OpenC2 commands,</p>

<p class=MsoBodyText style='margin-left:.75in;text-indent:-.5in'>2.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>the set of targets, target specifiers, and target options,</p>

<p class=MsoBodyText style='margin-left:.75in;text-indent:-.5in'>3.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>an organizational scheme that describes an actuator profile.</p>

<p class=MsoBodyText style='margin-left:.75in;text-indent:-.5in'>4.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>a syntax to express commands and responses.</p>

<p class=MsoBodyText style='margin-left:.75in;text-indent:-.5in'>5.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>the serialization of OpenC2 commands, and responses.</p>

<p class=MsoBodyText style='margin-left:.75in;text-indent:-.5in'>6.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>the procedures for extending the language to accommodate new
technologies in a manner that is consistent with the OpenC2 Language
Specification. </p>

<p class=MsoBodyText>The OpenC2 language is necessary but insufficient for the
realization of coordinated cyber response. Though necessary for cyber-response
implementations, the following items are beyond the scope of this
specification: </p>

<p class=MsoBodyText style='margin-left:.75in;text-indent:-.5in'>1.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>Language definitions for a particular actuator to extend the OpenC2
language. Extensions to the language will be captured in other specifications.</p>

<p class=MsoBodyText style='margin-left:.75in;text-indent:-.5in'>2.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>Specifying alternate serializations of OpenC2 commands. However,
optional serializations may be documented in other specifications.</p>

<p class=MsoBodyText style='margin-left:.75in;text-indent:-.5in'>3.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>The enumeration of the protocols required for transport, information
assurance, sensing, analytics and other external dependencies. The OpenC2
language assumes that the event has been detected, a decision to act has been
made, the act is warranted, and the initiator and recipient of the commands are
authenticated and authorized. The OpenC2 language was designed to be agnostic
of the other aspects of cyber defense implementations that realize these
assumptions.</p>

<h2><a name="_Toc287332007"></a><a name="_Toc85472893"></a><a
name="_Toc497202206">1.3 IPR Policy</a></h2>

<p class=Abstract style='margin-left:0in'>This Working Draft is being developed
under the <a
href="https://www.oasis-open.org/policies-guidelines/ipr#Non-Assertion-Mode">Non-Assertion</a>
Mode of the <a href="https://www.oasis-open.org/policies-guidelines/ipr">OASIS
IPR Policy</a>, the mode chosen when the Technical Committee was established.
For information on whether any patents have been disclosed that may be
essential to implementing this specification, and any offers of patent
licensing terms, please refer to the Intellectual Property Rights section of
the TC’s web page (<a
href="https://www.oasis-open.org/committees/openc2/ipr.php">https://www.oasis-open.org/committees/openc2/ipr.php</a>).</p>

<h2><a name="_Toc497202207">1.4 Terminology</a></h2>

<p class=MsoNormal>The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL
NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this
document are to be interpreted as described in [<a href="#RFC2119">RFC2119</a>]
and [<a href="#RFC8174">RFC8174</a>].</p>

<h2><a name="_Toc497202208">1.5 Document Conventions</a></h2>

<p class=MsoBodyText>TBSL</p>

<h2><a name="_Toc497202209">1.6 Naming Conventions</a></h2>

<p class=MsoBodyText>All type names, property names and literals are in
lowercase, except when referencing canonical names defined in another standard
(e.g. literal values from an IANA registry). Words in property names are
separated with an underscore (_), while words in type names and string
enumerations are separated with a hyphen (-). All type names, property names,
object names, and vocabulary terms are between three and 250 characters long.</p>

<div style='border-top:solid windowtext 1.0pt;border-left:none;border-bottom:
solid windowtext 1.0pt;border-right:none;padding:3.0pt 0in 3.0pt 0in;
background:#D9D9D9;margin-left:.3in;margin-right:.3in'>

<p class=Code style='margin:0in;margin-bottom:.0001pt;background:#D9D9D9'>{
&quot;action&quot;: &quot;contain&quot;,</p>

<p class=Code style='margin:0in;margin-bottom:.0001pt;background:#D9D9D9'> 
&quot;target&quot;: {</p>

<p class=Code style='margin:0in;margin-bottom:.0001pt;background:#D9D9D9'>   
&quot;user_account&quot;: {</p>

<p class=Code style='margin:0in;margin-bottom:.0001pt;background:#D9D9D9'>     
&quot;user_id&quot;: &quot;fjbloggs&quot;,</p>

<p class=Code style='margin:0in;margin-bottom:.0001pt;background:#D9D9D9'>     
&quot;account_type&quot;: &quot;windows-local&quot;</p>

<p class=Code style='margin:0in;margin-bottom:.0001pt;background:#D9D9D9'>    }</p>

<p class=Code style='margin:0in;margin-bottom:.0001pt;background:#D9D9D9'>  }</p>

<p class=Code style='margin:0in;margin-bottom:.0001pt;background:#D9D9D9'>}</p>

</div>

<h2><a name="_Toc497202210"></a><a name="_Toc287332008"></a><a
name="_Toc85472894"></a><a name="_Toc12011611"></a><a name="_Ref7502892">1.7 Normative</a>
References</h2>

<p class=Ref><span class=Refterm>[<a name=RFC2119>RFC2119</a>]</span>               Bradner,
S., &quot;Key words for use in RFCs to Indicate Requirement Levels&quot;, BCP
14, RFC 2119, DOI 10.17487/RFC2119, March 1997, &lt;<a
href="http://www.rfc-editor.org/info/rfc2119">http://www.rfc-editor.org/info/rfc2119</a>&gt;.</p>

<p class=Ref><b>[<a name=RFC8174>RFC8174</a>]</b>               Leiba, B.,
&quot;Ambiguity of Uppercase vs Lowercase in RFC 2119 Key Words&quot;, BCP 14,
RFC 8174, DOI 10.17487/RFC8174, May 2017, &lt;<a
href="http://www.rfc-editor.org/info/rfc8174">http://www.rfc-editor.org/info/rfc8174</a>&gt;.</p>

<p class=Ref><span class=Refterm>[Reference]</span><span class=Refterm><span
style='font-weight:normal'>             [Full reference citation]</span></span></p>

<h2><a name="_Toc497202211"></a><a name="_Toc287332009"></a><a
name="_Toc85472895">1.8 Non-Normative References</a></h2>

<p class=Ref><span class=Refterm>[Reference]</span><span class=Refterm><span
style='font-weight:normal'>             [Full reference citation]</span></span></p>

<p class=Ref>&nbsp;</p>

<div style='border:none;border-top:solid gray 1.0pt;padding:6.0pt 0in 0in 0in'>

<h1><a name="_Toc497202212">2<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>OpenC2 Language</a></h1>

</div>

<h2><a name="_Toc497202213">2.1 Overview</a></h2>

<p class=MsoBodyText>The OpenC2 language has two distinct types of messages:
Command and Response. At the most basic level, the OpenC2 Command describes an
action performed on a target. The OpenC2 Response is used to provide execution
status and optional data requested as a result of a command. OpenC2 Response
messages may refer to the command that initiated the response.</p>

<h2><a name="_Toc497202214">2.2 OpenC2 Command</a></h2>

<p class=MsoBodyText>The OpenC2 Command communicates an action to be performed
on a target and may include the actuator that is to execute the command.</p>

<h3><a name="_Toc497202215">2.2.1 Command Structure</a></h3>

<p class=MsoBodyText>An OpenC2 Command has four fields: ACTION, TARGET,
ACTUATOR and COMMAND-OPTIONS.</p>

<p class=MsoBodyText>The ACTION and TARGET fields are required and are
populated by one of the ‘action-types’ in Table 2-1 and the ‘target-types’ in
Table TBD. A particular target-type may be further refined by one or more
‘target-specifiers’ and/or ‘target-options’. </p>

<p class=MsoBodyText>The optional ACTUATOR field identifies the entity or
entities that are tasked to execute the OpenC2 Command.</p>

<p class=MsoBodyText>Information with respect to how the action is to be
executed is provided with one or more ‘actuator-options’. </p>

<p class=MsoBodyText>The optional COMMAND-OPTIONS field is populated by one or
more ‘command-options’ that provide information that influences how the command
is executed.    </p>

<p class=MsoBodyText>Table 2-1 summarizes the fields and subfields of an OpenC2
Command. OpenC2 Commands MUST contain an ACTION and TARGET and MAY contain an
ACTUATOR and/or COMMAND-OPTIONS. OpenC2 is agnostic of any particular
serialization; however, implementations MUST support JSON serialization of the
commands.</p>

<p class=MsoNormal align=center style='text-align:center;page-break-after:avoid'><b><span
style='color:black'>Table 2-1. OpenC2 Command Field Descriptions</span></b></p>

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0 width=624
 style='width:6.5in;margin-left:2.9pt;border-collapse:collapse;border:none'>
 <thead>
  <tr style='page-break-inside:avoid'>
   <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
   background:#1F497D;padding:0in 5.4pt 0in 5.4pt'>
   <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
   1.5pt;margin-left:0in;line-height:83%;page-break-after:avoid'><b><span
   style='line-height:83%;color:white'>Field</span></b></p>
   </td>
   <td width=486 valign=top style='width:364.5pt;border:solid black 1.0pt;
   border-left:none;background:#1F497D;padding:0in 5.4pt 0in 5.4pt'>
   <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
   1.5pt;margin-left:0in;line-height:83%;page-break-after:avoid'><b><span
   style='line-height:83%;color:white'>Description</span></b></p>
   </td>
  </tr>
 </thead>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>ACTION </span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Required. The task or activity to be performed.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>TARGET </span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Required. The object of the action. The ACTION is performed on
  the TARGET.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>type </span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Required. The specific type of TARGET.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#EFEFEF;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>target-specifier</span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#EFEFEF;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Optional. The specifier further identifies the target to some
  level of precision, such as a specific target, a list of targets, or a class
  of targets.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>target-option</span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Optional. Additional information about how to perform the action
  for a specific tar</span><span style='line-height:83%'>get type. </span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>ACTUATOR </span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Optional. The ACTUATOR may </span><span style='line-height:83%'>perform
  </span><span style='line-height:83%;color:black'>the ACTION on the TARGET.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>type </span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Required if the actuator is included, otherwise not applicable.
  The ACTUATOR type will be defined within the context of an actuator profile.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>actuator-specifier</span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Optional if the actuator is included, otherwise not applicable.
  The specifier identifies the actuator to some level of precision, such as a
  specific actuator, a list of actuators, or a </span><span style='line-height:
  83%'>group </span><span style='line-height:83%;color:black'>of actuators.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#EFEFEF;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>actuator-option</span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#EFEFEF;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Optional if the actuator is included, otherwise not applicable.
  Actuator-option identifies how a particular action is to be done for an
  actuator type. </span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 valign=top style='width:103.5pt;border:solid black 1.0pt;
  border-top:none;background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%'>COMMAND-OPTIONS</span><span
  style='line-height:83%;color:black'>(&lt;list-of-</span><span
  style='line-height:83%'>options</span><span style='line-height:83%;
  color:black'>&gt;)</span></p>
  </td>
  <td width=486 valign=top style='width:364.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Optional. Provide additional information on how the </span><span
  style='line-height:83%'>command </span><span style='line-height:83%;
  color:black'>is to be </span><span style='line-height:83%'>performed</span><span
  style='line-height:83%;color:black'>, such as date/time, periodicity,
  duration etc. </span><span style='line-height:83%'>COMMAND OPTIONS </span><span
  style='line-height:83%;color:black'>only influence/ impact the </span><span
  style='line-height:83%'>command </span><span style='line-height:83%;
  color:black'>and are defined independently of any ACTION, ACTUATOR or TARGET.
  </span></p>
  </td>
 </tr>
</table>

<p class=MsoBodyText>The TARGET of an OpenC2 command may include a set of
targets of the same type, a range of targets, or a particular target.
Specifiers for TARGETs are optional and provide additional precision for the
target.</p>

<p class=MsoBodyText>The OpenC2 ACTUATOR field provides information about the
entity that will execute the ACTION on the TARGET. Specifiers for actuators
provide additional information to refine the command so that a particular
function, system, class of devices, or specific device can be identified.
Options for actuators provide additional information to refine the command to
indicate how an action is to be done in the context of the actuator. Options
are distinct from COMMAND-OPTIONS in that options are a function of the
actuator and the action.</p>

<p class=MsoBodyText>COMMAND-OPTIONS influence the command by providing
information such as time, periodicity, duration, or other details on what is to
be executed. They can also be used to convey the need for acknowledgement or
additional status information about the execution of a command.</p>

<h3><a name="_Toc497202216">2.2.2 Action Vocabulary</a></h3>

<p class=MsoBodyText>This section defines the set of OpenC2 actions grouped by
their general activity. Table 2-2 summarizes the definition of the OpenC2
actions.</p>

<p class=MsoBodyText style='margin-left:.5in;text-indent:-.25in'><span
style='font-family:Symbol'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><u>Actions that Control Information</u>:<br>
These actions are used to gather information needed to determine the current
state or enhance cyber situational awareness.</p>

<p class=MsoBodyText style='margin-left:.5in;text-indent:-.25in'><span
style='font-family:Symbol'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><u>Actions that Control Permissions</u>:<br>
These actions are used to control traffic flow and file permissions (e.g.,
allow/deny).</p>

<p class=MsoBodyText style='margin-left:.5in;text-indent:-.25in'><span
style='font-family:Symbol'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><u>Actions that Control Activities/Devices</u>:<br>
These actions are used to control the state or the activity of a system, a
process, a connection, a host, or a device. The actions are used to execute
tasks, adjust configurations, set and update parameters, and modify attributes.</p>

<p class=MsoBodyText style='margin-left:.5in;text-indent:-.25in'><span
style='font-family:Symbol'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><u>Effects-Based Actions</u>:<br>
Effects-based actions are at a higher level of abstraction for purposes of
communicating a desired impact rather than a command to execute specific tasks.
This level of abstraction enables coordinated actions between enclaves, while
permitting a local enclave to optimize its workflow for its specific
environment. Effects-based action assumes that the recipient enclave has a
decision-making capability because effects-based actions typically do not have
a one-to-one mapping to the other actions.</p>

<p class=MsoNormal align=center style='text-align:center;page-break-after:avoid'><b><span
style='color:black'>Table 2-2. Summary of Action Definitions</span></b></p>

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0 width=624
 style='width:6.5in;margin-left:2.9pt;border-collapse:collapse;border:none'>
 <thead>
  <tr style='page-break-inside:avoid'>
   <td width=138 style='width:103.5pt;border:solid black 1.0pt;background:#1F497D;
   padding:0in 5.4pt 0in 5.4pt'>
   <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
   1.5pt;margin-left:0in;line-height:83%'><a name="_Hlk496907802"><b><span
   style='line-height:83%;color:white'>Action</span></b></a></p>
   </td>
   <td width=486 style='width:364.5pt;border:solid black 1.0pt;border-left:
   none;background:#1F497D;padding:0in 5.4pt 0in 5.4pt'>
   <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
   1.5pt;margin-left:0in;line-height:83%'><b><span style='line-height:83%;
   color:white'>Description</span></b></p>
   </td>
  </tr>
 </thead>
 <tr style='page-break-inside:avoid'>
  <td width=624 colspan=2 style='width:6.5in;border:solid black 1.0pt;
  border-top:none;background:gray;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-top:1.5pt;margin-right:0in;
  margin-bottom:1.5pt;margin-left:0in;text-align:center;line-height:83%'><b><span
  style='line-height:83%'>Actions that Control Information</span></b></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>scan</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘scan’ action is the systematic examination of some aspect
  of the entity or its environment in order to obtain information.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>locate</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘locate’ action is used to find an object either physically,
  logically, functionally, or by organization. </span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>query</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘query’ action initiates a single request for information.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>report</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘report’ action tasks an entity to provide information to a
  designated recipient of the information.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>notify</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘notify’ action is used to set an entity's alerting
  preferences.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=624 colspan=2 valign=top style='width:6.5in;border:solid black 1.0pt;
  border-top:none;background:gray;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-top:1.5pt;margin-right:0in;
  margin-bottom:1.5pt;margin-left:0in;text-align:center;line-height:83%;
  page-break-after:avoid'><b><span style='line-height:83%'>Actions that Control
  Permissions</span></b></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>deny</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘deny’ action is used to prevent a certain event or action
  from completion, such as preventing a flow from reaching a destination (e.g.,
  block) or preventing access.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>contain</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘contain’ action stipulates the isolation of a file</span><span
  style='line-height:83%'>,</span><span style='line-height:83%;color:black'>
  process, or entity such that it cannot modify or access assets or processes
  that support the business and/or operations of the enclave.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>allow</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘allow’ action permits the access to or execution of a
  target.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=624 colspan=2 valign=top style='width:6.5in;border:solid black 1.0pt;
  border-top:none;background:gray;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-top:1.5pt;margin-right:0in;
  margin-bottom:1.5pt;margin-left:0in;text-align:center;line-height:83%;
  page-break-after:avoid'><b><span style='line-height:83%'>Actions that Control
  Activities/Devices</span></b></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>start</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘start’ action initiates a process, application, system, or
  some other activity.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>stop</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘stop’ action halts a system or ends an activity.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>restart</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘restart’ action conducts a ‘stop</span><span
  style='line-height:83%;color:blue'>’ </span><span style='line-height:83%;
  color:black'>of a system or an activity followed by a ‘start’ of a system or
  an activity.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>pause</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘pause’ action ceases a system or activity while maintaining
  state.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>resume</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘resume’ action starts a system or activity from a paused
  state.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>cancel</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘cancel’ action invalidates a previously issued action.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>set</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘set’ action changes a value, configuration, or state of a
  managed entity within an IT system.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>update</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘update’ action instructs the component to retrieve,
  install, process, and operate in accordance with a software update,
  reconfiguration, or some other update.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>move</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘move’ action changes the location of a file, subnet,
  network, or process.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>redirect</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘redirect’ action changes the flow to a particular
  destination other than its original intended destination.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%'>create</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%'>The
  ‘create’ action adds a new entity (e.g., data, files, directories, security
  entities, etc.).</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>delete</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘delete’ action removes an entit</span><span
  style='line-height:83%'>y (e.g., </span><span style='line-height:83%;
  color:black'>data, files, flows, etc.). </span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>snapshot</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘snapshot’ action records and stores the state of a target
  at an instant in time.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>detonate</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘detonate’ action executes and observes the behavior of a
  target (e.g., file, hyperlink) in a manner that is isolated from assets that
  support the business or operations of the enclave.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>restore</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘restore’ action returns to an identical or similar known
  state.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>save</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘save’ action commits data or system state to memory.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>throttle</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘throttle’ action adjusts the rate of a process, function,
  or activity.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>delay</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘delay’ action stops or holds up an activity or data
  transmittal.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>substitute</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘substitute’ action replaces all or part of the data,
  content, or payload.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>copy</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘copy’ action duplicates a file or data flow.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>sync</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘sync’ action synchronizes a sensor or actuator with other
  system components.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=624 colspan=2 valign=top style='width:6.5in;border:solid black 1.0pt;
  border-top:none;background:gray;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-top:1.5pt;margin-right:0in;
  margin-bottom:1.5pt;margin-left:0in;text-align:center;line-height:83%;
  page-break-after:avoid'><b><span style='line-height:83%'>Effects-Based
  Actions</span></b></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>investigate</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘investigate’ action tasks the recipient enclave to
  aggregate and report information as it pertains to an anomaly.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>mitigate</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘mitigate’ action tasks the recipient enclave to circumvent
  the problem without necessarily eliminating the vulnerability or attack
  point.</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>remediate</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #D9D9D9;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>The ‘remediate’ action tasks the recipient enclave to eliminate
  the vulnerability or attack point.</span></p>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%;
  color:black'>Remediate implies that addressing the issue is paramount.</span></p>
  </td>
 </tr>
</table>

<h3><a name="_Toc497202217">2.2.3 Target Vocabulary</a></h3>

<p class=MsoBodyText>The TARGET is the object of the ACTION (or alternatively,
the ACTION is performed on the TARGET).  The baseline set of TARGETs is
summarized in Table 2-3 and a full description of the targets and their
associated specifiers is documented in the property tables (TBSL).</p>

<p class=MsoNormal align=center style='text-align:center'><b>Table 2-3. Summary
of Target Definitions</b>.</p>

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0 width=624
 style='width:6.5in;margin-left:2.9pt;border-collapse:collapse;border:none'>
 <tr>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;background:#1F497D;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><b><span style='line-height:83%;
  color:white'>Target</span></b></p>
  </td>
  <td width=486 style='width:364.5pt;border:solid black 1.0pt;border-left:none;
  background:#1F497D;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><b><span style='line-height:83%;
  color:white'>Description</span></b></p>
  </td>
 </tr>
 <tr>
  <td width=138 style='width:103.5pt;border:solid black 1.0pt;border-top:none;
  background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%'>TBSL</span></p>
  </td>
  <td width=486 style='width:364.5pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%'>TBSL</span></p>
  </td>
 </tr>
</table>

<h3><a name="_Toc497202218">2.2.4 Actuator</a></h3>

<p class=MsoBodyText>An ACTUATOR is an implementation of a cyber defense
function that executes the ACTION on the TARGET.  An actuator profile is a
specification that identifies the subset of actions, targets and other aspects
of this language specification that are meaningful in the context of a
particular ACTUATOR.  The actuator profile also identifies the portions of this
specification that are mandatory to implement as well as optional actions and
also defines appropriate actuator specifiers and the actuator options. </p>

<p class=MsoBodyText>An Actuator Profile SHALL be composed in accordance with
the following framework: TBSL.</p>

<h3><a name="_Toc497202219">2.2.5 Command Option Vocabulary</a></h3>

<p class=MsoBodyText>COMMAND OPTIONS influence a command and are independent of
the TARGET, ACTUATOR and ACTION itself.   COMMAND OPTIONS provide additional
information to refine how the command is to be performed such as time,
periodicity, or duration, or convey the need for status information such as a
response is required. The requested status/information will be carried in a
RESPONSE. </p>

<p class=MsoBodyText>Table 2-4 lists the valid modifiers.</p>

<p class=MsoNormal align=center style='text-align:center'><b>Table 2-4. Summary
of Command Options</b>.</p>

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0 width=624
 style='width:6.5in;margin-left:2.9pt;border-collapse:collapse;border:none'>
 <tr>
  <td width=135 style='width:101.5pt;border:solid black 1.0pt;background:#1F497D;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><b><span style='line-height:83%;
  color:white'>Command Option</span></b></p>
  </td>
  <td width=162 valign=top style='width:121.5pt;border:solid black 1.0pt;
  border-left:none;background:#1F497D;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><b><span style='line-height:83%;
  color:white'>Type</span></b></p>
  </td>
  <td width=327 style='width:245.0pt;border:solid black 1.0pt;border-left:none;
  background:#1F497D;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><b><span style='line-height:83%;
  color:white'>Description</span></b></p>
  </td>
 </tr>
 <tr>
  <td width=135 style='width:101.5pt;border:solid black 1.0pt;border-top:none;
  background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%'>TBSL</span></p>
  </td>
  <td width=162 valign=top style='width:121.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  background:#F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%'>TBSL</span></p>
  </td>
  <td width=327 style='width:245.0pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;background:
  #F2F2F2;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-top:1.5pt;margin-right:0in;margin-bottom:
  1.5pt;margin-left:0in;line-height:83%'><span style='line-height:83%'>TBSL</span></p>
  </td>
 </tr>
</table>

<p class=MsoBodyText>&nbsp;</p>

<h2><a name="_Toc497202220">2.3 OpenC2 Response</a></h2>

<p class=MsoBodyText>The OpenC2 Response is a message sent from an entity as
the result of a command.  Response messages provide acknowledgement, status,
results from a query or other information as requested from the issuer of the
command.  Response messages are solicited and correspond to a command.  The
recipient of the OpenC2 Response is typically the entity that issued the
command.</p>

<h3><a name="_Toc497202221">2.3.1 Response Structure</a></h3>

<p class=MsoNormal>TBSL</p>

<div style='border:none;border-top:solid gray 1.0pt;padding:6.0pt 0in 0in 0in'>

<h1><a name="_Toc497202222">3<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>OpenC2 Property Tables</a></h1>

</div>

<p class=MsoBodyText>TBSL</p>

<div style='border:none;border-top:solid gray 1.0pt;padding:6.0pt 0in 0in 0in'>

<h1><a name="_Toc497202223">4<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span>Foundational Actuator Profile</a></h1>

</div>

<p class=MsoBodyText>TBSL</p>

# 5. Conformance

OpenC2 is a command and control language that converges
(i.e. common point of understanding) on a common syntax, and lexicon.  OpenC2
does not have a dependency on a particular programming language, computing
platform, transport protocol etc. ~~.~~ Conformant implementations of OpenC2:

* MUST support OpenC2 commands, ~~responses and alerts~~ and responses as defined in this document.
* MUST implement the actions designated as mandatory in this document.
* MUST implement the targets designated as mandatory in this document.
* MAY implement optional targets defined in this document 
* MAY implement actuator specifiers, actuator options, target specifiers and/or target options as specified in one or more actuator profiles.
* MUST implement JSON serialization of the commands, responses and alerts that are consistent with the syntax defined in this document.
* TBSL


<p class=MsoBodyText>&nbsp;</p>

<div style='border:none;border-top:solid gray 1.0pt;padding:6.0pt 0in 0in 0in'>

<p class=AppendixHeading1><a name="_Toc497202225"></a><a name="_Toc287332012"></a><a
name="_Toc85472897">Appendix A. Acknowledgments</a></p>

</div>

<p class=MsoNormal>The following individuals have participated in the creation
of this specification and are gratefully acknowledged:</p>

<p class=Titlepageinfo>Participants:</p>

<p class=Contributor>TBSL</p>

<p class=MsoNormal>&nbsp;</p>

<div style='border:none;border-top:solid gray 1.0pt;padding:6.0pt 0in 0in 0in'>

<p class=AppendixHeading1><a name="_Toc497202226"></a><a name="_Toc287332014"></a><a
name="_Toc85472898">Appendix B. Revision History</a></p>

</div>

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none'>
 <tr>
  <td width=103 valign=top style='width:77.4pt;border:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><b>Revision</b></p>
  </td>
  <td width=96 valign=top style='width:1.0in;border:solid windowtext 1.0pt;
  border-left:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><b>Date</b></p>
  </td>
  <td width=144 valign=top style='width:1.5in;border:solid windowtext 1.0pt;
  border-left:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><b>Editor</b></p>
  </td>
  <td width=295 valign=top style='width:221.4pt;border:solid windowtext 1.0pt;
  border-left:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal><b>Changes Made</b></p>
  </td>
 </tr>
 <tr>
  <td width=103 valign=top style='width:77.4pt;border:solid windowtext 1.0pt;
  border-top:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal>v1.0-wd01</p>
  </td>
  <td width=96 valign=top style='width:1.0in;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal>10/31/2017</p>
  </td>
  <td width=144 valign=top style='width:1.5in;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal>Romano, Sparrell</p>
  </td>
  <td width=295 valign=top style='width:221.4pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal>Initial working draft</p>
  </td>
 </tr>
</table>

<p class=MsoNormal>&nbsp;</p>

</div>

</body>

</html>
