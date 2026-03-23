---
title: Hexo Webpages
date: 1969-10-29 00:00:00
category: guides
aside: true
copyright: false
archives: false
tags:
---
# Markdown
Markdown file are what Hexo uses to generate its webpages. The main structure of a Markdown file used by Hexo is simple; it consists of a front matter and a main body.

## Front Matter
The front matter of the Markdown file is denoted with three hyphens:

```YAML
---
criteria_a:
criteria_b:
...
criteria_e:
---

Some text...
```

It consists of toggles for specific settings provided by Hexo itself and other themes (Butterfly in this blog). For example, adding `title: Blog Page 1` would change the title of the corresponding page to Blog Page 1.

Detailed information about the configurations in front matter can be found on the documentation for Hexo and Butterfly: 
https://hexo.io/docs/front-matter
and
https://butterfly.js.org/en/posts/butterfly-docs-en-theme-pages/.

(the "pinned" tag also exists for this blog, and can be used to pin pages to the top of the homepage with "true" or "false". Defaults to false. This feature is from the hexo-generator-index-pin-top plugin.)
## Body
Under the front matter is where you write all the information or text you want your blog to show.

To write text, just type whatever you want underneath the front matter and it will display.

## Useful Things
Markdown also supports many different things other than plain text, such as media, code displays, hyperlinks, and many more. Butterfly also adds many utilities, but those are not needed for this blog.

### HTML, CSS and JavaScript
Hexo renders HTML, CSS and JavaScript input in Markdown files. More complex layouts not supported by the themes can be created using this.

For example:

```HTML
This is some text.

<style>
	.CSS {
		font-family: "Times New Roman", Times, serif;
  	}
</style>

<div class = "CSS">
	<p>HTML Text</p>
</div>

<script>
	let text = "JavaScript"
	document.write(`${text}`)
</script>
```

Gives:

This is some text.

<style>
	.CSS {
		font-family: "Times New Roman", Times, serif;
  	}
</style>

<div class = "CSS">
	<p>HTML Text</p>
</div>

<script>
	let text = "JavaScript"
	document.write(`${text}`)
</script>

### Images
Images can be shown with the following format: 

```Markdown
![<Alt Text>](<Image Link/Directory>).
```

Alt Text refers to the text displayed either in the corner of the screen or near your mouse when you hover over the image.

The Image Link is straightforward; the Directory refers to the location the image is stored on your device.

### Comments

You can write comments with:

```Markdown
<!-- <Comment> -->
```

They can be used to write notes that readers will not be able to see.

### Code Blocks

For single lines of code, enclose the desired code with the \` or backtick symbol.

```Markdown
`Hi!`
```

For multiple lines or code blocks, enclose the desired code with triple backticks.
The text after the first of the pair of triple backticks is displayed on the top of the code block, specifing the language used.

```Markdown
```PlainText
One
Two
Three```
```

(I don't see why this would come in handy for this blog but this is here if you need it)

## Additional Information
Many more toggles that change displays are can be found in \_config.yml and Butterfly's \_config.yml.

Documentation of Hexo's initial configs: https://hexo.io/docs/configuration
Documentation of Butterfly's configs and their usages: https://butterfly.js.org/en/posts/butterfly-docs-en-theme-config/

You can test your changes on a local domain, which should be http://localhost:4000, with `npx hexo s`. Remember to save the Markdown file or your changes will not display.