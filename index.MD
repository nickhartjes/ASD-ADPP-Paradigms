# Rust roest

[toc]

## Inleiding

"Rust roest" en dan heb ik het niet over de [televisieserie](https://nl.wikipedia.org/wiki/Rust_roest_(televisieserie)), maar dan heb ik het over het [spreekwoord](https://www.dbnl.org/tekst/stoe002nede01_01/stoe002nede01_01_2040.php). Het spreekwoord is ontleent aan ijzer, dat wanneer het gebruikt word blank blijft, maar wanneer het stil ligt gaat roesten. Dit gaat natuurlijk ook op in de wereld van programmeurs. Er blijft een continue stroom van nieuwe informatie komen, nieuwe technieken, andere talen, meer gespecializeerde frameworks, handige tools en ga zo maar door. Want zwem je niet met de stroom mee, ga je roesten. Gedoomd tot een leven lang leren ? Of steeds een nieuwe uitdaging om enthausiast van te worden. In mijn blog wil ik jullie meenemen in een nieuwe uitdaging die ik mezelf gegeven heb.

## De uitdaging

In mijn dagelijks werkzaamheden gebruik ik hoofdzakelijk Java, en daarnaast af en toe wat C#, maar veel variatie daarnaast is er niet. Dit zijn beide talen vanuit het objectgeoriënteerd  programmeren paradigma. Mijn nieuwe uitdaging is dus ook, om uit dit paradigma te stappen en een compleet andere programmeer taal te kiezen uit een ander paradigma. Maar voordat we doen zoomen we heel even in wat nu een programmeerparadigma is, en welke gangbare paradigma's er zijn.


### Programmeerparadigma's

> In de informatica zijn programmeerparadigma's denkpatronen of uitgesproken concepten van programmeren, die voornamelijk verschillen in de wijze van aanpak om het gewenste resultaat te kunnen behalen.

#### Gangbare paradigma's
De belangrijkste programmeerparadigma's zijn:

- Imperatief programmeren
- Functioneel programmeren
- Logisch programmeren
- Objectgeoriënteerd programmeren

In **imperatief programmeren** is een programma in essentie een reeks instructies die het geheugen manipuleren en die op volgorde door de computer worden uitgevoerd. Deze stijl van programmeren staat dicht bij de werking van een computer en werden derhalve als eerste praktisch gerealiseerd.

**Functioneel programmeren** is gebaseerd op formalismen zoals de theorie van recursieve functies of de lambdacalculus-programma's. Hieronder worden wiskundige functies gedefinieerd die invoer naar uitvoer transformeren.

Bij **logisch programmeren**, gebaseerd op (doorgaans) predicatenlogica, zijn het definities van predicaten die een bepaalde relatie tussen objecten in het geheugen uitdrukken.

**Objectgeoriënteerd programmeren** (object oriented programming) verenigt berekening en de gegevens: deze worden verpakt in objecten, waarbij de details worden verborgen achter een algemene interface, vaak gerangschikt in een hiërarchie van klassen. Objecten sturen elkaar berichten (Smalltalk) of roepen elkaars methoden aan (C++, Java); alleen zo hebben ze toegang tot elkaars gegevens. De methoden/reacties op berichten zijn procedures die de interne gegevens van een object manipuleren.



### De keuze

Om makkelijker te kunnen kiezen heb ik een shortlist gemaakt van potentiele talen, en een overzicht gemaakt van paradigma's waarin deze talen vallen.


| Language | Intended use                  | Imperative | Object-oriented | Functional | Procedural | Generic | Reflective | Event-driven | Other paradigm(s)            | Standardized?                                            |
| -------- | ----------------------------- | ---------- | --------------- | ---------- | ---------- | ------- | ---------- | ------------ | ---------------------------- | -------------------------------------------------------- |
| Clojure  | General                       |            |                 | Yes        |            |         |            |              | concurrent                   | No                                                       |
| Erlang   | Application, distributed      |            |                 | Yes        |            |         |            | Yes          | concurrent, distributed      | No                                                       |
| F#       | Application                   | Yes        | Yes             | Yes        | Yes        | Yes     | Yes        | Yes          |                              | No                                                       |
| Haskell  | Application                   |            |                 | Yes        |            | Yes     |            |              | lazy evaluation              | 2010, Haskell 2010[27]                                   |
| Occam    | General                       | Yes        |                 |            | Yes        |         |            |              | concurrent, process-oriented | No                                                       |
| R        | Application, statistics       | Yes        | Yes             | Yes        | Yes        |         | Yes        |              |                              | No                                                       |
| Rust     | Application, system           | Yes        | Yes             | Yes        | Yes        | Yes     |            | Yes          | concurrent                   | No                                                       |
| Scala    | Application, distributed, web | Yes        | Yes             | Yes        |            | Yes     | Yes        | Yes          |                              | De facto standard via Scala Language Specification (SLS) |
 [Bron: Comparison of programming languages. (2019, October 10)](https://en.wikipedia.org/wiki/Comparison_of_programming_languages)

Wat direct opvalt, is dat er een aantal talen zijn die heel puur in 1 paradigma vallen zoals Clojure en Erlang. Maar dat er veel talen zijn die onder meer paradigma's vallen. Dan is het dus aan de programmeur om het op de juiste manier te gebruiken.

Maar een keuze maken is, en blijft nog steeds lastig met de huidige gegevens. En uiteindelijk heb ik er voor gekozen om me iets meer te verdiepen in de populariteit van dit moment van de talen in de shortlist.


##### Tiobe Index Oktober 2019

| Programming Language | Rank     | Ratings |
|----------------------|----------|---------|
| Clojure              | 51 – 100 | -       |
| Erlang               | 51 – 100 | -       |
| F#                   | 32       | 0.391%  |
| Haskell              | 43       | 0.209%  |
| Occam                | -        | -       |
| R                    | 15       | 1.261%  |
| Rust                 | 34       | 0.356%  |
| Scala                | 29       | 0.442%  |

##### PyPL Index Oktober 2019

| Programming Language | Rank | share  |
|----------------------|------|--------|
| Clojure              | -    | -      |
| Erlang               | -    | -      |
| F#                   | -    | -      |
| Haskell              | 21   | 0.29 % |
| Occam                | -    | -      |
| R                    | 7    | 3.82 % |
| Rust                 | 18   | 0.64 % |
| Scala                | 16   | 1.15 % |

##### Stackoverflow Survey 2019 - Mosted used

| Programming Language | Rank | share |
|----------------------|------|-------|
| Clojure              | 24   | 1.50% |
| Erlang               | -    | -     |
| F#                   | -    | -     |
| Haskell              | -    | -     |
| Occam                | -    | -     |
| R                    | 16   | 5.60% |
| Rust                 | 21   | 3.00% |
| Scala                | 20   | 4.20% |

##### Stackoverflow Survey 2019 - Mosted loved

| Programming Language | Rank | share  |
|----------------------|------|--------|
| Clojure              | 7    | 68.30% |
| Erlang               | 22   | 47.40% |
| F#                   | 15   | 61.70% |
| Haskell              | -    | -      |
| Occam                | -    | -      |
| R                    | 20   | 51.70% |
| Rust                 | 1    | 83.50% |
| Scala                | 17   | 58.03% |



##### Overview

| Ranking | Programming Language | Tiobe | PyPL | SO - MU | SO – ML |
|---------|----------------------|-------|------|---------|---------|
| 1       | R                    | 15    | 7    | 16      | 20      |
| 2       | Rust                 | 34    | 18   | 21      | 1       |
| 3       | Scala                | 29    | 16   | 20      | 17      |
| 4       | Clojure              | 50    |      | 24      | 7       |
| 5       | F#                   | 32    |      |         | 15      |
| 6       | Haskell              | 43    | 21   |         |         |
| 7       | Erlang               | 50    |      |         | 22      |
| 8       | Occam                |       |      |         |         |

Flow Control Rust vs Java

| Rust                          | Java                              |
| ----------------------------- | --------------------------------- |
| break / break 'label          | break / break label               |
| continue / continue 'label    | continue / continue label         |
| for i in 0..n { _ } ¹         | for (int i = 0; i < n; i++) { _ } |
| for i in _ { _ }              | for (X i : _) { _ }               |
| if _ { _ } else { _ }         | if (_) { _ } else { _ }           |
| if let _ = _ { _ } else { _ } | if (_ = _) { _ } else { _ }       |
| loop { _ }                    | while (true) { _ }                |
| loop { .. ; if _ { break; }}  | do { .. } while (_);              |
| match _ { .. }                | switch (_) { .. } ²               |
| return _                      | return _                          |
| while _ { _ }                 | while (_) { _ }                   |
| while let _ = _ { _ }         | while (_ = _) { _ }               |

```rust
let mut new_length = length.clone() + 1;
```

Syntaxis: vorm
Aan welke vormregels moet een tekst voldoen om bij de taal te horen?
Semantiek: betekenis
Wat doen programma’s in de taal als we deze uitvoeren?
Pragmatiek: toepassing
Hoe schrijf je het het beste op, met de gewenste betekenis?

### Bronnen voor het blog

Programmeerparadigma. (2018, February 7). Retrieved from https://nl.wikipedia.org/wiki/Programmeerparadigma.

Comparison of programming languages. (2019, October 10). Retrieved from https://en.wikipedia.org/wiki/Comparison_of_programming_languages.

Tiobe Index. (2019, October). Retrieved from https://www.tiobe.com/tiobe-index/.

https://pypl.github.io/PYPL.html

https://insights.stackoverflow.com/survey/2019#technology

https://llogiq.github.io/2016/02/28/java-rust.html