+++
title = "FCM 146 Example Slide Deck"
date = 2019-06-09T10:40:11+02:00
outputs = ["Reveal"]
+++

# FCM 146 Example Slide Deck with hugo-reveal

---

# What is Reveal.js

- {{% fragment %}}An HTML-based presentation framework{{% /fragment %}}
- {{% fragment %}}Also available through a visual editor at [slides.com](slides.com){{% /fragment %}}

---

{{% section %}}

# Code

The following are a sample of various code formatting options.

---

## Python

The below code is a python generator function, updated for Python 3 from [here](https://stackoverflow.com/a/25706933).

~~~python
def getPrimes(n):
    if n <= 2:
        raise StopIteration
    yield 2
    for i in range(3, n, 2):
        for x in range(3, int(i**0.5)+2, 2):
            if not i % x:
                break
        else:
            yield i

p = getPrimes(100)
primes = [i for i in p]

print(primes)
~~~

---

## Bash

Below is my script for converting markdown to PDF using pandoc.

~~~bash
#!/bin/bash

pandoc --metadata pagetitle="${1/.md//}" -f markdown -t html5 "$1" --pdf-engine wkhtmltopdf --css ~/pandocPDF/tufte.css -o "${1/.md/.pdf}";
~~~

---

## Markdown

It's even possible to show snippets of markdown.

~~~markdown
## Markdown

It's even possible to show snippets of markdown.
~~~

{{% /section %}}

---

# Screenshots

![Python example](/carbon-smaller.png)

---

# Embed YouTube

{{< youtube id="RFPnZayG0VI" >}}

{{% note %}}
The above video is 40 Fingers performing Bohemian Rhapsody.
{{% /note %}}

---

{{% section %}}

# Speaker notes

You can create speaker notes by wrapping some text in the note shortcode (remove the spaces between the two opening curly braces).

~~~
{ {% note %}}{ {% /note %}}
~~~

To see them when presenting, press the `s` key.

---

## Example

{{< image speaker-notes-example Resize 650x >}}

{{% /section %}}

---

# References

- [https://themes.gohugo.io/reveal-hugo/](https://themes.gohugo.io/reveal-hugo/) - Page detailing the hugo theme.
- [https://revealjs.com/](https://revealjs.com/) - The Reveal.JS demo page.
- [https://stackoverflow.com/a/25706933](https://stackoverflow.com/a/25706933) - Prime number generator example in Python 2 (updated to 3 for this example.)