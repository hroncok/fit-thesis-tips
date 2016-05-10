# FIT ČVUT thesis tips
Opinionated tips based guide for writing bachalor and magister diploma thesis on [FIT ČVUT](http://fit.cvut.cz/). 
It's written in Czech, bacuse that way it can attract more readers from FIT ČVUT.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Používejte XeLaTeX](#pou%C5%BE%C3%ADvejte-xelatex)
- [Věnujte minimálně den přípravě sazby (před samotným psaním)](#v%C4%9Bnujte-minim%C3%A1ln%C4%9B-den-p%C5%99%C3%ADprav%C4%9B-sazby-p%C5%99ed-samotn%C3%BDm-psan%C3%ADm)
- [Oficiální šablona je doporučení](#ofici%C3%A1ln%C3%AD-%C5%A1ablona-je-doporu%C4%8Den%C3%AD)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Používejte [XeLaTeX](http://tex.stackexchange.com/questions/3393/what-is-xetex-exactly-and-why-should-i-use-it)

Unicode je dnes standard, přestaňte používat obyčejný LaTeX, který s ním neumí pracovat.
Určitě vás nebaví neustálě řešit `l\'etající akcent`, T1 kódování a podobné výmysly minulého tisíciletí.

XeLaTeXu se nemusíte bát, přestože oficiální šablona je pro obyčejný LaTeX, její úprava je poměrně triviální.
Oficiální šablona neexistuje, ale můžete se inspirovat třeba [touto](https://github.com/hroncok/bakalarka/blob/master/template/FITthesisXE.cls).
Pokud se naučíte šablonu mírně upravit, získáte i znalosti potřebné na to, abyste fixli nějaký případný problém, který se časem objeví.

Pak můžete ve zdrojáku používat normální Unicode, háčkyčárky, „uvozovky“ bez maker, Русский, &#x1f4a9;, cokoliv.

Stejně tak pro citace používejte [Biber](http://biblatex-biber.sourceforge.net/), který také podporuje Unicode.

(Pokud používáte TeX bez LaTeXu, stačí použít XeTeX.)

## Věnujte minimálně den přípravě sazby (před samotným psaním)

Setkávám se s tím, že studenti něco nějak napíšou a před odevzdáním se to snaží naprasit do školní latexové šablony.
Doporučuji předtím, než začnete psát tomu (Xe)LaTexu minimálně den věnovat a všechno si hezky připravit.
Může se to zdát jako ztráta času, ale pokud budete průběžně sázet, hned uvidíte, že něco vypadá blbě, že by bylo lepší to udělat takhle apod.

Sazbě je třeba se samozřejmě věnovat i na samotném konci, zkontrolovat, že vám nic nepřetéká z řádku, že všechno vypadá, jak má, apod.

## Oficiální šablona je doporučení

„Ale ono to pak vypadá jinak než v šabloně.“

„Šablona mi tam napsala v českém textu *Listing*, to mám nechat?“

Nehroťte to, šablona je **doporučení**, pokud něco uděláte jinak a budete k tomu mít dobrý důvod
(vypadá to líp, je to modernější, lépe se s tím pracuje, je to čitelnější apod.), je to více než v pořádku.

BTW Šablona samotná je na [školním GitLabu](https://gitlab.fit.cvut.cz/guthondr/ThesisTemplate)
a není problém poslat tam Merge Request (gitlabí ekvivalent githubího Pull Requestu), pokud máte úpravu, která je prospěšná všem.
