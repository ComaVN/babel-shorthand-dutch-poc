# PoC for LaTeX Babel package shorthand problem in Dutch

This shows the [issue](https://github.com/latex3/babel/issues/140) when using the `shorthands=off` parameter to the Babel package for the Dutch language

```
$ latex doc.tex
This is pdfTeX, Version 3.14159265-2.6-1.40.20 (TeX Live 2019/Debian) (preloaded format=latex)
 restricted \write18 enabled.
entering extended mode
(./doc.tex
LaTeX2e <2020-02-02> patch level 2
L3 programming layer <2020-02-14>
(/usr/share/texlive/texmf-dist/tex/latex/base/article.cls
Document Class: article 2019/12/20 v1.4l Standard LaTeX document class
(/usr/share/texlive/texmf-dist/tex/latex/base/size10.clo))
(/usr/share/texlive/texmf-dist/tex/generic/babel/babel.sty
(/usr/share/texlive/texmf-dist/tex/generic/babel/switch.def)
(/usr/share/texlive/texmf-dist/tex/generic/babel-dutch/dutch.ldf
(/usr/share/texlive/texmf-dist/tex/generic/babel/babel.def
(/usr/share/texlive/texmf-dist/tex/generic/babel/txtbabel.def))))
(/usr/share/texlive/texmf-dist/tex/latex/l3backend/l3backend-dvips.def)
(./doc.aux) (/usr/share/texlive/texmf-dist/tex/latex/base/omscmr.fd)
! Undefined control sequence.
\listfigurename ->L"
                    yst van figuren
l.16 ...h}listfigurename in Dutch: \listfigurename
```

`minimal.tex` is the minimal document that fails for me (in v3.61)
)
Using the other `\usepackage` line does work as expected (but enables shorthands)
