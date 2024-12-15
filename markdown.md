---
layout: default
title: Markdown
permalink: Markdown
---
Put the code below at the VERY top of the Markdown file to change the page's properties. Search will NOT work without this.
```yaml
---
layout: default
title: Markdown
permalink: Markdown
---
```
[***Old Version***](https://just-the-docs.github.io/just-the-docs/docs/index-test/){: .btn }

This is text.
This is text one linebreak below. It will appear on the same line.

This is text TWO linebreaks below. It will NOT appear on the same line.

~~This is striked text, using two tildes, delet this.🔫~~

*This is italic text, using one asterisk.*

_You can also use one underscore._

**This is bold text, using two asterisks.**

*This is italic, but you can add **two asterisks to turn the italic bold, and end both with three asterisks.***

*~~You can do the same~~ in reverse, and **even** in between.*

> This is a quote, using a GreaterThan sign.

Smol text at the <sub>bottom</sub> using HTML subscript tags.

Smol text at the <sup>top</sup> using HTML superscript tags.

Use a colon one line below to describe a term.
: Description of the term.

Add `{: .label .label-color }`, replacing color with one of the colors below to create labels.

Blue
{: .label .label-blue }
Green
{: .label .label-green }
Yellow
{: .label .label-yellow }
Red
{: .label .label-red }
**Purple and bold!?**
{: .label .label-purple }

Use `{: .fw-300 }` to set the font weight to 300.
{: .fw-300 }
Or 700.
{: .fw-700 }

Use `{: .fs-1 }` to set the font size to 1.
{: .fs-1 }
Or 10.
{: .fs-10 }

<!- Use HTML comment tags to make something invisible. This is visible because there's only one dash instead of two. ->

<!-- Bruh. -->

# Use a number sign to create a linkable header

## Add more number signs to make smaller headers

### An even smaller header

#### So smol

##### pls halp

###### a

1. Use a number, a period, and space
2. To make an ordered list.

* Use an asterisk and space
* To make an unordered list.

- You can also use
- A dash and space instead.

* [ ] Add square brackets and a space next to an unordered item to create checkmarks.
* [x] You can add an x (lowercase) instead of a space to mark the item done.

1. You can use 1
2. For every row
3. To allow Markdown
4. To number the list
5. Automatically.

* Use tabs
  * To add layers
    * To the unordered list.

Nesting an unordered list inside an ordered list inside an unordered list.

- level 1 item (Unordered)
  1. level 2 item (Ordered)
  1. level 2 item (Ordered)
    - level 3 item (Unordered)
    - level 3 item (Unordered)
- level 1 item (Unordered)
  1. level 2 item (Ordered)
  1. level 2 item (Ordered)
    - level 3 item (Unordered)
    - level 3 item (Unordered)
      1. level 4 item (Ordered)
      1. level 4 item (Ordered)
    - level 3 item (Unordered)
    - level 3 item (Unordered)
- level 1 item (Unordered)

Asterisk, space, asterisk, space, asterisk...
* * *
...creates a horizontal bar.

`Use grave accents for tiny code or keywords.`

```js
// Use three grave accents and the language to create code blocks. Here's some meme js.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```md
Specify md to display normal text. Long lines outside of code blocks wrap around, but long lines inside code blocks do not. This is a long enough text to demonstrate this. Did you know that in terms of Human to Pokemon breeding Vaporeon is- ok sorry.
```

To create a link, put the name of the link between square parentheses, then put the link itself between round parentheses, with no spaces.

[This is a link to a local Markdown page.](./index.md)

[This is a link to another webpage.](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

Add `{: .btn }` next to ) to create a button.
[The two links above,](./index.md){: .btn }
[But as buttons.](https://www.youtube.com/watch?v=dQw4w9WgXcQ){: .btn }

[You can link files too. If the file can't display on a browser window, a download will start.](https://static.f-list.net/images/avatar/tokumei%20kii.png)

Add ! at the beginning before the square parenthesis to embed. You cannot embed links or webpages, only files. There's no need to put anything inside the square parenthesis when you're embedding.

This is a smol PNG one line below.
![](https://static.f-list.net/images/avatar/tokumei%20kii.png)

This is a l o r g e PNG two lines below.

![](./Comparisons/Zorua Zoroark.png)

Embedded files cannot be bigger than 10MB, and must be either .PNG, .JPG, .SVG, .LOG, .TXT, .PDF, or .ZIP.

Animated files such as .GIF, .MP4, or .MOV, will only embed properly on Desktop (x86) Chromium and Firefox.

|Use vertical bars to create a table.|Use monospace fonts to avoid confusion.|
|Cells can vary in width|And do not need to be perfectly aligned within columns.|

| Left                        | Center           |              Right |
|:----------------------------|:----------------:|-------------------:|
| To tell text where to align | Use :- :-: or -: | On the second row. |

{% assign row = site.data.markdown[0] %}
{% for row in site.data.markdown %}{% if forloop.first %}{% for pair in row %}|{{ pair[0] }}{% endfor %}|
{% for pair in row %}|:-:{% endfor %}|{% endif %}
|{% for pair in row %}{{ pair[1] }}|{% endfor %}{% endfor %}

You can make footnotes with a caret and a number, between square brackets[^1].
You can also use whatever name you want instead of a number.[^Name]

[^1]: Add a colon (NOT semicolon) to invoke the footnote, make sure it's at the bottom of the page and at the beginning of the line or it won't work.
[^Name]: Although it will still display as a number with certain themes.
