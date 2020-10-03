---
layout: post
title:  Regex
date:   2020-10-03 18:20:55 +0200
categories: Learn Regex
---
# What is the meaning of life, the universe and everything?
```
^(?=(?!(.)\1)([^\DO:105-93+30])(?-1)(?<!\d(?<=(?![5-90-3])\d))).[^\WHY?]$
```
Referència a Regex + Vim `usr_42.txt` + Douglas Adams
# Història (força discutible xD) Dens, curiós i molt per aprendre.
En anglès, tenim que el plural de Regex és Regex**es**.
Hi ha una discussió de la diferència entre expressions regulars i regex: <https://www.rexegg.com/regex-vs-regular-expression.html>
Si diem que les expressions regulars són degudes al matemàtic Stephen Cole Kleene, aquest mostra el teorema de Kleene que diu que tota expressió regular es pot mostrar amb un automata finit.
Aquest home va estudiar també amb Alan Turing.
`TODOTODO` Kleene's theorem
<https://fr.wikipedia.org/wiki/Stephen_Cole_Kleene> També parla de recursivitat, entre altres

(the 1950s, at the dawn of computer science) a regular expression referred to what the mathematician Stephen Kleene described as a regular language
Regular expression engines that conformed to this regularity were called Deterministic Finite Automatons (DFAs).
In the late 1960s Ken Thompson of Bell Labs wrote them into the editor QED, and in the 1970s they made it into Unix programs and utilities such as grep, sed and AWK.
The engines that process this expanded regular expression syntax were no longer DFAs—they are called Non-Deterministic Finite Automatons (NFAs).
Perl had a huge influence: "Perl-style"

## Deterministic Finite Automatons
`TODOTODO` posar LaTex per a poder fer l'explicació correcta.

## Regex vs regular expressions
The engines that process this expanded regular expression syntax were no longer DFAs—they are called Non-Deterministic Finite Automatons (NFAs).
At that stage, regex patterns could no longer said to be regular in the mathematical sense.
This is why a small minority of people today (most of whom have email addresses ending with .edu) will maintain that what we call regex are not regular expressions.

For the rest of us… Regex and regular expressions? Same-same.

# Que és?
A regex is a text string that describes a pattern that a regex engine uses in order to find text (or positions) in a body of text, typically for the purposes of validating, finding, replacing or splitting.

## Motor
`TODOTODO` m'agradaria fer un prototip amb Kotlin o llenguatge agradable i amigable

Té principalment dos caps, un que llegeix el PATTERN, i l'altre que llegeix l'INPUT.

# Com escriurem la Regex?
Cosa que em sembla important definir, ja que hi ha qui parla de Regex coses que no ho són.
Escriurem la Regex sempre des del punt de vista purista.
No volem afegir el soroll d'escapament de caràcters de *Python*, *Java* o el llenguatge que sigui.

Per exemple, amb *bash*:
```bash
printf "%s\n" sense\ parentesis\ has\ d\'escapar\ els\ espais
printf "%s\n" "Aquí has d'escapar els \$"
printf "%s\n" 'Aquí cal escapar els \'\'
```
<!--
cat << EndOfMessage
jo sóc d'aquí i puc fer el que em roti menys escriure sense espais: End Of Message
EndOfMessage
-->

# Fundamental
Entenem com complex dominar:
- Els `(?X)` on `X in {permutacións d'estrings}`
- Condicionals
- Recursivitat

Recomanació per aprendre Regex:
- <https://www.rexegg.com/regex-quickstart.html>
- <https://www.rexegg.com/regex-disambiguation.html>
- <https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html>

Tenim diferents conecptes importants:
- Characters: `. \d \w \s`
  - Character Classes: `[a1] [^x] [a-m] [\d\D]`
- Quantifiers: `{1} {2,} {3,4} * + ?`
  - `* ≡ {0,}, + ≡ {1,}, ? ≡ {0,1}`
  - Quantifiers + ? -> Lazy quantifier
  - Quantifiers + + -> TODOTODO
- Logic: `| () \1`
- Anchors and Boundaries: `^$ \A\z`
- Inline Modifiers
  - (?i): Case-insensitive mode
  - (?s): DOTALL mode: `\n`
  - (?m): Multiline mode, vigilar que la regex no exploti.
  - (?x): Free-Spacing Mode mode, vigilar que els espais desitjats s'han d'escapar.

`TODOTODO` grups

# Referències
- <https://www.rexegg.com/>
