# idiots-guide-2-templating

- This is a quick guide to html templating and an overview for newbies. 
- The general idea is to have a few files, and the layout and stuff, and inject variables into the template which rendered on the fly
- What is a template ? 
- wikipedia - https://en.wikipedia.org/wiki/Template
- web templates is this zone = https://en.wikipedia.org/wiki/Web_template_system

*As the sun rises above the dawn,the shadow silently vanishing behind the developer's desk; a few few hits on the keyboard echoed around the room, code was being tested, the dawn on the internet and html, and some hacker was concerned about having to make a lot of pages,and created the first templates, which could have looked like this....*

```html
<html>\n
<head>\n
\t<title>@@@TITLE### | @@@SITE_TITLE###</title>\n
</head>\n
<body>\n
\t<h1>@@@TITLE###</h1>\n
\t<hr>\n
\t<h2>@@@SUMMARY###</h2>\n
\t@@@CONTENT###
\t<hr>
\t@@@FOOTER###
</body>\n
</html>
```

So depending where your coming from,  the idea here is to guide thought the concepts and how their implemented..


