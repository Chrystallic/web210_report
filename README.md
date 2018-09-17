# web210_report

## Nothing to see here

Om du ikke klarer å bygge rapporten, sjekk at du har pygemntize pakken innstallert


Du må også aktivere --shell-escape under bygging av PDF filen dette gjøres under
File -> Preferences -> Settings (søk etter Latex Compile) og trykk på "Edit in settings.json"

Legg til følgende på høyre side:
```
"latex-workshop.latex.tools": [
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "--shell-escape", // added arg to default
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "%DOC%"
            ]
        },
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "--shell-escape", // added arg to default
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": [
                "%DOCFILE%"
            ]
        }
    ]
```

Dersom dere vil lese mer om minted pakken i Latex, så kan dere sjekke ut [denne linken](ftp://ftp.dante.de/tex-archive/macros/latex/contrib/minted/minted.pdf).
