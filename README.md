# rentry

<a href="https://rentry.co/"><img width="110" height="110" src="https://rentry.co/static/logo-border-fit.png" align="right" alt="rentry.co markdown pastebin"></a>

[Rentry.co](https://rentry.co) ist ein Pastebin- / Publishing-Service von [@radude](https://github.com/radude) mit Vorschau. Schnell, einfach, ohne Anmeldung und sogar kostenlos. Aber mit Spionage durch Google-Analytics!  

Dieses Repositorium enth&auml;lt ein einfaches Skript, welches das Ver&ouml;ffentlichen und Editieren von der Kommandozeile aus erlaubt.

  
## Installation

##### Manuell:  
```sh
wget https://raw.githubusercontent.com/radude/rentry/master/rentry -O ./rentry && chmod +x ./rentry
```

##### Mit [PyPI](https://pypi.python.org/pypi/rentry):
```sh
pip3 install rentry
```

## Anwendung:

```console
$ rentry --help

Befehl: rentry {new | edit | raw} {-h | --help} {-u | --url} {-p | --edit-code} Mein_Text

Befehls-Parameter:
  new   Ver&ouml;ffentlicht eine neue Rentry.co-Seite
  edit  Editiere eine existierende Rentry.co-Seite
  raw   Zeigt den puren Markdown-Text einer existierenden Rentry.co-Seite
  
Optionen:
  -h, --help                 show this help message and exit
  -u, --url       URL        URL for the entry, random if not specified
  -p, --edit-code EDIT-CODE  edit code for the entry, random if not specified
    
Examples:
  rentry new 'markdown text'               # new entry with random url and edit code
  rentry new  -p pw -u example 'text'      # with custom edit code and url 
  rentry edit -p pw -u example 'text'      # edit the example entry
  cat FILE | rentry new                    # read from FILE and paste it to rentry
  cat FILE | rentry edit -p pw -u example  # read from FILE and edit the example entry
  rentry raw -u example                    # get raw markdown text
  rentry raw -u https://rentry.co/example  # -u accepts absolute and relative urls
    
```

##### URL

Optional URL can be set (`-u, --url URL`)  
It goes rentry.co/HERE. If no Url was set then random Url will be generated automatically.

##### Edit code

Optional edit code can be set (`-p, --edit-code EDIT-CODE`)  
It can be used to edit the entry later. If no edit code was set then random edit code will be generated automatically. Generated edit code will be shown to you only once, so remember it or save it. You can share this code with anyone so a group of people can edit the same entry.

