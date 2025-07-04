# About

This is a translation of
["Learning Zig" book](https://www.openmymind.net/learning_zig/)
by [Karl Seguin](https://github.com/karlseguin) into Russian.

# License

Distributed under the terms of
[Attribution-NonCommercial-ShareAlike 4.0 International](http://creativecommons.org/licenses/by-nc-sa/4.0/)

# Converting from `md` to other formats

## epub

```
cd src/
pandoc --syntax-definition="zig.xml" --highlight-style="zig.theme" zig.yaml *.md -o learning-zig.ru.epub
```

## docx

```
cd src/
pandoc --syntax-definition="zig.xml" --highlight-style="zig.theme" *.md -o learning-zig.ru.docx
```

## latex
```
pandoc --syntax-definition="zig.xml" \
       --highlight-style="zig.theme" \
       *.md -o learning-zig.ru.tex \
       --standalone \
       --to=latex \
       -V documentclass=report \
       -V lang=ru \
       -V mainfont="DejaVu Serif" \
       -V monofont="DejaVu Sans Mono" \
       -V geometry:"left=10mm, right=10mm, top=20mm, bottom=25mm" \
       --toc \
       --number-sections
```
