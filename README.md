# idiots-guide-2-templating

- This is a quick guide to html templating and an overview for newbies. 
- The general idea is to have a few files, and the layout and stuff, and inject variables into the template which rendered on the fly
- What is a template ? 
- wikipedia - https://en.wikipedia.org/wiki/Template
- web templates is this zone = https://en.wikipedia.org/wiki/Web_template_system

*As the sun rises above the dawn,the shadow silently vanishing behind the developer's desk; a few few hits on the keyboard echoed around the room, code was being tested, the dawn on the internet and html, and some hacker was concerned about having to make a lot of pages,and created the first templates, which could have looked like this....*

```html
<!-- And mad idea for a template {me} -->
<html>\n
<head>\n
\t<title>@@@TITLE### | @@@SITE_TITLE###</title>\n
</head>\n
<body>\n
\t<h1>@@@TITLE###</h1>\n
\t<hr>\n
\t<h2>@@@SUMMARY###</h2>\n
\t<h3>@@@PERSON###</h3>\n
\t@@@CONTENT###
\t<hr>
\t@@@FOOTER###
</body>\n
</html>
```

```php

// my variables for party..
$title = "Its party  time..."
$site_title = "Univerity Hack Dept"
$summary = "Hey guys and gals, if u see\t this\n then ping me on \t192\168\5\7 for some HTML"
$content = "Party time!!!!!!!!! room 14466545745|unix """
$person = "NULL"
$footer = "RSVP = don@unihacked.com"

// read template file
$TemplateFile = open("template.htm")
$tpl = $TemplateFile.readAll()
close($TemplateFile)

// get invite list
$EmailsFile = open("template.htm")
$emails_list = $EmailsFile.readAll()
close($EmailsFile)

$guest_list = split($emails_list, "\n")


for( $guest_list as $guest){
	// replace tempalte vars with persons
	$tpl = replace($tpl, "@@@SITE_TITLE###", $site_title)
	$tpl = replace($tpl, "@@@TITLE###", $title)
	$tpl = replace($tpl, "@@@SUMMARY###", $summary)
	$tpl = replace($tpl, "t@@@FOOTER###", $footer)
	sendmail("professor@another.uni", $guest, $tpl)
}
// :-)

```


So depending where your coming from,  the idea here is to guide thought the concepts and how their implemented..

Template Syntax.


For this exersize... we want a standard tempalte that does a few clever things..
# current date in your locale, and UTC dates
# Standard header and footer with terms..
# An active navigation system that higlights a page in nav
# 
