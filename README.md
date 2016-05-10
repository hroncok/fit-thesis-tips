# FIT ČVUT thesis tips
Opinionated tips based guide for writing bachalor and magister diploma thesis on [FIT ČVUT](http://fit.cvut.cz/). 
It's written in Czech, bacuse that way it can attract more readers from FIT ČVUT.

## Používejte [XeLaTeX](http://tex.stackexchange.com/questions/3393/what-is-xetex-exactly-and-why-should-i-use-it)

Unicode je dnes standard, přestaňte používat obyčejný LaTeX, který s ním neumí pracovat.
Určitě vás nebaví neustálě řešit `l\'etající akcent`, T1 kódování a podobné výmysly minulého tisíciletí.

XeLaTeXu se nemusíte bát, přestože oficiální šablona je pro obyčejný LaTeX, její úprava je poměrně triviální.
Oficiální šablona neexistuje, ale můžete se inspirovat třeba [touto](https://github.com/hroncok/bakalarka/blob/master/template/FITthesisXE.cls).
Pokud se naučíte šablonu mírně upravit, získáte i znalosti potřebné na to, abyste fixli nějaký případný problém, který se časem objeví.

Pak můžete ve zdrojáku používat normální Unicode, háčkyčárky, „uvozovky“ bez maker, Русский, &#x1f4a9;, cokoliv.

(Pokud používáte TeX bez LaTeXu, stačí použít XeTeX.)

## Věnujte minimálně den přípravě sazby (před samotným psaním)

Setkávám se s tím, že studenti něco nějak napíšou a před odevzdáním se to snaží naprasit do školní latexové šablony.
Doporučuji předtím, než začnete psát tomu (Xe)LaTexu minimálně den věnovat a všechno si hezky připravit.
Může se to zdát jako ztráta času, ale pokud budete průběžně sázet, hned uvidíte, že něco vypadá blbě, že by bylo lepší to udělat takhle apod.

Sazbě je třeba se samozřejmě věnovat i na samotném konci, zkontrolovat, že vám nic nepřetéká z řádku, že všechno vypadá, jak má, apod.
