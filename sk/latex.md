---
contributors:
    - ["Chaitanya Krishna Ande", "http://icymist.github.io"]
    - ["Colton Kohnke", "http://github.com/voltnor"]
    - ["Sricharan Chiruvolu", "http://sricharan.xyz"]
translators:
    - ["Terka Slanináková", "http://github.com/TerkaSlan"]
---

```tex
% Všetky komentáre začínajú s %
% Viac-riadkové komentáre sa nedajú urobiť

% LaTeX NIE JE WYSIWY ("What You See Is What You Get") software ako MS Word, alebo OpenOffice Writer

% Každý LaTeX príkaz začína s opačným lomítkom (\)

% LaTeX dokumenty začínajú s definíciou typu  kompilovaného dokumentu
% Ostatné typy sú napríklad kniha (book), správa (report), prezentácia (presentation), atď.
% Možnosti dokumentu sa píšu do [] zátvoriek. V tomto prípade tam upresňujeme veľkosť (12pt) fontu.
\documentclass[12pt]{article}

% Ďalej definujeme balíčky, ktoré dokuemnt používa.
% Ak chceš zahrnúť grafiku, farebný text, či zdrojový kód iného jazyka, musíš rozšíriť možnosti LaTeXu dodatočnými balíčkami.
% Zahŕňam float a caption. Na podporu slovenčiny treba zahrnúť aj utf8 balíček.
\usepackage{caption}
\usepackage{float}
\usepackage[utf8]{inputenc}
% Tu môžme definovať ostatné vlastnosti dokumentu!
% Autori tohto dokumentu, "\\*" znamená "choď na nový riadok"
\author{Chaitanya Krishna Ande, Colton Kohnke \& Sricharan Chiruvolu, \\*Preklad: Terka Slanináková}
% Vygeneruje dnešný dátum
\date{\today}
\title{Nauč sa LaTeX za Y Minút!}
% Teraz môžme začať pracovať na samotnom dokumente.
% Všetko do tohto riadku sa nazýva "Preambula" ("The Preamble")
\begin{document} 
% ak zadáme položky author, date a title, LaTeX vytvorí titulnú stranu.
\maketitle

% Väčšina odborných článkov má abstrakt, na jeho vytvorenie môžeš použiť preddefinované príkazy.
% Ten by sa mal zobraziť v logickom poradí, teda po hlavičke,
% no pred hlavnými sekciami tela.. 
% Tento príkaz je tiež dostupný v triedach article a report.
% Tzv. makro "abstract" je fixnou súčasťou LaTeXu, ak chceme použiť abstract
% a napísať ho po slovensky, musíme ho redefinovať nasledujúcim príkazom
\renewcommand\abstractname{Abstrakt}

\begin{abstract}
LaTeX dokumentácia v LaTeXe! Aké netradičné riešenie cudzieho nápadu!
\end{abstract}

% Príkazy pre sekciu sú intuitívne
% Všetky nadpisy sekcií sú pridané automaticky do obsahu.
\section{Úvod}
Čaute, volám sa Colton a spoločne sa pustíme do skúmania LaTeXu (toho druhého)!

\section{Ďalšia sekcia}
Toto je text ďalšej sekcie. Myslím, že potrebuje podsekciu.

\subsection{Toto je podsekcia} % Podsekcie sú tiež intuitívne.
Zdá sa mi, že treba ďalšiu.

\subsubsection{Pytagoras}
To je ono!
\label{subsec:pytagoras}

% Použitím '*' môžeme potlačiť zabudované číslovanie LaTeXu.
% Toto funguje aj na iné príkazy. 
\section*{Toto je nečíslovaná sekcia} 
Všetky číslované byť nemusia!

\section{Nejaké poznámočky}
Zarovnávať veci tam, kde ich chceš mať, je všeobecne ľahké. Ak 
potrebuješ \\ nový \\ riadok \\ pridaj \textbackslash\textbackslash do 
zdrojového kódu. \\ 

\section{Zoznamy}
Zoznamy sú jednou z najjednoduchších vecí vôbec! Treba mi zajtra nakúpiť, urobím si zoznam.
\begin{enumerate} % "enumerate" spustí číslovanie prvkov.
  % \item povie LaTeXu, ako že treba pripočítať 1 
  \item Vlašský šalát.
  \item 5 rožkov.
  \item 3 Horalky.
  % číslovanie môžeme pozmeniť použitím []
  \item[koľko?] Stredne veľkých guličkoviek.

  Ja už nie som položka zoznamu, no stále som časť "enumerate".

\end{enumerate} % Všetky prostredia končia s "end".

\section{Matika}

Jedným z primárnych použití LaTeXu je písanie akademických, či technických prác. Zvyčajne za použitia matematiky a vedy. Podpora špeciálnych symbolov preto nemôže chýbať!\\

Matematika má veľa symbolov, omnoho viac, než by klávesnica mohla reprezentovať;
Množinové a relačné symboly, šípky, operátory a Grécke písmená sú len malou ukážkou.\\

Množiny a relácie hrajú hlavnú rolu v mnohých matematických článkoch.
Takto napíšeš, že niečo platí pre všetky x patriace do X, $\forall$ x $\in$ X. \\
% Všimni si, že som pridal $ pred a po symboloch. Je to 
% preto, lebo pri písaní sme v textovom móde, 
% no matematické symboly existujú len v matematickom. 
% Vstúpime doňho z textového práve '$' znamienkami.
% Platí to aj opačne. Premenná môže byť zobrazená v matematickom móde takisto.
% Do matematického módu sa dá dostať aj s \[\]

\[a^2 + b^2 = c^2 \]

Moje obľúbené Grécke písmeno je $\xi$. Tiež sa mi pozdávajú $\beta$, $\gamma$ a $\sigma$.
Ešte som neprišiel na Grécke písmeno, ktoré by LaTeX nepoznal!

Operátory sú dôležitou súčasťou matematických dokumentov: 
goniometrické funkcie ($\sin$, $\cos$, $\tan$), 
logaritmy and exponenciálne výrazy ($\log$, $\exp$), 
limity ($\lim$), atď. 
majú pred-definované LaTeXové príkazy. 
Napíšme si rovnicu, nech vidíme, ako to funguje: \\

$\cos(2\theta) = \cos^{2}(\theta) - \sin^{2}(\theta)$

Zlomky(Čitateľ-menovateľ) sa píšu v týchto formách:

% 10 / 7
$^{10}/_{7}$ 

% Relatívne komplexné zlomky sa píšu ako
% \frac{čitateľ}{menovateľ}
$\frac{n!}{k!(n - k)!}$ \\

Rovnice tiež môžeme zadať v "rovnicovom prostredí". 

% Takto funguje rovnicové prostredie
\begin{equation} % vstúpi do matematického módu
    c^2 = a^2 + b^2.
    \label{eq:pythagoras} % na odkazovanie
\end{equation} % všetky \begin príkazy musia mať konečný príkaz.

Teraz môžeme odkázať na novovytvorenú rovnicu! 
Rovn.~\ref{eq:pythagoras} je tiež známa ako Pytagorova Veta, ktorá je tiež predmetom Sekc.~\ref{subsec:pytagoras}. Odkazovať môžme na veľa vecí, napr na: čísla, rovnice, či sekcie.

Sumácie a Integrály sa píšu príkazmi sum a int:

% Niektoré prekladače LaTeXu sa môžu sťažovať na prázdne riadky (ak tam sú)
% v rovnicovom prostredí.
\begin{equation} 
  \sum_{i=0}^{5} f_{i}
\end{equation} 
\begin{equation} 
  \int_{0}^{\infty} \mathrm{e}^{-x} \mathrm{d}x
\end{equation} 

\section{Obrázky}

Vloženie obrázku môže byť zložitejšie. Ja si vždy možnosti vloženia pozerám pre každý obrázok.
\renewcommand\figurename{Obrázok}
\begin{figure}[H] % H značí možnosť zarovnania. 
    \centering % nacentruje obrázok na stránku
    % Vloží obrázok na 80% šírky stránky.
    %\includegraphics[width=0.8\linewidth]{right-triangle.png} 
    % Zakomentované kvôli kompilácií, použi svoju predstavivosť :).
    \caption{Pravouhlý trojuholník so stranami $a$, $b$, $c$}
    \label{fig:right-triangle}
\end{figure}
% Opäť, fixné makro "table" nahradíme slovenskou tabuľkou. Pokiaľ preferuješ table, nasledujúci riadok nepridávaj
\renewcommand\tablename{Tabuľka}

\subsection{Tabuľky}
Tabuľky sa vkládajú podobne ako obrázky.

\begin{table}[H]
  \caption{Nadpis tabuľky.}
  % zátvorky: {} hovoria ako sa vykreslí každý riadok.
  % Toto si nikdy nepamätám a vždy to musím hľadať. Všetko. Každý. Jeden. Raz!
  \begin{tabular}{c|cc} 
    Číslo & Priezvisko & Krstné meno \\ % Stĺpce sú rozdelené $
    \hline % horizontálna čiara
    1 & Ladislav & Meliško \\
    2 & Eva & Máziková
  \end{tabular}
\end{table}

% \section{Hyperlinks} % Už čoskoro :)

\section{Prikáž LaTeXu nekompilovať (napr. Zdrojový Kód)}
Povedzme, že chceme do dokumentu vložiť zdrojový kód, budeme musieť LaTeXu povedať, nech sa ho nesnaží skompilovať, ale nech s ním pracuje ako s textom.
Toto sa robí vo verbatim prostredí. 

% Tiež sú na to špeciálne balíčky, (napr. minty, lstlisting, atď.)
% ale verbatim je to najzákladnejšie, čo môžeš použiť.
\begin{verbatim} 
  print("Hello World!")
  a%b; pozri! Vo verbatime môžme použiť % znamienka. 
  random = 4; #priradené randomným hodom kockou
\end{verbatim}

\section{Kompilácia} 

Už by bolo načase túto nádheru skompilovať a zhliadnuť jej úžasnú úžasnosť v podobe LaTeX pdfka, čo povieš?
(áno, tento dokument sa musí kompilovať). \\
Cesta k finálnemu dokumentu pomocou LaTeXu pozostáva z nasledujúcich krokov:
  \begin{enumerate}
    \item Napíš dokument v čistom texte (v "zdrojáku").
    \item Skompiluj zdroják na získanie pdfka. 
     Kompilácia by mala vyzerať nasledovne (v Linuxe): \\
     \begin{verbatim} 
        $pdflatex learn-latex.tex learn-latex.pdf 
     \end{verbatim}
  \end{enumerate}

Mnoho LaTeX editorov kombinuje Krok 1 a Krok 2 v jednom prostredí. Krok 1 teda uvidíš, krok 2 už nie.
Ten sa deje za oponou. Kompilácia v 2. kroku sa postará o produkciu dokumentu v tebou zadanom formáte.

\section{Koniec}

To je zatiaľ všetko!

% koniec dokumentu
\end{document}
```

## Viac o LaTeXe (anglicky)

* Úžasná LaTeX wikikniha: [https://en.wikibooks.org/wiki/LaTeX](https://en.wikibooks.org/wiki/LaTeX)
* Naozajstný tutoriál: [http://www.latex-tutorial.com/](http://www.latex-tutorial.com/)
