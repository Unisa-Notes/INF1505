# UNISA INF1505 Notes

This repo contains the LaTeX files needed to compile a set of notes for the course **Introduction to Business Information Systems** at the University of South Africa.

## Accessing the Notes

A PDF can be generated using [latexmk](https://ctan.org/pkg/latexmk), or any other LaTeX compiler. If you want to access pre-generated PDFs, please check the [Releases](https://github.com/Unisa-Notes/INF1505/releases) section on the sidebar.

## Contributing
Please fork this repo, make your changes, and then open a pull request.

## The Code
### The Structure
- The file [notes.tex](notes.tex) contains the general structure and order of the files. Building this file should build all the other `.tex` files, and include them in one `.pdf` called `notes.pdf`
- Each part has a separate folder for the chapters in that part. These are contained in the [units](./units) folder.
- Each chapter is a separate `tex` file, stored within the folder for that part.
- If the chapter contains images, these are contained in a folder with the same number as the chapter. For example: [Chapter 7 Images](units/part03/chapter07/).
- The styles, commands and packages used are in the package file [notestyles.sty](notestyles.sty)

### Packages Used
TeX packages that have been used are:
- [amsmath, amssymb](https://www.ctan.org/pkg/amsmath): Used for mathematical symbols and environments
- [babel](https://ctan.org/pkg/babel): Use description environment, and chapter renaming
- [bookmark](https://ctan.org/pkg/bookmark): Set pdf bookmarks accurately
- [changepage](https://ctan.org/pkg/changepage): Allow paragraphs to be indented
- [enumitem](https://ctan.org/pkg/enumitem): Used to improve the way lists are displayed
- [fancyhdr](https://ctan.org/pkg/fancyhdr): Improve header and footer display
- [fontenc](https://ctan.org/pkg/fontenc), [charter](https://ctan.org/pkg/charter), [inconsolata](https://ctan.org/pkg/inconsolata), [cabin](https://ctan.org/pkg/cabin), [newtxmath](https://ctan.org/pkg/newtx), [bm](https://ctan.org/pkg/bm): Font display
- [geometry](https://ctan.org/pkg/geometry): Used for document margins
- [graphicx](https://ctan.org/pkg/graphicx): Used for images
- [hyperref](https://ctan.org/pkg/hyperref): Add PDF bookmarks
- [hyphsubst](https://ctan.org/pkg/hyphsubst): Prevent hyphenation on line ends
- [parskip](https://ctan.org/pkg/parskip): Set proper default values for paragraph separation
- [subfiles](https://ctan.org/pkg/subfiles): Allow `tex` files to be written separately, but built together
- [tabularray](https://ctan.org/pkg/tabularray): Better table display and management.
  * Also uses libraries to simulate [booktabs](https://ctan.org/pkg/booktabs) and [varwidth](https://ctan.org/pkg/varwidth)
- [tcolorbox](https://ctan.org/pkg/tcolorbox), [adjustbox](https://ctan.org/pkg/adjustbox): Create colored boxes for different environments
- [tikz](https://ctan.org/pkg/tikz): Used for images.
  * [forest](https://ctan.org/pkg/forest): Used for tree diagrams
  * [circledsteps](https://ctan.org/pkg/circledsteps): Used to circle characters
- [xcolor](https://ctan.org/pkg/xcolor): Used to get more colours
- [xstring](https://ctan.org/pkg/xstring): Analyse strings given as arguments to an environment

### Commands Added
For intellisense, a list of the commands is added in the [package_intellisense](./package_intellisense/) folder. These have been written in formats that can be understood by different LaTeX tools.

#### Commands
- `addfile [input] {<filename>}`: Include or input the file into the document. By default, it includes the file, the option `input` can be given to input it instead.
- `concept {text}`: Mark specific text as a concept to be learned. Puts the text in bold.
- `question {text}`: Mark specific text as a question. Puts the text in bold, and adds extra spacing.
- `rulebookend`: Insert a decorative horizontal line at the end of the text.
- `rulechapterend`: Insert a decorative horizontal line at the end of each unit.

#### Environments
- `definition {title}`: Coloured box used for highlighting important concepts.
- `example`: Coloured box used to highlight examples.
- `exercise {title}`: Coloured box used to highlight exercises.
- `indentparagraph`: Indent selected text to the left.
- `sidenote`: Coloured box used to indicate extra information.

---