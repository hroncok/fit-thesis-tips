# FIT ČVUT thesis tips
Opinionated tips based guide for writing bachalor and magister diploma thesis on [FIT ČVUT](http://fit.cvut.cz/). 
It's written in Czech, bacuse that way it can attract more readers from FIT ČVUT.

## Používejete [XeLaTeX](http://tex.stackexchange.com/questions/3393/what-is-xetex-exactly-and-why-should-i-use-it)

Unicode je dnes standard, přestaňte používat obyčejný LaTeX, který s ním neumí pracovat.
Určitě vás nebaví neustálě řešit `l\'etající akcent`, T1 kódování a podobné výmysly minulého tisíciletí.

XeLaTeXu se nemusíte bát, přestože oficiální šablona je pro obyčejný LaTeX, její úprava je poměrně triviální.
Oficiální šablona neexistuje, ale můžete se inspirovat třeba [touto](https://github.com/hroncok/bakalarka/blob/master/template/FITthesisXE.cls).
Pokud se naučíte šablonu mírně upravit, získáte i znalosti potřebné na to, abyste fixli nějaký případný problém, který se časem objeví.

Pak můžete ve zdrojáku používat normální Unicode, háčkyčárky, „uvozovky“ bez maker, Русский, &#x1f4a9;, cokoliv.

(Pokud používáte TeX bez LaTeXu, stačí použít XeTeX.)
