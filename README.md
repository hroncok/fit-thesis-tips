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
- [Naučte se používat svůj operační systém](#nau%C4%8Dte-se-pou%C5%BE%C3%ADvat-sv%C5%AFj-opera%C4%8Dn%C3%AD-syst%C3%A9m)
- [Používejte nástroj Arara](#pou%C5%BE%C3%ADvejte-n%C3%A1stroj-arara)
- [Používejte nástroj latexmk](#pou%C5%BE%C3%ADvejte-n%C3%A1stroj-latexmk)
- [Používejte (nějakou) vlnu](#pou%C5%BE%C3%ADvejte-n%C4%9Bjakou-vlnu)
- [Nesázejte ukázky kódu proporciálním písmem](#nes%C3%A1zejte-uk%C3%A1zky-k%C3%B3du-proporci%C3%A1ln%C3%ADm-p%C3%ADsmem)
- [Co můžete, dejte vektorem/textem](#co-m%C5%AF%C5%BEete-dejte-vektoremtextem)
- [Tiskněte na silnější papír](#tiskn%C4%9Bte-na-siln%C4%9Bj%C5%A1%C3%AD-pap%C3%ADr)
- [Vložte zadání práce do PDF](#vlo%C5%BEte-zad%C3%A1n%C3%AD-pr%C3%A1ce-do-pdf)

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

## Naučte se používat svůj operační systém

Pokud na vás TeX křičí, že mu chybí `foo.sty`, naučte se, kde ho vzít.
Na Fedoře stačí udělat `dnf install 'tex(foo.sty)'`,
na jiných distribucích a operačních systémech to půjde nějak podobně.
IMHO není v pořádku se s chybovou hláškou o chybějícím souboru/balíčku TeXu v posledním ročníku FITu nedokázat vypořádat.

## Používejte nástroj [Arara](http://www.texdev.net/2012/04/24/arara-making-latex-files-your-way/)

„Když vám nefungují odkazy a obsahy, projeďte to TeXem ještě jednou.“ Děláte to ručně?
Vyzkoušejte nástroj Arara, který to udělá za vás. Na začátek zdrojáku dejte (něco jako):

```tex
% arara: xelatex
% arara: biber
% arara: xelatex
% arara: xelatex
```

Případně s obyčejným LaTeXem:

```tex
% arara: pdflatex
% arara: bibtex
% arara: pdflatex
% arara: pdflatex
```

A pak použijte příkaz `arara foo.tex`. Arara je papoušek, který papouškuje příkazy za vás.

## Používejte nástroj [latexmk](https://www.ctan.org/pkg/latexmk/)

Výstup LaTeXu je dlouhý a nečitelný, těžko v něm najít to, co stojí za to číst.
LaTeXmk vám hezky napíše, co se podělalo, nebo čemu věnovat pozornost.

```
Latexmk: List of undefined refs and citations:
  Label `hateoas' multiply defined
Biber warning: Duplicate entry key: 'BSD3' in file 'library.bib', skipping ...
Biber warning: I didn't find a database entry for 'foo' (section 0)
```

Zároveň se účelem trochu kryje s Ararou, protože vám taky ten dokument projede víckrát.
Každopádně ho můžete používat i z Arary, například takto:

```tex
% arara: xelatexmk
```

## Používejte (nějakou) vlnu

Vlna vkládá nedělitelné mezery (vln(k)y, `~`) za neslabičné předložky (a i jinam, kam nedělitelná mezera patří, ale ne úplně všude).
Použít vlnu je dobré, protože nemusíte na nedělitelné mezery tolik myslet.

Můžete použít různé vlny: [Olšákovu vlnu](http://petr.olsak.net/ftp/olsak/vlna/),
[xevlnu](https://www.ctan.org/pkg/xevlna) pro XeTex,
chytřejší [luavlnu](https://github.com/michal-h21/luavlna) pro LuaTex (umí tituly, jednotky apod.).

Vlna se dá používat jako řádkový program, kterému soubor předhodíte (vlna), nebo jako balíček přímo ve zdrojáku (luavlna a xevlna):

```tex
% XeLaTeX:
\usepackage{xevlna}

% XeTeX:
\input xevlna.sty
```

(Z Facebooku to vypadá, že si všichni kompilují vlnu sami, tak jen připomenu,
že na Fedoře opět stačí `dnf install /usr/bin/vlna` nebo `dnf install 'tex(xevlna.sty)'`.)

Nejen pokud používáte vlnu manuálně z řádky, je vhodný čas použít na to všechno `Makefile`, což vám ušetří hromadu práce.
To už jistě umíte.

## Nesázejte ukázky kódu proporciálním písmem

...je to hnusné. A dělá to skoro každý.
Nějaký výchozí listing balíček to tak totiž asi má ve výchozím stavu.
Používá proporciální písmo, ale zarovná ho jakoby neproporicálně.
Pokud víte, co je to kerning, vytečou vám oči z důlků.

A vůbec, použijte [minted](https://www.ctan.org/pkg/minted). Zvýrazňuje syntaxi a je mnohem modernější, hezčí a křupavější.
[Tady najdete nějaký použitelný setup](https://github.com/hroncok/diplomka/blob/master/template/FITthesisXE.cls#L68).

```tex
\begin{listing}[htbp]
\caption{\label{code:foo}Minted: Nyní ještě křupavější}
\begin{minted}[bgcolor=codebg]{python}
# ... code here ...
\end{minted}
\end{listing}
```

## Co můžete, dejte vektorem/textem

Výstup z terminálu, log? -- text (*listing*), ne obrázek.

Graf, diagram? -- vektor, ne bitmapa.

Kreslíte nějaké schéma rukou? Použijte výborný [cartoonist](https://github.com/honzajavorek/cartoonist).

Chcete dělat class diagramy, use case schémata a aktivity? Zkuste [yuml](http://yuml.me/)/[scruffy](https://github.com/aivarsk/scruffy).

Děláte vlastní grafy/diagramy/... s popisky? **Použijte v popiskách stejné písmo, jako v práci!**
Ano, je to občas pakárna, zjistit, co to je za písmo, ale pokud používáte XeLaTeX, tak to vlastně víte.

## Tiskněte na silnější papír

Obyčejný papír je částečně průsvitný/průhledný a druhá strana je přes něj vidět.
To nechceš. Dejte pár korun navíc za 100gramový papír. Vypadá to lépe.

## Vložte zadání práce do PDF

Tam, kde je napsané „Sem vložte zadání práce,“ máte vložit zadání práce.
Já vím, je to instrukce těžká na pochopení, a proto většina studentů v odevzdaném PDF nechává tuto instrukci,
což je ostuda. Vložení zadání je jednoduché jak facka:

```tex
\RequirePackage{pdfpages} % v šabloně, jinak \usepackage

\includepdf[pages={1}]{zadani.pdf}
```

Náš odevzdávací systém, který máme všichni tak rádi, to nějak umí udělat za vás,
což je super, ale pokud chcete to PDF použít i jinde, bylo by stejně lepší to udělat ručně.
Jak to ten sytém dělá (jestli vymění první stranu, nebo jen první stranu, která obsahuje magický text),
těžko říct, protože je to magie (proprietární black box).
O důvod víc, proč to udělat v TeXu.
