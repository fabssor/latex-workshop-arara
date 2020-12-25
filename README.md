# latex-workshop-arara
Template for Latex (LuaTex) with [arara](https://ctan.org/pkg/arara?lang=de) as build system.

## What is it?
Minimal template for LaTex with arara as build system. Also this will smoothly integrate into the VS Code Plugin [Latex-Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop).

For the typesetting system LuaTex is used. Since it seems to me is the most future proof.

## Why arara?
I hate guesswork. So arara gives me full control over the build process and I know what is done when. 

This is not the case with other latex build automation tools like [latexmk](https://www.ctan.org/pkg/latexmk).

## How to build
To build the document you can run in your terminal

```sh
arara -p build Document.tex
```

or clean all build files with

```sh
arara -p clean Document.tex
```

This will also clear the `Tikz` folder and remove the PDF-file.

Or you can use the Latex-Workshop Plugin. Just open one tex-file in your editor, navigate to the plugin shortcut on the right.

![Latex Workshop Commands](/images/latex-workshop-commands.png?raw=true)

## What can it do?

- LuaTex is used as the typesetting system.
- The [`glossaries-extra`](https://ctan.org/pkg/glossaries-extra?lang=en) package is used for a glossary. The entries are stored in a bib-file and bib2gls is used to convert this file.
- All literature is also stored in a bib-file. [`biblatex`](https://ctan.org/pkg/biblatex?lang=en) with backend `biber` is used for this.
- Also [`tikz`](https://ctan.org/pkg/tikz?lang=en) is already supported. To speed up the build process `tikz-externalize` is used and all your graphics will be exported to the `Tikz` folder.

To manage the bib-files you can do it by hand or for example use [JabRef](https://www.jabref.org/).
