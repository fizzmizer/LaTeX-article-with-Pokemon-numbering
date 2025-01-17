# [LaTeX-article-with-Pokemon-numbering](https://naereen.github.io/LaTeX-article-with-Pokemon-numbering/)

Experiment to have a LaTeX article class which includes a small Pokémon image, in every page (on the bottom right or left), instead of numbering with indexes!

## How to use this
1. First, [don't use this code](https://seriously.dontusethiscode.com/), it's stupid.
2. Now, to use it:
   - Git clone this repository,
   - Copy the [`icons`](icons) and [`pokemonnumbering.sty`](pokemonnumbering.sty) in your own directory, wherever you are writing your LaTeX document,
   - Use this LaTeX code in your own document:
     ```tex
     \usepackage{pokemonnumbering}  % default
     ```
   - After your introduction, abstract etc, when you want to start numbering your pages with Pokémon, use this LaTeX code:
     ```tex
     \pokemonnumbering
     ```
   - And don't write a document with more than ~~151~~807 pages!
   - Compile with `pdflatex`, `xelatex` or `luatex` (it must support PNG images).

## Demo
See any of these PDF files (not gitted, on my website):

- [test](https://perso.crans.org/besson/publis/LaTeX-article-with-Pokemon-numbering.git/test.pdf) is the default document,
- [test_left](https://perso.crans.org/besson/publis/LaTeX-article-with-Pokemon-numbering.git/test_left.pdf) shows the `left` option,
- [test_right](https://perso.crans.org/besson/publis/LaTeX-article-with-Pokemon-numbering.git/test_right.pdf) shows the `right` option (is the same as the default document),
- [test_rotate](https://perso.crans.org/besson/publis/LaTeX-article-with-Pokemon-numbering.git/test_rotate.pdf) shows the `rotate` option,
- [test_lorem](https://perso.crans.org/besson/publis/LaTeX-article-with-Pokemon-numbering.git/test_lorem.pdf) test with a dummy text.

## Screenshots
> Here are a few examples:


![screenshots/demo1.png](screenshots/demo1.png)

![screenshots/demo2.png](screenshots/demo2.png)

![screenshots/demo3.png](screenshots/demo3.png)

![screenshots/demo4.png](screenshots/demo4.png)

![screenshots/demo5.png](screenshots/demo5.png)

----

## *How I did that?*

See [pokemonnumbering.sty](pokemonnumbering.sty):

- I use [`fancyhdr`](https://en.wikibooks.org/wiki/LaTeX/Customizing_Page_Headers_and_Footers#Customizing_with_fancyhdr) to add a image to the bottom right or left.
- I use `adjustbox` package, with `export` option, to force the image to be flushed right or left.


Others things:

- This [Makefile](Makefile) contains some build rule to generate the examples. It takes a few minutes to generate all of them.


For the [demo document](test.tex):

- This [bash script (get_data.sh)](src/get_data.sh) downloads HTML pages from [this website](https://www.math.miami.edu/~jam/azure/pokedex/species/001.htm), converts them to Markdown, extract the text, and save the data for each Pokémon as a json file. See [1.json](src/1.json) for example (for Bulbasaur).
- This [Python script (json2tex.py)](src/json2tex.py) converts this json file to a LaTeX file, using [this template](src/_template.tex). See [1.tex](src/1.tex) for example (for Bulbasaur).


----

## Options
By default, the Pokémon images are inserted on the bottom right corner.
The package can be loaded with an option:

- `right` : by default,
```tex
\usepackage[right]{pokemonnumbering}  % default
```

- `left` : insert them in the bottom left corner instead,
```tex
\usepackage[left]{pokemonnumbering}
```

- `rotate` : rotate the image by 20° (clock-wise if right, counter clock-wise if left),
```tex
\usepackage[rotate]{pokemonnumbering}
```


----

## :scroll: License ? [![GitHub license](https://img.shields.io/github/license/Naereen/LaTeX-article-with-Pokemon-numbering.svg)](https://github.com/Naereen/LaTeX-article-with-Pokemon-numbering/blob/master/LICENSE)
[MIT Licensed](https://lbesson.mit-license.org/) (file [LICENSE](LICENSE)).
© [Lilian Besson](https://GitHub.com/Naereen), 2018.

[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/LaTeX-article-with-Pokemon-numbering/graphs/commit-activity)
[![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)](https://GitHub.com/Naereen/ama)
[![Analytics](https://ga-beacon.appspot.com/UA-38514290-17/github.com/Naereen/LaTeX-article-with-Pokemon-numbering/README.md?pixel)](https://GitHub.com/Naereen/LaTeX-article-with-Pokemon-numbering/)

[![Contains-Pokémon](https://img.shields.io/badge/Contains-Pokémons-7fb78a.svg)](https://github.com/Naereen/LaTeX-article-with-Pokemon-numbering/tree/master/icons/)

[![ForTheBadge built-with-swag](https://ForTheBadge.com/images/badges/built-with-swag.svg)](https://GitHub.com/Naereen/)

[![ForTheBadge uses-badges](https://ForTheBadge.com/images/badges/uses-badges.svg)](https://ForTheBadge.com)
[![ForTheBadge uses-git](https://ForTheBadge.com/images/badges/uses-git.svg)](https://GitHub.com/)
[![ForTheBadge uses-css](https://ForTheBadge.com/images/badges/uses-css.svg)](https://ForTheBadge.com)
[![ForTheBadge uses-html](https://ForTheBadge.com/images/badges/uses-html.svg)](https://ForTheBadge.com)
[![ForTheBadge uses-js](https://ForTheBadge.com/images/badges/uses-js.svg)](https://ForTheBadge.com)
