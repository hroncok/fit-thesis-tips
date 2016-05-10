# FIT ČVUT thesis tips
Opinionated tips based guide for writing bachalor and magister diploma thesis on [FIT ČVUT](http://fit.cvut.cz/). 
It's written in Czech, bacuse that way it can attract more readers from FIT ČVUT.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Používejte XeLaTeX](#pou%C5%BE%C3%ADvejte-xelatex)
- [Věnujte minimálně den přípravě sazby (před samotným psaním)](#v%C4%9Bnujte-minim%C3%A1ln%C4%9B-den-p%C5%99%C3%ADprav%C4%9B-sazby-p%C5%99ed-samotn%C3%BDm-psan%C3%ADm)
- [Oficiální šablona je doporučení](#ofici%C3%A1ln%C3%AD-%C5%A1ablona-je-doporu%C4%8Den%C3%AD)
- [Používejte git](#pou%C5%BE%C3%ADvejte-git)
- [Tvořte free (open-source) software](#tvo%C5%99te-free-open-source-software)

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

## Používejte git

Nejen pro kód implementační části, i pro text vaší práce (každou tu věc samozřejmě v samostatném repozitáři).
Pomůže vám to, když něco přestane fungovat. Naučte se používat `git bisect`, bude se to hodit.

Pokud použijete GitHub nebo školní GitLab, váš vedoucí vám může přímo v jednotlivých commitech komentovat změny
a nemusíte ho otravovat a posílat mu dokola e-mailem PDFko :)

Ideálně použijte repozitář v režimu public, pokud nejste vázání nějakou smlouvou o výhradní licenci.
Z vašeho zdrojáku mohou spolužáci čerpat tipy, jak něco udělat, a vaše práce stejně bude nakonec veřejná.

Tady jen pozor, aby vám kamarádi nebo vedoucí neposílali Pull Requesty, práci musíte vypracovat sami.

## Tvořte free (open-source) software

Tady záleží na názoru, ale já v 3D labu chci po svých studentech, aby vytvářeli implementační část práce jako svobodný software.
Pokud neděláte práci pro firmu, která vám to zakáže, je to dobrá volba, projekt pak uvidí například firmy, ve kterých (třeba) budete chtít pracovat.

Zvolte si licenci jakou chcete -- kašlete na prohlášení, máte právo (pokud neuzavíráte s někým smlouvu o exkluzivitě) odevzdat škole práci s nějakým prohlášením a tu stejnou práci dát na GitHub s MIT/GPL/... licencí.
Pokud chcete použít prohlášení, které se podobá GPL, zvolte prohlášení 4
(*...osoby jsou oprávněny Dílo užít jakýmkoli způsobem, který nesnižuje hodnotu Díla a za jakýmkoli účelem ...
licenci alespoň ve výše uvedeném rozsahu a zároveň zpřístupnit zdrojový kód takového díla...*).

V repozitáři se softwarem používejte anglické commit message, komentáře, proměnné. Dejte tam anglické README.
Kolemjdoucí by neměl poznat, že to je implementační část české bakalářky/diplomky (pokud to tam samozřejmě nenapíšete).
